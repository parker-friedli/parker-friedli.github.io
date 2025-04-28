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
  ### Preserve and Obstacle Geometry

After creating a simplified model of the calipers, additional perserve and obsticle geometries were created with the goal of providing support of the calipers. Specifically, preserve geometries were created at three contact points where the caliper body rests: the main blade/scale of caliper (longest part of the body), a back rest behind the calipers center of mass, and an area to cradle the lower measurement jaws. A fourth preserve geometry was created to serve as a base footprint to rest on table or other surface.

Obstacle geometries were defined around the areas where the caliper would need to move freely. Meaning the main obstacle geometry involved the simplified model of the calipers with an obstacle offset of 0.5 mm. The second geometry invloved a simplified rectangular prism placed in front of the main caliper body to ensure the measurement guide would be both visible while displayed and easily grabbed by this portion to take the calipers off of the stand. Additional preserve geometries were created in the base footprint to serve as storage space for additional caliper batteries. Note that the preserve geometry for the batteries was defined to be taller than the batteries to ensure the model would not generate in the space above such that the batteries could still be accessible by hand.

  - **Preserve Geometry**
    - Mounting cradle contact points for securing the caliper.
    - Stable base footprint to resist tipping.
    - Support arms that maintain visibility of the display without blocking the caliper jaws.
  - **Obstacle Geometry:**
    - Clearance zones around caliper jaws.
    - Clearance for insertion/removal of caliper without obstruction.
    - Space reserved for buttons and screen access.


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
  
