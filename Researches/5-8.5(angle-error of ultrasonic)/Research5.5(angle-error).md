On May 5, we collected data for a graph of error versus angle and studied the conversion from polar to Cartesian coordinates and vice versa, odometry, tactics for zeroing odometry, and determining the position of bars.

Research:
Last year, we reset the robot's position on turns. But if the robot was at an angle, the ultrasonic sensor showed incorrect data. To find the real distance from the robot to the wall, we decided to make a graph of error versus angle. Error refers to the difference between what the sensor outputs and the expected data. We expected that the graph would not depend on the distance from the robot to the wall. We tried to collect this data on April 30, but the distances turned out to be very inaccurate because we measured them with a ruler.

1st test’s error graph at a distance of 10 cm:

1st test’s error graph at a distance of 25 cm:

1st test’s error graph at a distance of 50 cm:

1st test’s error graph at a distance of 100 cm:

The graphs are similar at distances of 50 and 100 cm.

On May 5, we needed to collect data again, but this time more accurate. Plan:
⦁	Make a measuring robot
⦁	Need ultrasonic sensor, gyroscope, EV3 Brick
⦁	The ultrasonic sensor must be placed on a rotating platform with a gyroscope
⦁	Write code
⦁	Write data to a file at the click of a button
⦁	Take measurements
⦁	Smoothly rotate the platform by pressing the button
⦁	Once the ultrasonic sensor starts showing 255, you need to change the distance
⦁	Transfer data from file to table
Code:

Measuring process (robot without wheels):

Final robot for measurements:

As a result of the 2nd tests, we got this graph:

Conclusions:
The graph of error versus angle can be roughly expressed by the function 
y=0.00856x^2-0.0967x+0.345
error=0.345-0.0967angle+0.00856angle^2
error=horisontal_dist/cos(angle*π/180)

2nd test’s error graph at a distance of 9.1 cm:

2nd test’s error graph at a distance of 17.9 cm:

2nd test’s error graph at a distance of 25.5 cm:

2nd test’s error graph at a distance of 33.8 cm:

2nd test’s error graph at a distance of 42 cm:

2nd test’s error graph at a distance of 50 cm:

2nd test’s error graph at a distance of 59 cm:

2nd test’s error graph at a distance of 67 cm:

2nd test’s error graph at a distance of 75 cm:

2nd test’s error graph at a distance of 82.6 cm:

The final results of the research:

length - angle, width - distance, height - error.

We will take this into account when measuring the distance from the robot to the wall, to minimize the difference between what the sensor produces and the expected data. Thanks to this, our robot will more accurately determine its distance to the wall, which will make his drive more stable.