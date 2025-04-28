---

title: "Digital Caliper Stand Using Generative Design"
excerpt: "Using Fusions generative design workspace to create digital caliper stand."
header:
  image: /assets/img/IMG_5183.jpeg
  teaser: /assets/img/IMG_5183.jpeg
gallery:
  - image_path: assets/img/Lower_clamp.png
  - image_path: assets/img/Upper_clamp.png
  - image_path: assets/img/Inner_detent.png
  - image_path: assets/img/outer_detent.png
  - image_path: assets/img/stretch_band.png
  - image_path: assets/img/Detent_cover.png
  - image_path: assets/img/slider.png
  - image_path: assets/img/Slider_holder.png

---


## Project Overview

The purpose of this project was to produce a stand for 6-inch digital calipers using generative desig stand for use in lab/workshop environments. It provides a stable, upright storage solution that keeps calipers accessible for quick use and protecting them from damage. While a caliper stand is not traditionally the type of component optimized through generative design—compared to brackets or structural assemblies—this project adapted the use case to explore the generative design process and produce a unique asthetic design. The choice for a calipers stand was made based on the fact it is the tool I frequently rely on in fabrication and coursework, and creating a dedicated, space-efficient holder directly improved organization with the added benefit of display. 

---
## Design Setup

###Preserve and Obstacle Geometry

<p align="center">
  <img src="/assets/img/front.png" width="45%">
  <img src="/assets/img/back.png" width="45%">
</p>

After creating a simplified model of the calipers, additional perserve and obsticle geometries were created with the goal of providing support of the calipers. Specifically, preserve geometries were created at three contact points where the caliper body rests: the main blade/scale of caliper (longest part of the body), a back rest behind the calipers center of mass, and an area to cradle the lower measurement jaws. A fourth preserve geometry was created to serve as a base footprint to rest on table or other surface.

Obstacle geometries were defined around the areas where the caliper would need to move freely. Meaning the main obstacle geometry involved the simplified model of the calipers with an obstacle offset of 0.5 mm. The second geometry invloved a simplified rectangular prism placed in front of the main caliper body to ensure the measurement guide would be both visible while displayed and easily grabbed by this portion to take the calipers off of the stand. Additional preserve geometries were created in the base footprint to serve as storage space for additional caliper batteries. Note that the preserve geometry for the batteries was defined to be taller than the batteries to ensure the model would not generate in the space above such that the batteries could still be able to be removed when needed.

  **Preserve Geometries *(green components)***
  - **Main Blade/Scale Support:**  
    A preserve region along the length of the caliper’s main blade was created to provide continuous support for the body during storage.
  
  - **Back Rest Support:**  
    A preserve located behind the caliper’s center of mass stabilized the tool and prevented tipping backward while resting in the stand.
  
  - **Lower Jaw Cradle:**  
    A preserve cradle was positioned under the lower measurement jaws to protect and support the caliper’s most sensitive measuring surfaces.
  
  - **Base Footprint:**  
    A preserve was added to define a stable base platform where the stand rests securely on a table or workbench surface.
  
  **Obstacle Geometries *(red components)***
  
   - **Caliper Clearance Volume:**  
    The entire simplified caliper body was designated as obstacle geometry with a 0.5 mm offset, ensuring that the generative model would not interfere with inserting or removing the caliper.
  
  - **Grip Clearance:**  
    A rectangular obstacle volume was added in front of the main caliper body to maintain clear access to the caliper’s measurement guide, allowing easy grasping for removal from the stand.
  
  - **Battery Access Clearance:**  
    The preserve volume for the battery storage areas was extended vertically to prevent material generation above the batteries, ensuring they remain accessible.


### Load Cases and Structural Constraints
  | Load Type         | Approximate Value | Application Area       | Reasoning                        |
|-------------------|-------------------|-------------------------|----------------------------------|
| Vertical Load     | ~3 N               | Support arms and base   | Support weight of caliper        |
| Lateral Shear     | ~2 N               | Cradle and holder area  | Simulate bumping during use      |
| Moment (Torque)   | ~0.3 Nm            | Base around center      | Simulate tipping from imbalance  |

- **Structural Constraints:**
  - Fixed constraint applied at the bottom of the base, simulating a stable surface like a lab bench.
  - Loads applied based on typical handling forces when placing or removing the caliper.


---
## Generative Design Process
  ### Workflow Summary
  ### Fusion 360 Iterations
  
