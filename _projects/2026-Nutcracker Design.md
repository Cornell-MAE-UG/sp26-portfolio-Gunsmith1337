---
layout: project
title: Nutcracker Design
description: Basic nutcracker design problem.
technologies: [Microsoft Paint]
image: /assets/images/pretty-nutcracker.jpg
---
In 2026, I was tasked with designing a nutcracker capable of breaking open a macadamia nut using a human's grip strength. The goal was to determine the dimensions of the nutcracker and simple geometry was advised. Through some basic research, I came up with the following input values for this problem:  
Maximum load withstood by a macademia nut $F_{nut} = 222.18$ kg (Schrauf and Visalberghi 421)  
Diameter of a macadamia nut $d_{nut} = 16$ mm (World Macadamia Organisation)  
Human grip strength $F_{grip} = 40$ kg (Massy-Westropp 3)  
&nbsp;&nbsp;&nbsp;&nbsp;note: This value was rounded down to 40kg despite most age ranges having an average above 40kg.  
  
My plan for solving this problem was to isolate the top half of the nutcracker as its own free body diagram.   
Then, I would identify the distance between the hinge joint, $A$, and the contact point, $B$, between the nut and the nutcracker as $L_1$ and also identify the distance between $B$ and the point of applied force, $C$, as $L_2$.  
Setting the moment about the hinge joint (point $A$) to equal 0 would allow me to find $L_1$ and $L_2$ as a ratio.  
  
When solving this problem, I initially drew the free body diagram as a triangle:  
<img src="{{ "/assets/images/triangle-nutcracker.jpg" | relative_url }}" width="500">  
However, I realized that the problem could be simplified even further by instead drawing the shape of the nutcracker as an open rectangle:  
<img src="{{ "/assets/images/base-nutcracker-dimensions.jpg" | relative_url }}" width="500">  
This meant that instead of having to rely on triangle geometry when calculating distances and moments, I could just treat the horizontal distance between $A, B,$ and $C$ as the lengths of the moment lever arm, $L_1$ and $L_2$.  
I also realized that the value of L1 would be the radius of a macadamia nut, since maximizing mechanical advantage of the tool would ideally involve minimizing the opposing moment from the macadamia nut and maximizing the moment produced by the applied grip force.

Solving the problem yielded the following calculations:
Assuming that the radius of the average macadamia nut is the maximum L1 (or $L_1 = r_nut = d_nut/2 = 8 mm$),

<img src="{{ "/assets/images/nutcracker-FBD.jpg" | relative_url }}" width="500">  

$\sum{M_A}=F_{nut} * L_1 - F_{grip} * (L_1 + L_2) = 0$  
$F_nut * L_1 = F_{grip} * (L_1 + L_2)$  
$L_2 = \frac{F_{nut} * L_1 - F_{grip} * L_1}{F_{grip}}$  
$L_2 = 36.44mm \approx 36 mm$  
$L_1 + L_2 = 44 mm$  

These calculations are merely theoretical and would need significant adjustment in order to translate directly into a new product. For instance, the actual grip handle would actually require a longer handle beyond the applied force; otherwise, it would be exceedingly difficult to gain a good grip exactly on the outmost of the handle. The squared design also fails to account for any structural weaknesses brought about by having a sharp bend in the nutcracker (stress concentrations near the bend may be significant!). More fundamentally, the nutcracker's squared design prevents it from fully closing, which sacrifices its ability to crack nuts below a certain size in exchange for making the math easier. Nuts may also simply slide out of the nutcracker since no grooves were implemented to hold nuts in place.  
To address these problems, I will first start by rounding off the sharp corner, similar to adding a fillet. Then, I will assume that the nutcracker will be able to withstand any forces applied to it by the nut and grip force, since any further adjustments requires going beyond the scope of analyzing mehcanical advantage. I also added grooves so that the nut does not slide out. Furthermore, I will change the design of the handle to be similar to scissor blades. This will allow the grips to slide past each other beyond their normal limit. Although this solution is not fully ideal if a particularly strong, small nut shows up, that case will simply be an exception that is traded off in order to allow for a squared-off design. This revised design will look something like this:

<img src="{{ "/assets/images/pretty-nutcracker-FBD.jpg" | relative_url }}" width="500">  


  
  
  
Citations:  
Schrauf, C., Huber, L. & Visalberghi, E. Do capuchin monkeys use weight to select hammer tools?. Anim Cogn 11, 413–422 (2008). https://doi.org/10.1007/s10071-007-0131-2

Massy-Westropp, N. M., Gill, T. K., Taylor, A. W., Bohannon, R. W., & Hill, C. L. (2011). Hand Grip Strength: age and gender stratified normative data in a population-based study. BMC research notes, 4, 127. https://doi.org/10.1186/1756-0500-4-127

https://www.worldmacadamia.com/style-guide/
