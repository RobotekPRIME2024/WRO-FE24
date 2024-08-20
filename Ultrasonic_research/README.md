On May 5, we collected data for a graph of error versus angle and studied the conversion from polar to Cartesian coordinates and vice versa, odometry, tactics for zeroing odometry, and determining the position of bars.

<h1> Research: </h1>

Last year, we reset the robot's position on turns. But if the robot was at an angle, the ultrasonic sensor showed incorrect data. To find the real distance from the robot to the wall, we decided to make a graph of error versus angle. Error refers to the difference between what the sensor outputs and the expected data. We expected that the graph would not depend on the distance from the robot to the wall. We tried to collect this data on April 30, but the distances turned out to be very inaccurate because we measured them with a ruler.
<div align=center>

 ![photo](./Images/Research_photos/Explanatory_board.jpg)
 ![photo](./Images/Research_photos/Explanation.jpg)
</div>
1st test’s error graph at a distance of 10 cm:
<div align=center>

 ![photo](./Images/Research_photos/Test1Graph1.png)
</div>
1st test’s error graph at a distance of 25 cm:
<div align=center>

 ![photo](./Images/Research_photos/Test1Graph2.png)
</div>
1st test’s error graph at a distance of 50 cm:
<div align=center>

 ![photo](./Images/Research_photos/Test1Graph2.png)
</div>
1st test’s error graph at a distance of 100 cm:
<div align=center>

 ![photo](./Images/Research_photos/Test1Graph3.png)
</div>
The graphs are similar at distances of 50 and 100 cm.

<h2> 2nd test: </h2>

On May 5, we needed to collect data again, but this time more accurate.

<h3> Plan: </h3>

⦁	Make a measuring robot. Need ultrasonic sensor, gyroscope, EV3 Brick.	The ultrasonic sensor must be placed on a rotating platform with a gyroscope.

⦁	Write code:	Write data to a file at the click of a button.

⦁ Take measurements:	Smoothly rotate the platform by pressing the button.	Once the ultrasonic sensor starts showing 255, you need to change the distance.

⦁	Transfer data from file to table

<h3> [Code:](https://github.com/RobotekPRIME2024/WRO-FE24/blob/main/Ultrasonic_research/Test2Code.ev3) </h3>
<div align=center>

 ![photo](./Images/Research_photos/Program_for_measurements.png)
</div>
Measuring process (robot without wheels):
<div align=center>

 ![photo](./Images/Research_photos/Measurement.jpg)
</div>
Final robot for measurements:
<div align=center>

 ![photo](./Images/Research_photos/Robot_for_measurements.jpg)
</div>
As a result of the 2nd tests, we got this graph:
<div align=center>

 ![photo](./Images/Research_photos/Test2Graph1.png)
</div>
<h2> Conclusions: </h2>
The graph of error versus angle can be roughly expressed by the function 
y=0.00856x^2-0.0967x+0.345

error=0.00856angle^2-0.0967angle+0.345

error=horisontal_dist/cos(angle*π/180)

2nd test’s error graph at a distance of 9.1 cm:
<div align=center>

 ![photo](./Images/Research_photos/Test2Graph2.png)
</div>
2nd test’s error graph at a distance of 17.9 cm:
<div align=center>

 ![photo](./Images/Research_photos/Test2Graph3.png)
</div>
2nd test’s error graph at a distance of 25.5 cm:
<div align=center>

 ![photo](./Images/Research_photos/Test2Graph4.png)
</div>
2nd test’s error graph at a distance of 33.8 cm:
<div align=center>

 ![photo](./Images/Research_photos/Test2Graph5.png)
</div>
2nd test’s error graph at a distance of 42 cm:
<div align=center>

 ![photo](./Images/Research_photos/Test2Graph6.png)
</div>
2nd test’s error graph at a distance of 50 cm:
<div align=center>

 ![photo](./Images/Research_photos/Test2Graph7.png)
</div>
2nd test’s error graph at a distance of 59 cm:
<div align=center>

 ![photo](./Images/Research_photos/Test2Graph8.png)
</div>
2nd test’s error graph at a distance of 67 cm:
<div align=center>

 ![photo](./Images/Research_photos/Test2Graph9.png)
</div>
2nd test’s error graph at a distance of 75 cm:
<div align=center>

 ![photo](./Images/Research_photos/Test2Graph10.png)
</div>
2nd test’s error graph at a distance of 82.6 cm:
<div align=center>

 ![photo](./Images/Research_photos/Test2Graph11.png)
</div>
The final results of the research:
<div align=center>

 ![photo](./Images/Research_photos/Test2Graph12.png)
</div>
length - angle, width - distance, height - error.

We will take this into account when measuring the distance from the robot to the wall, to minimize the difference between what the sensor produces and the expected data. Thanks to this, our robot will more accurately determine its distance to the wall, which will make his drive more stable.
