---

title: "Microfluidic Pinch Flow Fractination Device"
excerpt: "Utilizing SLA printing for the creation of precise microfluidic device."

header:
  image: /assets/img/IMG_5117.jpeg
  teaser: /assets/img/IMG_5117.jpeg

---


## Introduction to uFluidic Devices
Microfluidic devices are systems that use small amounts of fluids which manipulate through channels ranging from tens to hundreds of micrometers. These channels function as small pipes that control flow, allowing for experimentation and analysis which extreme precision. These devices have allowed various fields, including biology, chemistry, and medicine, through the precise flow, rapid analysis, and minimizing reagent consumption; in essence functioning as a small *Lab on a chip* [^1].

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

| Principles of PPF [^4]| Example Flow Profile [^4]|
|--------------------------|---------------------------------|
| ![](/assets/img/PFF.png) | ![](/assets/img/streamlines.png)|

- **Flow Rates:** The ratio of flow rates from the inlets is critical, as it determines the width of the particle-containing liquid in the pinched segment. This ratio influences the alignment of particles to the sidewall, thereby affecting the overall separation efficiency.

**Application:**

A specific application that requires the sorting of small particles is the isolation and purification of **circulating tumor cells (CTCs)** from blood samples for cancer diagnostics. CTCs are rare and often present in very low concentrations in the bloodstream, but their presence can provide valuable insights into cancer progression, metastasis, and treatment response. Pinch Flow Fractionation (PFF) can be used to separate CTCs from other blood components like red blood cells and white blood cells based on size. This separation enables further analysis of the CTCs, which could lead to early cancer detection, monitoring of treatment effectiveness, and personalized medicine approaches [^2].

## Procedure for Fabrication of Final Device from 3D-Printed Mold
The fabrication of the final (PDMS) device involved multiple steps to ensure functionality. The following describes the process in detail.

**1. CAD Model Design**
  - **Model Development:** The 3D model of the microfluidic device was designed using Fusion 360, incorporating all necessary features such as the inlets, broad section, outlets, and given design specifications (shown in figure below).
  
<p align="center">
  <img width="550" src="/assets/img/blank_mold.png">
</p>

**2. 3D Printing and Mold Post-Processing**
  - **Mold Fabrication:** The mold was printed using a Formlabs 3+ SLA printer with Black Resin to achieve high feature fidelity and smooth surfaces. 
  - **Post-Processing:** After printing, the mold was washed in isopropyl alcohol (IPA) to remove uncured resin. It was then cured under UV light at 60 °C for approximately 60 seconds to enhance mechanical stability [^1].
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

| Final SLS Mold with parylene coating|     Final PDMS device      |
|---------------------------------|--------------------------------|
| ![](/assets/img/final_mold.jpg) | ![](/assets/img/final_pdms.jpg) |

## Discussion of Key Elements of uFluidic Device
**Purpose of Parylene Coating:**  
  The use of parylene coating on resin-printed molds is essential for compatibility, chemical resistance, and surface properties of the final microfluidic   devices. One of the primary challenges in using SLA 3D-printed molds for soft lithography is that most  resins inhibit PDMS curing, preventing accurate   replication of microfluidic features. Research has shown that SLA resins contain phosphine oxide-based photo-initiators, which leach out and interfere    with the platinum-based PDMS catalyst, effectively poisoning the curing process [^3].  Parylene coating provides a solution by forming a protective   barrier on the mold surface, preventing direct contact between the PDMS and any residual inhibitors. Additionally, the coating ensures easy demolding of PDMS, preserving the integrity of the flow channels and microstructures while maintaining consistent and reproducible device fabrication. 

<p align="center">
  <img width="460" height="300" src="/assets/img/parlyene_coating.png">
</p>


**Geometry for Sorting:**The location of the outlet ports—determined by the height at which each particle is expected to exit—is a function of the widths of both the broad section ($$w_B$$) and pinched section ($$w_P$$), as well as the diameters of the small and large particles ( $$D_{\text{small}},D_{\text{large}}$$ ). he equation governing the height at which a particle exits is given by: 

  $$y=(w_P - D_P/2)\frac{w_B}{w_P}$$[^4]    

  where...   
  $$w_B=19 \text{ mm}$$   
  $$w_P=0.75 \text{ m}$$  
  $$D_{\text{small}}=0.150 \text{ m}$$  
  $$D_{\text{large}}=0.500 \text{ m}$$  
    
  Using these values, the predicted exit heights for small and large particles are calculated as follows...   
  $$y_{\text{small}}=(0.75 \text{ mm}-(0.150 \text{ mm})/2)\frac{19\text{ mm}}{0.75 \text{ mm}}=17.10\text { mm}$$  
  $$y_{\text{large}}=(0.75 \text{ mm}-(0.500 \text{ mm})/2)\frac{19\text{ mm}}{0.75 \text{ mm}}=12.667\text { mm}$$

These calculated heights provided a basis for determining the optimal placement of the outlet channels. To maximize the efficiency of particle separation, the widths of the outlet ports were optimized by positioning them at the midpoint between the two predicted heights. This ensures that any particles deviating slightly from their expected streamline still enter the correct channel.

In addition, the outlet design was adjusted to provide sufficient clearance around each particle’s expected trajectory, allowing for minor fluctuations in flow behavior while maintaining proper sorting. The buffer solution outlets, which are mirrored on the opposite side, were positioned to ensure that misdirected particles are less likely to cross over into unintended channels.

