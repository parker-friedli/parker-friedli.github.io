---

title: "Digital Caliper Stand | Generative Design Project"
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
# Digital Caliper Stand | Generative Design Project

## Project Overview
The final part is a lightweight, generatively designed stand for a standard 6-inch digital caliper. In typical lab and workshop environments, calipers are often placed loosely on benches, risking damage to their sensitive jaws and compromising measurement accuracy. Commercial caliper stands tend to be bulky, overbuilt, or not optimized for frequent handling.

This project aimed to create a compact, stable, and material-efficient stand that supports the caliper securely while allowing for easy access and safe storage. The generative design approach allowed the stand to maintain necessary mechanical support while minimizing material usage, resulting in an organic, efficient form ideal for SLS printing with PA12 nylon.

I chose this project because I use calipers regularly during coursework and fabrication projects, and I saw firsthand how common it is for these precision tools to get dropped or improperly stored. Designing a stand not only made the tool more accessible during daily use but also helped extend its lifespan, making this project personally meaningful and practically useful.

---
## Design Setup
  # Preserve and Obstacle Geometry
  - **Preserve Geometry**
    - Mounting cradle contact points for securing the caliper.
    - Stable base footprint to resist tipping.
    - Support arms that maintain visibility of the display without blocking the caliper jaws.
  - **Obstacle Geometry:**
    - Clearance zones around caliper jaws.
    - Clearance for insertion/removal of caliper without obstruction.
    - Space reserved for buttons and screen access.


  # Load Cases and Structural Constraints
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
  # Workflow Summary
  # Fusion 360 Iterations
  
