---
title: "Syringe Pump"
excerpt: "Syringe pump designed to eject fluid at fixed rate."
header:
  image: /assets/img/Syringe_Pump_IRL.jpg
  teaser: /assets/img/syringe_pump_rendering.png
gallery:
  - image_path: assets/img/syringe_pump_rendering.png
  - image_path: assets/img/Syringe_pump_wiring_diagram.png
  - image_path: assets/img/syringe_pump_petgpartiers.png
   
---

# Features

* **Regulated Fluid Delivery** 0.1 to 5 mL/min. The syringe pump converts the rotational motion of a stepper motor into linear displacement via a lead screw, ensuring highly accurate and consistent fluid transfer.
* **Versatile Syringe Compatibility** 10 mL and 20 mL. The physical carriage and end supports are designed to securely clamp standard 10 mL and 20 mL syringes, while the software can be configured to accommodate other diameters.
* **Protective 3D-Printed Enclosure** A custom-designed enclosure houses all electronic components, leaving minimal openings only for the buttons and LED to protect the wiring from accidental fluid exposure and ensure user safety.

# Off-the-Shelf Parts

| Component | Description |
| :--- | :--- |
| Stepper Motor & Driver | Drives the lead screw mechanism; utilizes microstepping (set to 8) for smooth motion. |
| Arduino & Breadboard | Commands the system using the AccelStepper library. |
| Lead Screw & Linear Rods | 8mm pitch lead screw and press-fit linear bearings for stable carriage travel. |
| Power Supply | 120V power supply to operate the system. |
| Aluminum Extrusion | Serves as the foundational rail for the linear motion assembly. |
| Electronic Controls | Latching button, limit switch, potentiometer, and two jog buttons. |
| RGB LED | Indicates system status (green, yellow, red). |
| Fasteners & Wiring | Assorted screws, bolts, heat shrink tubing, and jumper wires. |

# 3D Printed Parts

| Part Name | Material | Function |
| :--- | :--- | :--- |
| Motor-Mounting-Plate | ABS | Secures the motor; printed in ABS due to heat contact. |
| Carriage | PLA | Travels along the lead screw to push the plunger. |
| Syringe-End-Support | PLA | Clamps the 10 mL or 20 mL syringe securely in place. |
| End-Support | PLA | Stabilizes the far end of the linear rods and lead screw. |
| Enclosure Assembly | PLA | Includes the main box, lid, shelf insert, and v-slot holder to house and protect electronics. |

# Arduino Code
https://github.com/Baileyzhu/Syringe_Pump_ArduinoCode/blob/main/Syringe_Pump_ArduinoCode.ino

# CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b60281115024c78543613a4?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

# Operation Instructions
  1. Plug the power supply into a 120V outlet to power the system.  
  1. Press the latching button to activate the pump; the front panel LED will turn green to indicate it is running.  
  1. Observe the fluid dispensing, and adjust the flow rate as needed via the potentiometer or by modifying the code variables.  
  1. Press the latching button again to pause the pump (indicated by a yellow LED), or wait for the syringe to empty, which will trigger the limit switch and stop the motor automatically (indicated by a red LED).  
  1. Press the latching button once more to turn off the pump, then reset the syringe to repeat the process.  

{% include gallery caption="Syringe Pump Gallery" %}
