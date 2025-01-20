---
title: "Syringe Pump"
excerpt: "Syringe pump with adjustable flow rates and compatibility for various syringe types."
header:
  image: /assets/img/syringe_render.png
  teaser: /assets/img/syringe_real.png
gallery:
  - image_path: assets/img/drawing1.png
  - image_path: assets/img/wiring.png
  - image_path: assets/img/drawing2.png
   
---

# Purpose & Features of the Syringe Pump Design
The syringe pump is designed to provide precise and controlled delivery of fluids, such as medication or nutrients, which is vital in biomedical, healthcare, and industrial applications. This device uses a stepper motor to turn a lead screw, pushing the syringe plunger forward to deliver fluid in a controlled, consistent manner. The pump accommodates syringes ranging from 5 mL to 20 mL, with adjustable flow rates. Key features include...

* Adjustable syringe sizes (5mL to 20mL)
* Stepper motor-driven lead screw mechanism
* Adjustable syringe stabilizers for precise placement
* LED indicator system for operational status
* Reversible pump for resetting syringes
* Easy-to-use controls for operation, pause, and reversal


# CAD Model
#<iframe src="https://myhub.autodesk360.com/ue2df0af5/shares/public/SH35dfcQT936092f0e437224cd558fdcdc2f?mode=embed" width="800" height="600" #allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

# Operating Instructions
1. Insert a syringe (5 mL or 20 mL) into the holder and secure it using the strap.
2. In the Arduino code, set the syringe size (1 for 20mL, 2 for 5mL) and desired flow rate (mL per minute).
3. Upload the code to the Arduino and power on the pump.
4. Press the "On/Off" button to start the pump, indicated by the green LED.
5. Press the button again to pause the pump (yellow LED).
6. Once the syringe is empty, the red LED will activate. Press the reverse button to reset the pump (purple LED).
7. Once reversed, the pump is ready for another cycle, indicated by the yellow LED.


# Arduino Code
The full Arduino code for controlling the syringe pump can be accessed through my GitHub repository here: 

# Components
* Off-the-Shelf Parts
* 3D Printed Parts
{% include gallery caption="Syringe Pump Project Gallery" %}
