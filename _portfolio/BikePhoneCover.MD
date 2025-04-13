---

title: "Bike Phone Holder with Detent Mechanism"
excerpt: "Using Top-down Modeling Technique to design and filament 3D print a phone holder
for a bike."
header:
  image: /assets/img/IMG_5183.jpeg
  teaser: /assets/img/IMG_5183.jpeg
gallery:
  - image_path: assets/img/empty_box.png
  - image_path: assets/img/empty_dove.png
  - image_path: assets/img/full_box.png
  - image_path: assets/img/full_dove.png
  - image_path: assets/img/IMG_5145.jpeg

---
## Project Overview

This project features a 3D-printed phone holder designed to attach to bike handlebars. The design incorporates a spring-loaded detent mechanism that allows the phone to snap securely between orientations without the need for tools. Developed for both powder SLS and filament printing, the design was iteratively refined to optimize tolerances and clearances for a tight fit and durable assembly. The phone holder mounts to standard handlebars and remains stable during motion.

## Final Product

## Design Rationale
This phone holder was designed around two primary goals: functionality as a phone holder with ability to rotate between portrait and landscape orientations, and ability to be manufactured with available rapid prototyping methods.  When designing, a top-down modeling approach was used to establish correct fit with the given part dimensions and ensure components fit together smoothly. The top-down method involves starting with the overall assembly, using fixed references—such as the handle bar and phone-to define the spatial relationships between other components.  Individual parts were then modeled around these references to ensue precise fit and alignment. In essence, the top-down approach ensured the final holder functiond with the constrainsts of the given part dimensions, namely the handle bar diameter, phone size, and ball and spring detent parts.

A key feature of the design is the rotation mechanism, which uses a spring-loaded detent system to let the phone rotate cleanly between portrait and landscape orientations. The detents provide tactile feedback and help keep the phone stable. During early testing, however, it became clear that small forces on the handle bar-forces that would occur with normal riding condition-introduced enough vibration and jarring forces to sometimes cause unintended rotation of the detent mechanism. To address this, the spring stiffness was increased, and a slot feature (fig. X) was created to further increase the springe force by increasing the compression the spring. A stiffer spring raised the force required to rotate the phone, preventing it from shifting unless deliberately adjusted by the user. 

Another important aspect of the design was achieving a secure grip on the phone. To address this, two solutions were implemented:
1. A stretchable TPU grip that conforms around the edges of the phone to hold it in place.
2. A sliding clamp mechanism that adjusts to different phone sizes.
Both features work together to secure the device firmly without the need for tools. 


## Assembly & Use Instructions


## 3D Printing Process

## Component Gallery
## Bill of Materials

| Item No. | Part Name              | Quantity | Material        | Manufacturing Method | Notes                            |
|----------|------------------------|----------|------------------|---------------------|----------------------------------|
| 1        | Lower Handle Bar Clamp | 1        | Nylon            | SLS Powder Printing | Designed for 22.2 / 25.4 mm bars |
| 2        | Upper Handle Bar Clamp | 1        | Nylon            | SLS Powder Printing | Designed for 22.2 / 25.4 mm bars |
| 3        | Detent Base (Fixed)    | 1        | Nylon            | SLS Powder Printing | The stationary part with indents or pockets for the bearing.          |
| 4        | Detent Housing (Rotating)| 1      | Nylon            | SLS Powder Printing | The rotating part that holds the spring and allows movement.     
| 5        | Spring (Detent)        | 1        | Steel            | Off-the-shelf       | Compression spring               |
| 6        | Ball Bearing (Detent)  | 1        | Steel            | Off-the-shelf       | 8 mm Ball bearing                | 
| 7        | TPU Phone Grip         | 1        | TPU              | FFF 3D Printing     | Stretches to fit phone edges     |
| 8        | Phone Mount Frame      | 1        | PLA              | FFF 3D Printing     | Covers fixed detent base and supports sliding clamps; interfaces with TPU band for secure phone retention. |
| 9        | Phone Mount Slider     | 1        | PLA              | FFF 3D Printing     | Slides into Phone Mount Frame to secure phone. |
| 10       | Phone Mount Band       | 1        | TPU                | FFF 3D Printing     | Holds Phone Mount Frame and Slider together. |
| 11       | Heat Set Inserts (M5 x 6mm) | 3   | Brass            | Off-the-shelf       |              |
| 12       | Heat Set Inserts (M5 x 8mm) | 3   | Brass            | Off-the-shelf       |              |
| 13       | Socket Heat Screw (M5 x 20 mm)      | 2        | Alloy Steel  | Off-the-shelf       |              |
| 14       | Socket Heat Screw (M5 x 8 mm)      | 1        | Alloy Steel  | Off-the-shelf       |              |
| 15       | Socket Heat Screw (M5 x 8 mm)  | 3        | Alloy Steel  | Off-the-shelf       |              |


## Files & Downloads
