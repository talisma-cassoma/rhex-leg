# rhex-leg

The most important mechanical part of the robot is the leg

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

this version uses also a Advanced Motion Controls (AMC) DZRLATE-20L080 motor controller.  This motor controller comes preprogrammed with a variety of control modes that allow for quick testing of control strategies with limited custom code. These control schemes include position and velocity PID-F, current, voltage, rate limiter, current limiter, PVT 

## A closed loop PID controller

### PD controller in position
### pure current loop
### position-around-velocity controller