<div align=center>
 Robotek PRIME team's repository for WRO Future Engineers 2024
 
 Members: Dastan Musrepov, Vagis Disembayev

 ![logo](./Images/Robotek.png)
</div>

***

# Contents

* [**Mobility management**](#mobility-management)
  * [Motor selection](#motor-selection)
  * [Chassis design](#chassis-design)
* [**Power and sense management**](#power-and-sense-management)
  * [Sensor management](#sensor-management)
  * [Power management](#power-management)
* [**Engineering factor**](#engineering-factor)
* [**Obstacle management**](#obstacle-management)
* [**Pictures**](#pictures)
  * [Team photos](#team-photos)
  * [Robot photos](#robot-photos)
* [**Performance video**](#performance-video)

***

# Mobility Management

## Motor selection

Comparison of motors:
The large motor runs at 160-170 rpm, with a running torque of 20 Ncm and a stall torque of 40 Ncm (slower, but stronger).
The medium motor runs at 240-250 rpm, with a running torque of 8 Ncm and a stall torque of 12 Ncm (faster, but less powerful).
We use a medium motor for steering and two medium motors in the back for driving. We use medium motors because they are lighter, faster and have enough torque.
<!The medium motor is lighter and is sufficient for steering, while the larger motors have more power, which helps them be the main driving force of the robot.>

## Chassis design

![photo](./Images/Ackermann%20steering%20geometry.jpg)

We placed the steering motor horizontally to save space and make an simple approximation of Ackerman angle ([photo above](https://github.com/RobotekPRIME2024/WRO-FE24/tree/main/Images/Ackermann%20steering%20geometry.jpg)). The length of our robot is 16 cm, which allows us to park perpendicularly. With the help of gears, we increase the number of revolutions of the rear motors by 19%. Wheels with a diameter of 62.4 mm also help to increase speed. The maximum speed of our robot is 1 m/s. Our robot is rear-wheel drive. This greatly simplifies the design and improves maintainability. We have a differential on the rear axle, which helps reduce the turning radius. By using Ackermann steering geometry, we increase the accuracy of odometry, prevent wheel spin, and reduce the turning radius. We 3D models of the robot made in BrickLink Studio 2.0 and SolidWorks are located in the [Models](https://github.com/RobotekPRIME2024/WRO-FE24/tree/main/Models) folder. Building instructions located in the [Instruction](https://github.com/RobotekPRIME2024/WRO-FE24/tree/main/Instruction.pdf) file.

***

# Power and sense management

## Power management

The power for the EV3 Brick and the whole vehicle comes from a rechargeable 10V Lithium Battery. It (with a brick) is placed closer to the front axle than to the rear to ensure good traction of the front wheels when cornering.
Links to power schemes for each electronic part:

[EV3 P-Brick](https://github.com/RobotekPRIME2024/WRO-FE24/blob/main/Schemes/95646c01%20Programmable%20brick.pdf)

[Battery](https://github.com/RobotekPRIME2024/WRO-FE24/blob/main/Schemes/95656%20Rechargeable%20battery.pdf)

[Medium motor](https://github.com/RobotekPRIME2024/WRO-FE24/blob/main/Schemes/99455%20Medium%20motor.pdf)

[Color Sensor](https://github.com/RobotekPRIME2024/WRO-FE24/blob/main/Schemes/95650%20Color%20sensor.pdf)

[Ultrasonic Sensor](schemes/ultrasonic-sensor.pdf)

[Gyro Sensor](https://github.com/RobotekPRIME2024/WRO-FE24/blob/main/Schemes/99380%20Gyro%20sensor.pdf)

[Pixy2](https://github.com/RobotekPRIME2024/WRO-FE24/blob/main/Schemes/Pixy2.pdf)

## Sensor management

We use a color sensor to detect and determine the color of lines, a gyroscope to determine the angle of the robot, ultrasonic sensor to determine the distance between from the robot to the wall, thereby updating the odometry on turns - when seeing a line. We also use the Pixy2 Camera to detect and determine the color of road signs on the first 'obstacle' lap. To determine the most accurate distance of the robot from the border, we conducted a research, which you can find in the [Researches](https://github.com/RobotekPRIME2024/WRO-FE24/tree/main/Researches/5-8.5(angle-error%20of%20ultrasonic)). The ultrasonic sensor shows incorrect data if it is located at an angle. On April 8, we made a graph of error versus angle.

***

# Engineering factor

We used components from the MINDSTORMS EV3 Core Set, a Pixy2 camera and some other technic pieces from other sets.

***

# Obstacle management

First you need to configure Pixy2 to detect green and red road signs. Then you need to find the trajectory of the road sign using the Pixy2 camera. To do this, we launch the robot so that it goes around the road sign and records its coordinates using the Pixy2 camera. He takes the center of the road sign as the coordinates. After that, we transfer the data into a table and use the built-in tools in Google Sheets to find the equation. The robot tries to adhere to this trajectory. If the object is red, then x of function are multiplied by 1, and if the object is green, then x of function are multiplied by -1 (inverse function).

![photo](./Images/Trajectory%20of%20road%20sign.jpg)

Compared to the robot from the regional stage, we only drive with the held of the Pixy2 Camera on the first lap, during which we record the coordinates of the points along which it will drive to avoid road signs on the remaining laps. We use local ododmetry to determine the position of the robot. To calculate the robot's x, we multiply the distance traveled by the cosine of the robot's angle, and to calculate the robot's y we multiply the distance traveled by the sine of the robot's angle. We calculate the distance traveled by multiplying the encoder angle by a coefficient equal to 15.43 dergrees to cm. We reset robot's odometry on turns, without using ultrasonic.

The final robot program with pseudocode is located in the [Source](https://github.com/RobotekPRIME2024/WRO-FE24/tree/main/Source).

***

# Pictures
## Team photos
![photo](./Images/Team%20Photos/Official.jpg)
![photo](./Images/Team%20Photos/Funny.jpg)

## Robot photos
![photo](./Images/Robot%20photos/Photorealistic/Front-left.png)
![photo](./Images/Robot%20photos/Photorealistic/Top.png)
![photo](./Images/Robot%20photos/Photorealistic/Bottom.png)
![photo](./Images/Robot%20photos/Photorealistic/Front.png)
![photo](./Images/Robot%20photos/Photorealistic/Rear.png)
![photo](./Images/Robot%20photos/Photorealistic/Left.png)
![photo](./Images/Robot%20photos/Photorealistic/Right.png)

# Performance video

Here is the link to [qualification round demonstration](https://youtu.be/wz5MyXlZ5nA).
