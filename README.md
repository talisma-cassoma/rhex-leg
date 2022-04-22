# rhex-leg
  GÖKHAN ORAL: ``The most important mechanical part of the robot is the leg``

## OBJECTIF :
create a mecanism for simulate rhex's leg.
- rhex uses pc104 board to control the six legs, here i'm just interessed on simulating the legs mechanism, using the low level inteface of Rhexlib, this is why i'm using arduino on my experiences
    

## Mechaninal design 
even if this repo tittle's rhex legs, the references used here for rhex mechecanicals parts where based on X-RHex 
<p align="center">
  <img src="images/XRHEX.png" width="33.3%"/> <img src="images/View_of_internal_electronics.png" width="35%"/>
</p>

### leg design and motor selection 
<p align="center">
<img src="images/Exploded_view_of_the_motor_mounting_assembly.png" width="50%"/>
</p>

the X-RHex version uses high-torque, flat “pancake-style” brushless motors offered by Maxon Motors3.
<p align="center">
<img src="images/A_disassembled_view_of_the_brushless_motor.png" width="50%"/>
</p>

### Control Electronics

this version uses also a Advanced Motion Controls (AMC) DZRLATE-20L080 motor controller. The DZRALTE-020L080 digital servo drive is designed to drive brushed and brushless servomotors, stepper motors, and AC induction motors from a compact form factor ideal for embedded applications. This motor controller comes preprogrammed with a variety of control modes that allow for quick testing of control strategies with limited custom code. These control schemes include position and velocity PID-F, current, voltage, rate limiter, current limiter, PVT 

## A closed loop PID controller

### PD controller in position
### pure current loop
### position-around-velocity controller