The figure below illustrates a schematic representation of the broad section, depicting the locations of $$y_{\text{small}}$$ and $$y_{\text{large}}$$ along with the corresponding outlet channels. Note that the buffer solution outlets are not shown in this figure for clarity.



<p align="center">
  <img width="600" src="/assets/img/section_view.png">
</p>


**Flow Rate Uniformity and Streamline Stability:** Maintaining equal flow rates at both outlets was crucial to ensure the accuracy of the particle separation. Any imbalance in outlet flow rates could disrupt the streamline positions, causing particles to deviate from their expected trajectories. Unequal flow distribution could also introduce undesired recirculation zones or velocity gradients, leading to streamline instability and potential particle mixing. For example if streamlines deviate the larger particle could be pulled upward into the smaller particle outlet. To prevent these issues and preserve the intended separation mechanism, the following design modifications were implemented.    
1. Balancing Hydraulic Resistance Through Outlet Length-to-Width Ratio
  Since the two outlet channels had different widths, their lengths were adjusted to balance hydraulic resistance. Without this adjustment, the wider channel would have lower resistance, causing a disproportionate flow split. By increasing the length-to-width ratio of the wider outlet, additional resistance was introduced, ensuring that both outlets received an equal share of the total flow. This ratio was determined using Hagen-Poiseuille flow approximations, accounting for both channel width and length to equalize resistance across the two outlets. The equation describes laminar flow through a long, straight, and rigid microchannel and is given by:  

  $$
  R = \frac{12\mu L}{w h^3} \left( 1 - 0.63 \frac{h}{w} \right)
  $$
  
  where:  
  - \( R \) is the hydraulic resistance,  
  - \( \mu \) is the dynamic viscosity of the fluid,  
  - \( L \) is the channel length,  
  - \( w \) is the channel width,  
  - \( h \) is the channel height.  
  
  Since the two outlet channels had different widths (\( w_1 \) and \( w_2 \)), their lengths (\( L_1 \) and \( L_2 \)) were adjusted to balance resistance, ensuring equal volumetric flow rates. The resistance ratio was set equal to the desired flow rate ratio:
  
  $$
  \frac{R_1}{R_2} = \frac{Q_2}{Q_1} = 1
  $$
  
  Substituting the Hagen-Poiseuille equation:
  
  $$
  \frac{L_1}{w_1 h^3} \left( 1 - 0.63 \frac{h}{w_1} \right) = \frac{L_2}{w_2 h^3} \left( 1 - 0.63 \frac{h}{w_2} \right)
  $$
  
  Since both outlets had the same height \( h \), the equation simplifies to:
  
  $$
  \frac{L_1}{w_1} \left( 1 - 0.63 \frac{h}{w_1} \right) = \frac{L_2}{w_2} \left( 1 - 0.63 \frac{h}{w_2} \right)
  $$
  
  By solving for \( L_1 \) and \( L_2 \), the lengths were adjusted to ensure equal resistance and maintain uniform flow distribution.

### **Impact on Flow Stability**  
By balancing resistance, the design prevented uneven flow splitting, which could otherwise cause deviations in streamline trajectories. Ensuring equal outlet flow rates reduced disturbances in the pinch flow fractionation process, improving separation accuracy and preventing eddy formation at the outlet.

  
  
2. Trapezoidal Channel Geometry for Barb Integration
  A gradual tapering of the channels was used to accommodate barbed fittings at the outlet. The tapering ensured a seamless transition from the broader outlet region to a narrower connection point, preventing any contractions that could cause flow separation or vortex formation since the barb outlet (given as 1 mm diameter was larger than the beggining outlet widths). The taper was used to allow sufficient space for the barbs while maintaining a controlled narrowing to minimize sudden pressure changes.
  
3. Adjustment of Inlet Flow Rates to Maintain Constant Velocity
  To ensure a stable laminar flow profile, the flow rates of the inlets were controlled using two syringe pumps. The device's two inlet streams—one carrying the particle-laden fluid and another containing only buffer solution—needed to be properly balanced these to maintain a consistent velocity across the pinched segment, ensuring that particles aligned predictably along streamlines. The flow rate of the buffer solution inlet was higher relative to the particle-laden inlet, effectively compressing the particle stream into a narrow region. By tuning this ratio, the velocity profile remained uniform while minimizing shear-induced disturbances.


<img src="/assets/img/Outlets_calibrated.png" width="800px" />

**Future Improvements Based on Testing:**
* 
* 
* 




## CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a43ec6ba2c8022d8a4?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>


## References
[^1]: O'grady, B. J., Geuy, M. D., Kim, H., Balotin, K. M., Allchin, E. R., Florian, D. C., Bute, N. N., Scott, T. E., Lowen, G. B., Fricker, C. M., Fitzgerald, M. L., Guelcher, S. A., Wikswo, J. P., & Bellan, L. M. E. S. (2021). Lab on a Chip . https://doi.org/10.1039/d1lc00744k
[^2]: Sajeesh, P., Kumar, A., & Sen, Á. A. K. (2013). Particle separation and sorting in microfluidic devices: a review. https://doi.org/10.1007/s10404-013-1291-9
[^3]: Venzac, B., Deng, S., Mahmoud, Z., Lenferink, A., Costa, F. A., Bray, C., Otto, C., & Rolando, S. (2021). PDMS curing inhibition on 3D-printed molds: Why? Also, how to avoid it? https://doi.org/10.1021/acs.analchem.0c04944
[^4]: Yamada, M., Nakashima, M., & Seki, M. (2004). Pinched flow fractionation: Continuous size separation of particles utilizing a laminar flow profile in a pinched microchannel. https://doi.org/10.1021/ac049863r

