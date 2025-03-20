---

title: "Syringe Pump"
excerpt: "Syringe pump with adjustable flow rates and compatibility for various syringe types."
header:
  image: /assets/img/render.jpg
  teaser: /assets/img/syringe_real.png
gallery:
  - image_path: assets/img/wiring.png
  - image_path: assets/img/drawing1.png
  - image_path: assets/img/drawing2.png
  - image_path: assets/img/drawing3.png
  - image_path: assets/img/drawing4.png
  - image_path: assets/img/drawing5.png


---

# Purpose & Features of the Syringe Pump Design
The syringe pump is designed to provide precise and controlled delivery of fluids, such as medication or nutrients, which is vital in biomedical, healthcare, and industrial applications. This device uses a stepper motor to turn a lead screw, pushing the syringe plunger forward to deliver fluid in a controlled, consistent manner. The pump accommodates syringes ranging from 5 mL to 20 mL, with adjustable flow rates. Key features include...

* Adjustable syringe sizes (5mL to 20mL)
* Stepper motor-driven lead screw mechanism
* Adjustable syringe stabilizers for precise placement
* LED indicator system for operational status
* Reversible pump for resetting syringes
* Easy-to-use controls for operation, pause, and reversal


# Components
**Off-the-Shelf Parts**

| Part Name                | Description                           | Quantity |
|--------------------------|---------------------------------------|----------|
| Stepper Motor            | Provides motion to drive lead screw   | 1        |
| Arduino Uno              | Microcontroller for control           | 1        |
| LED Lights               | RGB LEDs for status indication        | 3        |
| Push Buttons             | For controlling pump operation       | 2        |
| Limit Switch             | Detects when syringe is fully depressed | 1        |
| Power Supply (AC/DC)     | Converts AC to DC for Arduino and breadboard | 1   |

**3D Printed Parts** 

| Part Name                | Description                           | Quantity |
|--------------------------|---------------------------------------|----------|
| Syringe Holder Base      | Holds syringe in place                | 1        |
| Barrel Stabilizer        | Stabilizes syringe barrel             | 1        |
| Plunger Holder           | Holds syringe plunger during operation | 1        |
| Enclosure Box            | Protective casing for electronics     | 1        |
| Motor Mount              | Secures motor in place               | 1        |



# Operating Instructions
1. Insert a syringe (5 mL or 20 mL) into the holder and secure it using the strap.
2. In the Arduino code, set the syringe size (1 for 20mL, 2 for 5mL) and desired flow rate (mL per minute).
3. Upload the code to the Arduino and power on the pump.
4. Press the "On/Off" button to start the pump, indicated by the green LED.
5. Press the button again to pause the pump (yellow LED).
6. Once the syringe is empty, the red LED will activate. Press the reverse button to reset the pump (purple LED).
7. Once reversed, the pump is ready for another cycle, indicated by the yellow LED.



# Arduino Code
The full Arduino code for controlling the syringe pump can be accessed through my GitHub repository [here](https://github.com/parker-friedli/parker-friedli.github.io/blob/0512d142ed77940a472a36297beb53b25aa8523d/_portfolio/syringe_pump_project_code)



# CAD Model

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a4c1562112373539a7?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>


![](/assets/img/syringe_real.png)
{% include gallery caption="Syringe Pump Project Gallery" %}
