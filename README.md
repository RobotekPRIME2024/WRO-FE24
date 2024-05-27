***
**Robotek PRIME team's repository for WRO Future Engineers 2024.**
***
<div align=center>
 
![logo](./Images/Robotek.png)

</div>

* [**Mobility management**](#mobility-management)
  * [Motor selection](#motor-selection-and-implementation)
  * [Chassis design](#chassis-design-and-implementation)
* [**Power and sense management**](#power-and-sense-management)
  * [Sensor management](#sensor-management)
  * [Power management](#power-management)
* [**Obstacle management**](#obstacle-management)
  * [Sensor-based obstacle detection](#Sensor-Based-Obstacle-Detection)
  * [Trajectory calibration](#trajectory-calibration)
  * [Program](#Program)
* [**Pictures**](#Pictures)
  * [Team photos](#team-photos)
  * [Vehicle photos](#vehicle-photos)
* [**Performance videos**](#performance-videos)

## Mobility Management

## Motor selection

Comparison of motors:

The large motor runs at 160-170 rpm, with a running torque of 20 Ncm and a stall torque of 40 Ncm (slower, but stronger).

The medium motor runs at 240-250 rpm, with a running torque of 8 Ncm and a stall torque of 12 Ncm (faster, but less powerful).
We use a medium motor for steering and two large motors in the back for driving. The medium motor is lighter and is sufficient for steering, while the larger motors have more power, which helps them be the main driving force of the robot.

## Chassis design

We placed the middle motor for the rudder horizontally, trying to create an ackerman angle, but eventually abandoned this idea. With the help of gears, we increase the number of revolutions of the rear motors by 19% (20/12*20/28). Wheels with a diameter of 62.4 mm also help to increase speed. The speed of our robot is 6.4 m/s (165*20/12*20/28*pi*62.4/100/60). Our robot is rear-wheel drive. This greatly simplifies the design and improves maintainability. We have a differential on the rear axle, which helps reduce the turning radius. 3D models of the robot made in BrickLink Studio 2.0 and SolidWorks here: https://github.com/RobotekPRIME2024/WRO-FE24/tree/main/Models.

# Power and sense management

## Power management

The power for the EV3 Brick and the whole vehicle comes from a rechargeable 10V Lithium Battery. It (with a brick) is placed closer to the front axle than to the rear to ensure good traction of the front wheels when cornering.
Power supply diagrams for each electronic part are here:

[Brick](Schemes/95646c01 Programmable Brick.pdf)

[Battery](Schemes/95656 Rechargeable Battery.pdf)

[Large motor](Schemes/95658 Large Motor.pdf)

[Medium motor](Schemes/99455 Medium Motor.pdf)

[Color sensor](Schemes/95650 Color Sensor.pdf)

[Ultrasonic sensor](Schemes/95652 Ultrasonic sensor.pdf)

[Gyro sensor](Schemes/99380 Gyro sensor.pdf)

[Pixy2](Schemes/Pixy2 LEGO.pdf)

## Sensor management

We use a color sensor to detect and determine the color of lines, a gyroscope to determine the angle of the robot, one ultrasonic sensor in the “obstacle” (clockwise or counterclockwise) or two in the “open” to determine the distance between the robot and the wall. We also use the Pixie Camera to detect and determine the color of road signs. To determine the most accurate distance of the robot from the border, we conducted a study, which you can find here: https://github.com/RobotekPRIME2024/WRO-FE24/tree/main/Researches/5-8.5(angle-error%20of%20ultrasonic). The ultrasonic sensor shows incorrect data if it is located at an angle. On April 8, we made a graph of error versus angle.

# Obstacle management

The final program for the robot and pseudocode is here: https://github.com/RobotekPRIME2024/WRO-FE24/tree/main/SRC

## Pictures
## Team


## Robot
![vehph](./V-photos/Photorealistic/Robot.png)
![photo](./V-photos/Photorealistic/RobotTop.png)
![photo](./V-photos/Photorealistic/RobotBottom.png)
![photo](./V-photos/Photorealistic/RobotFront.png)
![photo](./V-photos/Photorealistic/RobotRear.png)
![photo](./V-photos/Photorealistic/RobotLeft.png)
![photo](./V-photos/Photorealistic/RobotRight.png)

# Performance videos


# Engineering factor

We used components from the MINDSTORMS EV3 Core Set, a Pixy2 camera and some other technic pieces from other sets.
