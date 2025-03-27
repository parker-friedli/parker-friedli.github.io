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

Common Filament bonding characteristics for multi-material printing...

| Material 1 | Material 2   | Bonding Behavior[^1][^2]    |
|------------|--------------|-----------------------------|
| PLA        | PVA          | No bonding (dissolvable)    | 
| PETG       | TPU (95A)    | Partial bonding             | 
| ABS        | TPU          | Good adhesion               | 
| PLA        | TPU          | Weak adhesion               | 
| Nylon      | TPU          | Strong adhesion             |


---


## Design Description

The initial design concept was inspired by a common 3D-printed plier mechanism that incorporates a thermoplastic polyurethane (TPU) grid as the central spring component. This approach, as seen in designs such as the ColorFabb 3D-printed pliers (left image[^3], and right image[^4]) which utilizes the flexible TPU grid to provide a restoring force, allowing the pliers to return to their open position after being squeezed. This method effectively replaces traditional metal springs with a fully 3D-printed solution, making it ideal for integrating multiple materials with 3D Printing. 

<p align="center">
  <img src="/assets/img/reference.png/" width="30%">
  <img src="https://learn.colorfabb.com/wp-content/uploads/2017/01/colorfabb_flexi_tang-2.jpg" width="45%">
</p>


Building on this concept, the design evolved to resemble tweezers rather than pliers, for the purpose of enabling finer control and improved precision. While the TPU grid was retained as the central spring element, its dimensions and structure were adjusted to fit the new geometry. Several spring types were designed and tested to find the best iteration with good control, and enough resistance to return the tweezers to open position without excessive force needed to close. 

For example the first spring iteration consisted of a rectangular section with dove tails to connect to the tweezer body. Eliminating the top and bottom layers in SuperSlicer and varying the wall thickness, and infill precentages allowed me to iteratively test various spring constant using the same model.


<p align="center">  
  <img src="/assets/img/box_tweezer.jpeg/" height="150%" width="45%">  
  <img src="/assets/img/spring_infill_Change.png/" width="45%">  
  <br/>
  <em>Tweezer iteration with rectangular spring element (left). Super slicer settings with various infill percentages (right).</em>
</p>

The rectangular spring element was found to be too stiff and so I tested other spring geometries, including a flat spring iterations, and an accordion spring.  

|            |              |                 |
|------------| ------------ | ------------ |
| ![](/assets/img/spring5.png/) | ![](/assets/img/spring6.png/) | ![](/assets/img/coil_spring.png/)|

<p align="center">
  <img src="/assets/img/spring5.png/" width="30%">
  <img src="/assets/img/spring6.png/" width="30%">
  <img src="/assets/img/coil_spring.png/" width="30%">
</p>

The final chosen design can be seen below. This set of tweezers includes a 
* Relevant specifications of the pliers (jaw length, jaw capacity)



## CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a4320aaac0bce5af5e?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>


## Printing Details
**Print Settings:**

- Rigid Parts: PLA (standard extrusion settings)

- Flexible Spring: 95A TPU (lower speed, higher retraction)

- Layer Height: 0.2mm

- Infill: 100% for rigid parts, 100% for TPU spring

- Print Orientation: Optimized to ensure moving parts are free after printing

## Image Gallery and GIF  

<p align="center">
  <img width="550" src="/assets/img/IMG_5140.gif/">
</p>

{% include gallery caption="Syringe Pump Project Gallery" %}

## References
[^1]: G. L. Goh, S. Lee, S. H. Cheng, D. J. S. Goh, P. Laya, V. P. Nguyen, B. S. Han, and W. Y. Yeong, "Enhancing interlaminar adhesion in multi-material 3D printing: A study of conductive PLA and TPU interfaces through fused filament fabrication," Mater. Sci. Addit. Manuf., vol. 3, no. 1, p. 2672, 2024. doi: 10.36922/msam.2672.
[^2]: Tom's 3D, "Try these filament combinations for multi-material and supports," Tom's 3D Printing Guides and Reviews, Dec. 6, 2024. [Online]. Available: https://toms3d.org/2024/12/06/try-these-filament-combinations-for-multi-material-and-supports/. [Accessed: Mar. 26, 2025].
[^3]: ColorFabb. "Pliers." ColorFabb, 6 Dec. 2024, https://learn.colorfabb.com/pliers/.
[^4]: A. Ion et al., "Metamaterial Mechanisms," in Proceedings of the 29th Annual Symposium on User Interface Software and Technology (UIST '16), 2016, pp. 529–539. doi: 10.1145/2984511.2984540.


