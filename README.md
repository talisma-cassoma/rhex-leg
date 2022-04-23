# rhex-leg
  GÖKHAN ORAL: ``The most important mechanical part of the robot is the leg``

## OBJECTIF :
create a mecanism for simulate rhex's leg.
- rhex uses pc104 board to control the six legs, here i'm just interessed on simulating the legs mechanism, using the low level inteface of Rhexlib, this is why i'm using arduino on my experiences
    

## MECHANINAL DESIGN 
even if this repo tittle's rhex legs, the references <br>
used here for rhex mechecanicals parts where based on X-RHex 
<p align="center">
  <img src="images/XRHEX.png" width="33.3%"/> <img src="images/View_of_internal_electronics.png" width="35%"/>
</p>

### LEG DESIGN AND MOTOR SELECTION 
<p align="center">
<img src="images/Exploded_view_of_the_motor_mounting_assembly.png" width="50%"/>
</p>

the X-RHex version uses high-torque, <br>
flat “pancake-style” brushless motors offered by Maxon Motors3.
<p align="center">
<img src="images/A_disassembled_view_of_the_brushless_motor.png" width="50%"/>
</p>

### CONTROL ELECTRONICS

this version uses also a Advanced Motion Controls (AMC) DZRLATE-20L080 motor controller. The DZRALTE-020L080 digital servo drive is designed to drive brushed and brushless servomotors, stepper motors, and AC induction motors from a compact form factor ideal for embedded applications. This motor controller comes preprogrammed with a variety of control modes that allow for quick testing of control strategies with limited custom code. These control schemes include position and velocity PID-F, current, voltage, rate limiter, current limiter, PVT 

While using a COTS controller like this one saves the time and effort needed to develop the various control modes, substantial development time is required to understand and effectively use the slew of control modes provided by a third-party product.

so then, this is what we will explore here, we will explore those methods and undunstand their results by building those solutions with our own code. 

first lets understand how the hardware used for test.

### SETUP THE HARDWARE OF THE PROJET 

lets just built a digital servo drive :)... Nah, i'll be using the Brushless DC Motor controller from<a href="https://github.com/mrkindustries/bldc.git"> Benjamin Vedder.</a>
<p align= "center">
 <img src="http://vedder.se/wp-content/uploads/2015/01/PCB_Front.png" width="70%"/>
</p> 

The software consists of a ChibiOS-project for the STM32F4 and a Qt-program to test and debug the hardware.

### POSITION-AROUND-VELOCITY CONTROLLER
