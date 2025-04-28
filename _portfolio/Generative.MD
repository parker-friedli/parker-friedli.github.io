---

title: "Digital Caliper Stand Using Generative Design"
excerpt: "Using Fusions generative design workspace to create digital caliper stand."
header:
  image: /assets/img/caliper_stand_render.png
  teaser: /assets/img/caliper_stand_render.png
gallery:
  - image_path: assets/img/gen_1.png
  - image_path: assets/img/gen_2.png
  - image_path: assets/img/gen_3.png
  - image_path: assets/img/gen_4.png
  - image_path: assets/img/gen_5.png

---


## Project Overview

The purpose of this project was to produce a stand for 6-inch digital calipers using generative desig stand for use in lab/workshop environments. It provides a stable, upright storage solution that keeps calipers accessible for quick use and protecting them from damage. While a caliper stand is not traditionally the type of component optimized through generative design—compared to brackets or structural assemblies—this project adapted the use case to explore the generative design process and produce a unique asthetic design. The choice for a calipers stand was made based on the fact it is the tool I frequently rely on in fabrication and coursework, and creating a dedicated, space-efficient holder directly improved organization with the added benefit of display. 

---
## Design Setup

### Preserve and Obstacle Geometry
<p align="center">
  <img src="/assets/img/fbd.png" width="75%">
</p>

After creating a simplified model of the calipers, additional perserve and obsticle geometries were created with the goal of providing support of the calipers. Specifically, preserve geometries were created at three contact points where the caliper body rests: the main blade/scale of caliper (longest part of the body), a back rest behind the calipers center of mass, and an area to cradle the lower measurement jaws. A fourth preserve geometry was created to serve as a base footprint to rest on table or other surface.

**Preserve Geometries *(green components)***
  - **Main Blade/Scale Support:**  
    A preserve region along the length of the caliper’s main blade was created to provide continuous support for the body during storage.
  
  - **Back Rest Support:**  
    A preserve located behind the caliper’s center of mass stabilized the tool and prevented tipping backward while resting in the stand.
  
  - **Lower Jaw Cradle:**  
    A preserve cradle was positioned under the lower measurement jaws to protect and support the caliper’s most sensitive measuring surfaces.
  
  - **Base Footprint:**  
    A preserve was added to define a stable base platform where the stand rests securely on a table or workbench surface.

<p align="center">
  <img src="/assets/img/preserve.png" width="75%">
</p>

Obstacle geometries were defined around the areas where the caliper would need to move freely. Meaning the main obstacle geometry involved the simplified model of the calipers with an obstacle offset of 0.5 mm. The second geometry invloved a simplified rectangular prism placed in front of the main caliper body to ensure the measurement guide would be both visible while displayed and easily grabbed by this portion to take the calipers off of the stand. Additional preserve geometries were created in the base footprint to serve as storage space for additional caliper batteries. Note that the preserve geometry for the batteries was defined to be taller than the batteries to ensure the model would not generate in the space above such that the batteries could still be able to be removed when needed.

  
  **Obstacle Geometries *(red components)***
  
   - **Caliper Clearance Volume:**  
    The entire simplified caliper body was designated as obstacle geometry with a 0.5 mm offset, ensuring that the generative model would not interfere with inserting or removing the caliper.
  
  - **Grip Clearance:**  
    A rectangular obstacle volume was added in front of the main caliper body to maintain clear access to the caliper’s measurement guide, allowing easy grasping for removal from the stand.
  
  - **Battery Access Clearance:**  
    The preserve volume for the battery storage areas was extended vertically to prevent material generation above the batteries, ensuring they remain accessible.

<p align="center">
  <img src="/assets/img/front.png" width="45%">
  <img src="/assets/img/back.png" width="45%">
</p>

### Load Cases and Structural Constraints

### Types of Forces Applied
Three types of forces were applied in the generative design study:
- *Normal Force:* Simulated the weight of the caliper resting on the stand, applied at center of mass. Additional normal forces at all contact points simulating compression from weight of caliper.
- *Lateral Shear Load:* Represented small side forces from incidental bumps or sliding contact during placement or removal.
- *Moment (Tipping Load):* Modeled the potential tipping effect if the caliper was placed unevenly, and to represent excess moment of weight from unsported section of caliper. 

