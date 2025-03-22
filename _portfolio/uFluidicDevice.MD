---

title: "Microfluidic Pinch Flow Fractination Device"
excerpt: "Utilizing SLA printing for the creation of precise microfluidic device."

header:
  image: /assets/img/IMG_5117.jpeg
  teaser: /assets/img/IMG_5117.jpeg
gallery:
  - image_path: assets/img/wiring.png
  - image_path: assets/img/drawing1.png
  - image_path: assets/img/drawing2.png
  - image_path: assets/img/drawing3.png
  - image_path: assets/img/drawing4.png
  - image_path: assets/img/drawing5.png

---
<img src="/assets/img/IMG_5117.jpeg" width="80%" />

## Introduction to uFluidic Devices
Microfluidic devices are systems that use small amounts of fluids which manipulate through channels ranging from tens to hundreds of micrometers. These channels function as small pipes that control flow, allowing for experimentation and analysis which extreme precision. These devices have allowed various fields, including biology, chemistry, and medicine, through the precise flow, rapid analysis, and minimizing reagent consumption; in essence functioning as a small *Lab on a chip*. [1]

uFluidic devices can be designed to serve various functions including…

* **Mixing**: These microscale channels enable precise fluid blending and combination, which is essential for conducting chemical processes and preparing samples for analysis
* **Chemical Reactions**: The microfluidic chamber's controlled environment enables precise chemical reactions for drug discovery and material synthesis
* **Separation**: Some devices can separate components within a mixture based on size, density, or other properties. 
This project involved the development of a microfluidic device that employs the technique of **pinch flow fractionation (PFF)**, a method that performs particle **separation** based on particle size.


**Basic Concept of PFF:**

PFF operates using a microchannel with a pinched segment to **separate** particles according to their size. The technique relies on the laminar flow profile within the microchannel, thereby eliminating the need for external fields (which are commonly used in other separation methods such as field flow fractionation).

**Mechanism:** 

The effectiveness of PFF is influenced by several factors:

- **Microchannel Geometry:** The design of the microchannel, particularly the width of the pinched segment and the angle at the transition between the pinched and broadened segments, plays a significant role in the separation efficiency. A narrower pinched segment typically results in improved separation.

| Principles of PPF [4]| Example Flow Profile [4] |
|---------|---------|
| ![](/assets/img/PFF.png) | ![](/assets/img/streamlines.png) |

- **Flow Rates:** The ratio of flow rates from the inlets is critical, as it determines the width of the particle-containing liquid in the pinched segment. This ratio influences the alignment of particles to the sidewall, thereby affecting the overall separation efficiency.

**Application:**

A specific application that requires the sorting of small particles is the isolation and purification of **circulating tumor cells (CTCs)** from blood samples for cancer diagnostics. CTCs are rare and often present in very low concentrations in the bloodstream, but their presence can provide valuable insights into cancer progression, metastasis, and treatment response. Pinch Flow Fractionation (PFF) can be used to separate CTCs from other blood components like red blood cells and white blood cells based on size. This separation enables further analysis of the CTCs, which could lead to early cancer detection, monitoring of treatment effectiveness, and personalized medicine approaches. [P Sajeesh, Ashis Jumar Sen, 2013]

## Procedure for Fabrication of Final Device from 3D-Printed Mold
The fabrication of the final (PDMS) device involved multiple steps to ensure functionality. The following describes the process in detail.

**1. CAD Model Design**
  - **Model Development:** The 3D model of the microfluidic device was designed using Fusion 360, incorporating all necessary features such as the inlets, broad section, outlets, and given design specifications. *The design specifics will be discused below.*

**2. 3D Printing and Mold Post-Processing**
  - **Mold Fabrication:** The mold was printed using a Formlabs 3+ SLA printer with Black Resin to achieve high feature fidelity and smooth surfaces. 
  - **Post-Processing:** After printing, the mold was washed in isopropyl alcohol (IPA) to remove uncured resin. It was then cured under UV light at 60 °C for approximately 60 seconds to enhance mechanical stability.
  - **Surface Inspection:** The mold was examined for defects and surface finish, ensuring that the surfaces were smooth enough to facilitate demolding and ensure no remaining un-cured resin residue.

