Unit: kg-mm-ms-kN-GPa

Geometry:
Wall: 4N shell, size:200*200, mesh density:100*100 center: (0,0,0)
Ball: Sphere Solid, radius: 15, mesh density:20 center: (0,0,30)

Name part: Wall-wall Ball-ball

Material:
Wall: MAT018 (power law plasticity)
RO:2.685E-06 E:69 PR:0.33 K:0.0974 N:0.33587 EPSF:0.4876

Ball: rigid MAT020
RO:7.8E-06 E:200 PR:0.3

Boundary Condition:Fixed constraints are applied to the four edges of the wall.

Initia Condition: 
Velocity: -30, along Z direction

Element Formulation:
Wall: Shell, thickness 0.1
Ball: Solid

Contact: Automatic surface to surface
master surface: wall, slave surface: ball;
Static coefficient of friction:0.2, Dynamic coefficient of friction:0.1, 

Output Control:
Endtime:10
Data: Binary_D3Plot, time interval between outputs:0.1