<p align="center">
  <img src="/assets/img/normal.png" width="30%">
  <img src="/assets/img/moment.png" width="30%">
  <img src="/assets/img/shear.png" width="30%">
</p>

Each of these forces were applied in excess (i.e. high safety factor) such that the final design maintained both stability and functionality during  use, accounting for main static loads (the caliper’s weight) as well as possible dynamic interactions (bumping and tipping).

### Load Magnitude, Direction, and Location
- The *vertical normal load* was estimated at approximately 3 N, based on the mass of a typical 6-inch digital caliper (~300 grams) and converted using $$F = m \times g$$
- The *lateral shear load* was estimated at about 2 N, accounting for light side impacts from a user's hand or workspace movement.
- The *moment load* was approximated at 0.3 Nm to represent a small rotational force acting around the base edge if the caliper was bumped unevenly.

Loads were applied at the main contact points where the caliper body rests: the blade/scale support area, the lower jaw cradle, and the back rest. The moment was centered around the footprint where the stand contacts the surface.

### Structural Constraints
Fixed constraints were applied at the bottom face of the base footprint to simulate the stand resting securely on a flat table surface. This constraint anchored the stand during the generative process, ensuring that optimization efforts focused on reinforcing the load paths above the base while minimizing material in less critical regions. The fixed boundary conditions helped the generative design produce a structure that maintained stability without unnecessarily thickening the base, contributing to weight reduction.

### Real-World Testing to Refine Loads
The prototype can be tested by placing a caliper onto the stand and simulating everyday handling conditions. Testing would involve:
- Applying vertical loading by resting and removing the caliper repeatedly.
- Simulating shear forces by lightly pushing the caliper from the side to test lateral stability.
- Intentionally applying small tipping forces to verify the stand’s resistance to overturning.

If excessive flexing, deformation, or instability is observed during testing, adjustments could be made to refine the estimated loads or modify preserve regions to reinforce weak points. Real-world testing ensures that the simplified load assumptions made during the generative setup accurately reflect how the stand behaves under true usage conditions.

| Force Name           | Approximate Magnitude | Applied Location                   | Purpose                                                                                  |
|----------------------|------------------------|-------------------------------------|------------------------------------------------------------------------------------------|
| Normal Force         | ~3 N (distributed)      | Center of mass and contact points   | Simulate caliper weight and localized compression at main support areas                 |
| Lateral Shear Load   | ~2 N                    | Side of caliper body and stand      | Simulate side impacts or incidental bumps during placement and removal                  |
| Moment (Tipping Load)| ~0.3 Nm                 | Around base footprint              | Simulate tipping from uneven placement and excess moment from unsupported caliper mass   |

- **Structural Constraints:**
  - Fixed constraint applied at the bottom of the base, simulating a stable surface like a lab table.

---
## Generative Design Process
- **Software:** Autodesk Fusion 360 (Generative Design workspace)
- **Material:** Nylon 12 (PA12) using SLS (Selective Laser Sintering) on the Formlabs Fuse 1 printer
- **Unrestricted Manufacturing:**  
  Full use of unrestricted manufacturing settings to take advantage of the SLS process and allow complex geometries without support structures.
- **Additive Z-Axis Constraint:**  
  Additive manufacturing along the Z-axis was enabled to allow for prototyping, as setting allowed for minor design corrections or small features to be easily modified or repaired with FF 3D printing if necessary during iteration.

### Workflow Summary
Created a simplified model of the calipers to define critical interfaces and clearances.
- Defined reserve geometries at three main caliper contact points (blade/scale support, lower jaw cradle, back rest) and the base footprint for surface stability.
- Created obstacle geometries around the caliper clearance volume (with 0.5 mm offset), around the gripping area for easy removal, and above the battery storage locations to maintain access.
- Applied three main types of loads to the preserves:  
  *Normal forces* to simulate caliper weight, *lateral shear* to simulate side impacts, and *tipping moments* to model uneven placement stresses.
- Applied fixed constraints along the bottom surface of the base footprint to simulate a rigid surface interaction.
- Ran multiple generative design studies prioritizing lightweighting while maintaining sufficient stiffness and support at contact points.
- Selected a final geometry that balanced minimal mass with functional stability and clearance requirements for everyday caliper use.

### Fusion 360 Iterations
  
