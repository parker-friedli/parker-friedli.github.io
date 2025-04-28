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

## Project Overview

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
  
