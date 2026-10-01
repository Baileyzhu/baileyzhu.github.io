---
title: "Print-in-Place Pliers"
excerpt: "Multi-material print-in-place pliers for small objects."
header:
  image: assets/img/3D-printing-pliers.JPG
  teaser: assets/img/plier_final.jpeg
gallery:
  - image_path: assets/img/plier_CAD_Assembly.png
  - image_path: assets/img/plier_final.png
  - image_path: assets/img/plier.gif
   

# Introduction
 
After plenty of experience 3D printing single-material models, the next step for me was to try out multi-material printing. A perk   of using multiple materials in the same model is a pairing of flexible and stiff material, which unlocks an abundance of new         possibilities for my prints. I was most interested in movement, specifically how multi-material methods could be used to make        functional moving parts. The result: a set of pliers, functional straight from the print bed without need for additional parts.      After all, what better way is there to use a tool (3D printing) than to make another tool (pliers)? 

# Description
 
Print-in-place models allow for parts with multiple moving components to be printed in one print bed. These models can function      without needing extra tools for assembly, like adhesives or fasteners. Their function relies on precise, intentional designs of       joints. In fact, print-in-place methods can be used to create mechanical joints, specifically [vertical pin-and-socket hinges,       horizontal teardrop hinges, and articulated chain links and captive ball-and-socket joints(https://www.sovol3d.com/blogs/news/print-in-place-3d-printing-how-to-design-hinges-joints-and-moving-parts-that-actually-work?srsltid=AU7gw4WqwzSwKkkUHQEHuxtbEeprpD8fcKD_IyCgyrs_g_O89oKhagXK). The combination of flexible and stiff materials can also be    utilized to create movement in the model. Certain pairings can optimize multi-material printing, such as pairings chosen to minimize cross-material bonding like PETG and PLA.  In the case of the pliers, I chose to use PLA for my stiff elements and TPU for my flexible elements. 

# Design and Iterative Process 

The specifications for my pliers were precision and usability: my goal was to be able to pick up small objects efficiently. This was tested by a 30 second trial where I would use my pliers to pick up through-hole resistors. Therefore, I decided to start small.

<p align="center">
  <img src="assets/img/through_hole_resistor.png" width="500">
</p>

I aimed to make the pliers as small as possible—increasing precision, of course, but also maximizing portability and aesthetics. I based my design off an example shown in class: 

<p align="center">
  <img src="assets/img/plier_example.jpg" width="500">
</p>

The handle (in white) is made of PLA and is the stiff component. The ‘teeth’ of the pliers are made of PLU, and the flexible material along with the thin arcs filling the shape of each triangle allow for curved bending of the shape. When the PLA ‘lever’ (the white circle) is pulled, the deformation of the TPU pulls the tips of the triangles together, allowing the teeth to clamp shut. The issue encountered with this example, which is quite large (iPad case under plier for reference), is the teeth of the pliers were flimsy and would misalign vertically, meaning the teeth often wouldn’t meet nicely in the middle and a strong grip couldn’t be achieved. However, I liked the aesthetics of the design, and wondered if the imprecision could be remedied with a shorter length and a wider thickness. 

<table>
  <tr>
    <td><img src="images/plier_sketch_grabber.png" width="300"></td>
    <td><img src="iimages/plier_sketch_handle.png" width="300"></td>
    <td><img src="iimages/plier_sketch_lever.png" width="300"></td>
  </tr>
</table>

I used the lab’s single-extrusion Voron 3D printers to create my piece, so the TPU and PLA parts were printed separately and assembled via hand-pressing the mechanical joints together. My first iteration was essentially a test to see if they would function as intended and check tolerances, because I couldn’t design the joints in Fusion360 to demonstrate the flexing. Though the joints didn’t fit because I didn’t leave enough clearance, I was able to determine that the mechanism worked as intended. 

<p align="center">
  <img src="images/plier_first_try.jpeg" width="500">
</p>

In the second and final iteration, I adjusted the fit of the TPU joints to better fit the PLA joints. Additionally, I added 50% infill in SuperSlicer to help prevent the TPU from sagging from bridging and make the grabbers more sturdy. The result was an efficient and precise plier. 

<p align="center">
  <img src="images/plier_final.jpeg" width="500">
</p>

<p align="center">
  <img src="images/plier.gif" width="500">
</p>

# Specifications
  The jaws are approximately 50 mm long, and can open up to 5.5 mm. The entire plier is roughly 100 mm long when resting.

| Setting | PLA | TPU |
|---|---:|---:|
| Print width (mm) | 0.6 | 0.6 |
| Bed temperature (°C) | 65 | 60 |
| Print temperature (°C) | 215 | 240 |
| Infill (%) | 20 | 50 |
| Infill pattern | Gyroid | Gyroid |



# Interactive CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b602811edf85497d2772f0b?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

{% include gallery caption="Plier Gallery" %}

