<Official repository of the Robotek PRIME team from Kazakhstan. It contains all the engineering materials of our self-driven vehicle's model participating in the WRO Future Engineers competition in the season of 2024.>
/*<a link="https://github.com/RobotekPRIME2024/WRO-FE24/tree/main/Models">qqqqqq</a>*/
<We used components from a MINDSTORMS EV3 Core Set + a Pixy2 Camera and some other technic pieces from other sets.

A 3D model of the robot can be found here: https://github.com/RobotekPRIME2024/WRO-FE24/tree/main/Models

The final program/code for our autonomous vehicle can be found here: https://github.com/RobotekPRIME2024/WRO-FE24/tree/main/SRC

Our autonomous vehicle relies on a combination of sensors to execute precise movements, crucial for both obstacle avoidance and the qualification challenges of the competition.

Color Sensor: This sensor is employed to identify turns and determine the driving direction by reading colored lines (orange or blue) on the competition field.

Ultrasonic Sensor: Positioned at the front of the vehicle, the ultrasonic sensor measures the distance between the vehicle and field barriers, ensuring that the vehicle's relative position before and after a turn is continuously known.

Gyro Sensor: The gyro sensor plays a pivotal role in maintaining proper alignment. It detects changes in the vehicle's driving angle, alerting the system to any misalignment or deviation. The implementation of a PID (Proportional-Integral-Derivative) regulator ensures that any deviation from the desired steering angle is continuously corrected, guaranteeing the vehicle's straight and precise trajectory.

The PID regulator operates in a continuous loop throughout the program, ensuring the vehicle remains aligned and on the intended path, supporting its autonomous navigation capabilities.

Pixy2 Camera: A camera is used to detect and differentiate obstacles during the obstacle round. Custom made 3D Print Models for the cover and the case for the camera can be found in the corresponding links.>
