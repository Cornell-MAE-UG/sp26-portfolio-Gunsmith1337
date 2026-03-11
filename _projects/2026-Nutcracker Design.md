---
layout: project
title: Nutcracker Design
description: Overoptimized, bare minimum nutcracker.
technologies: [Microsoft Paint]
image: /assets/images/nutcracker.jpg
---

Inline math: $a^2 + b^2 = c^2$

Display math:

$$
\int_0^1 x^2 dx
$$

In 2026, I was tasked with designing a nutcracker capable of breaking open a macadamia nut using a human's grip strength. The goal was to determine the dimensions of the nutcracker and simple geometry was advised. Through some basic research, I came up with the following input values for this problem:  
$$
\text{Maximum load withstood by a macademia nut} F_nut = 222.18kg \text{(Schrauf and Visalberghi 421)}  
\text{Diameter of a macadamia nut} d_nut = 16mm \text{(World Macadamia Organisation)}  
\text{Human grip strength} F_grip = 40kg \text{(Massy-Westropp 3)}  
    \text{note: This value was rounded down to 40kg despite most age ranges having an average above 40kg.}  
$$

My plan for solving this problem was to isolate the top half of the nutcracker as its own free body diagram.   Then, I would identify the distance between the hinge joint, $A$, and the contact point, $B$, between the nut and the nutcracker as L1, while the distance between B and the point of applied force, $C$, as L2.  
Setting the moment about the hinge joint (point $A$) to equal 0 would allow me to find L1 and L2 as a ratio.

When solving this problem, I initially drew the free body diagram as a triangle.  
However, I realized that the problem could be simplified even further by instead drawing the shape of the nutcracker as an open rectangle. This meant that instead of having to rely on triangle geometry when calculating distances and moments, I could just treat the horizontal distance between A, B, and C as the lengths of the moment lever arm.  
I also realized that the value of L1 would be the radius of a macadamia nut, since maximizing mechanical advantage of the tool would ideally involve minimizing the opposing moment from the macadamia nut and maximizing the moment produced by the applied grip force.

Solving the problem yielded the following calculations:
Assuming that the radius of the average macadamia nut is the maximum L1 (or $L_1 = r_nut = d_nut/2 = 8 mm$),
$$
\sum{M_A}=F_nut * L_1 - F_grip * (L_1 + L_2) = 0
F_nut * L_1 = F_grip * (L_1 + L_2)
L_2 = \frac{F_nut * L_1 - F_grip * L_1}{F_grip}
L_2 = 36.44mm \approx 36 mm
L_1 + L_2 = 44 mm
$$


Citations:  
Schrauf, C., Huber, L. & Visalberghi, E. Do capuchin monkeys use weight to select hammer tools?. Anim Cogn 11, 413–422 (2008). https://doi.org/10.1007/s10071-007-0131-2

Massy-Westropp, N. M., Gill, T. K., Taylor, A. W., Bohannon, R. W., & Hill, C. L. (2011). Hand Grip Strength: age and gender stratified normative data in a population-based study. BMC research notes, 4, 127. https://doi.org/10.1186/1756-0500-4-127

https://www.worldmacadamia.com/style-guide/
