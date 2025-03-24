---

title: "3D Printed Multi-material Pliers"
excerpt: "Utilizing pring-in-place principles to create usable 3D printed pliers"
header:
  image: /assets/img/multi-material.png
  teaser: /assets/img/multi-material.png
gallery:
  - image_path: assets/img/wiring.png
  - image_path: assets/img/drawing1.png
  - image_path: assets/img/drawing2.png
  - image_path: assets/img/drawing3.png
  - image_path: assets/img/drawing4.png
  - image_path: assets/img/drawing5.png


---

---   
### Overview
This project focuses on creating functional print-in-place pliers that need no post-processing or assembly. These pliers are designed to grip and pick up through-hole resistors, with a *flexible spring component* that returns them to an open position when released.  

The success of print-in-place designs depends on precise clearances between moving parts to ensure smooth operation right after printing. While extrusion-based 3D printing can create inconsistencies that lead to stiff or "crunchy" movement, this design solves that challenge by using a separately printed flexible spring component. This addition improves both the pliers' range of motion and durability.

###  What Are Print-in-Place Models?
Print-in-place (PIP) designs enable the creation of complex, multi-component mechanisms in a single, ready-to-use print. These designs excel in applications featuring articulating joints, hinges, or interlocking components. PIP designs require precise clearances and print orientation to prevent component fusion during printing. Moreover, multi-material printing can add flexibility to specific areas of the design, enhancing functionality.  

  **Aplications for PIP**  

| Articulated Models | Mechanical Components | Integrated Mechanisms |
|----------------|----------------|----------------|
|Movable figures, such as chains, gears, and animals with articulated limbs, allowing for parts to flex or rotate relative to each other without assembly.​|Functional parts like gears, levers, or hinges printed as a single piece with operational movement.|Devices with built-in functional systems, such as springs or latches, that operate immediately after printing.​|
| ![](https://videos.cults3d.com/sgSNbXrXnt_-62i-8iVdVtn8nMM=/516x516/filters:no_upscale():format(webp)/https://fbi.cults3d.com/uploaders/14456321/illustration-file/29a252c6-99a3-444e-a0b5-fcf5fce5ad95/Lizard.gif) | ![](https://videos.cults3d.com/eLug1Dg-C9VvgmC65mXUKJNEc4s=/516x516/filters:no_upscale():format(webp)/https://fbi.cults3d.com/uploaders/13845051/illustration-file/771721dc-69c5-45b5-b1d7-04098e879400/giffff2.gif)  | ![](https://videos.cults3d.com/6sOGTx0mO1dUGfRKF4msWDAzS8w=/516x516/filters:no_upscale():format(webp)/https://fbi.cults3d.com/uploaders/13845051/illustration-file/092f3c23-dc8d-4035-addf-7686587f525b/working-gif.gif)  |


  **Multi-material Printing with PIP**
    Combining print-in-place with multi-material printing results in the advantage associated with with different materials, such as having both ridgid and flexible materials within a single print. By using different materials, PIP designs can incorporate elastic return mechanis, and grip-enhaving surfaces withtout requreing assembly and design changes if you were to print materials separately. However, for successful prints you have to select compatible material combinations. Factors such as adhesion properties, thermal compatibility, and the desired material property balance between felxibility and ridgity need to be taken into consideration. The goal is to integration materials that bond appropriately to ensure both sturctural integrity and the desired movement in the final product.

| Material 1 | Material 2   | Bonding Behavior[^1][^2]    |
|------------|--------------|-----------------------------|
| PLA        | PVA          | No bonding (dissolvable)    | 
| PETG       | TPU (95A)    | Partial bonding             | 
| ABS        | TPU          | Good adhesion               | 
| PLA        | TPU          | Weak adhesion               | 
| Nylon      | TPU          | Strong adhesion             |


---


## Design Description
* About the design and iterative process (e.g., how was the spring component created and how is it retained in the model, 
* materials used)
* Relevant specifications of the pliers (jaw length, jaw capacity)

## CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a4320aaac0bce5af5e?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>


## Print Settings

## Image Gallery and GIF  

## References
[^1]:
[^2]:
[^3]:

{% include gallery caption="Syringe Pump Project Gallery" %}