**3. Parylene Coating**
- **Coating Application:** A parylene-C coating was applied to the mold using a chemical vapor deposition (CVD) system to ensure chemical inertness (no reaction with resin), and a non-stick surface. 
- **Deposition Process:** The manufacturer's recommended parameters were followed, to achieve uniform coverage.

**4. PDMS Casting and Curing**
- **PDMS Preparation:** A PDMS mixture was prepared by combining the elastomer base and curing agent at a 10:1 weight ratio. The mixture was stirred thoroughly to ensure homogeneity.
- **Degassing:** The prepared PDMS was placed in a vacuum desiccator for 30 minutes to eliminate trapped air bubbles.
- **Mold Casting:** The degassed PDMS was poured onto the parylene-coated mold, ensuring complete coverage of all microfluidic features.
- **Thermal Curing:** The mold was placed in an oven at 60°C for approximately 2 hours to fully cure the polymer.

**5. Plasma Bonding to a Glass Substrate**
- **Glass Preparation:** A glass microscope slide was cleaned thoroughly with acetone and IPA to remove contaminants and improve bonding efficiency.
- **Plasma Surface Activation:** Both the PDMS and glass surfaces were treated using a plasma cleaner (e.g., Harrick Plasma Cleaner) to induce surface activation, generating silanol groups for enhanced adhesion.
- **Bonding Process:** The PDMS layer was aligned with the glass slide and pressed together, forming a strong, bond due to the plasma activation.

## Discussion of Key Elements of uFluidic Device
- **Purpose of Parylene Coating:**
  The use of parylene coating on resin-printed molds is essential for compatibility, chemical resistance, and surface properties of the final microfluidic   devices. One of the primary challenges in using SLA 3D-printed molds for soft lithography is that most  resins inhibit PDMS curing, preventing accurate   replication of microfluidic features. Research has shown that SLA resins contain phosphine oxide-based photo-initiators, which leach out and interfere    with the platinum-based PDMS catalyst, effectively poisoning the curing process [3].  Parylene coating provides a solution by forming a protective   barrier on the mold surface, preventing direct contact between the PDMS and any residual inhibitors. Additionally, the coating ensures easy demolding of PDMS, preserving the integrity of the flow channels and microstructures while maintaining consistent and reproducible device fabrication. 
  ![](/assets/img/parlyene_coating.png)

- **Geometry for Sorting**

    $$ 
    y=(w_P - D_P/2)\frac{w_B}{w_P}
    $$
    
    where...\
      $$w_B=19 \text{ mm}$$\
      $$w_P=0.75 \text{ m}$$\
      $$D_{\text{small}}=0.150 \text{ m}$$\
      $$D_{\text{large}}=0.500 \text{ m}$$
    
    then...
      $$y_{\text{small}}=(0.75 \text{ mm}-(0.150 \text{ mm})/2)\frac{19\text{ mm}}{0.75 \text{ mm}}=17.10\text { mm}$$
      $$y_{\text{large}}=(0.75 \text{ mm}-(0.500 \text{ mm})/2)\frac{19\text{ mm}}{0.75 \text{ mm}}=12.667\text { mm}$$

|                |                |                |
|----------------|----------------|----------------|
|![](/assets/img/blank_mold.png) | ![](/assets/img/section_view.png)  | ![](/assets/img/Outlets_calibrated.png)  |
| Row 2, Cell 1  | Row 2, Cell 2  | Row 2, Cell 3  |


- **Flow Rate Uniformity and Streamline Stability**
- **Future Improvements Based on Testing**






# CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a43ec6ba2c8022d8a4?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>


![](/assets/img/syringe_real.png)
{% include gallery caption="Syringe Pump Project Gallery" %}
