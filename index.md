## What is a Spline?

* A continuous curve that passes through a set of points
* Piecewise function that is defined by a number of polynomials
* Can have polynomials of differing degrees
* Parametric curve and can be interpolated

## How Can Cubic Splines Splines Be Interpolated?

* In this project, I will specifically be using and talking about cubic splines
* Splines can be split into various subintervals
* For example, the interval [0,2] can be split up into [0,1] and [1,2]
* A cubic function can be calculated for that specific segment and parameterized from the domain [0,1]
* To ensure the curve is always continuous, the derivative and second derivative have to equal each other at the connection points between the subintervals
* The endpoints can either have specific values of the second derivatives it has to equal to, which is a clamped spline
* It could also have the second derivative equal to 0, which is a natural spline

## How Can Splines Be Utilized in the Context of Robotics?

We can first look at ways for robots to travel between between two points.  There are a quite of few methods that exist for robots to travel between points.  A simple approach is to use a sequence of straight lines and turns that the robot travels on.  To go accurately to the points with the straight lines and turns, the robot can slow down as it reaches the desired end point using a PID controller (which was actually my project last year).  This is a viable approach in many cases for traveling to a point with a robot.

However, when a high speed is used with these traditional methods, the robot typically falters due to many limitations ranging from effeciency losses, the higher acceleration causing the wheels to slip, and outside forces like the force of friction.

A proposed solution to this problem would to create a motion profile for the robot based off of its physical constraints.  This ramps up and ramps down the speed of the robot; it makes the robot follow a trapezoidal profile which is pictured below.  

However, this is only some of the solution to the problem, and alone, it even exacerbates the issue that we were trying to solve in making the robot faster; this is because a full acceleration and deceleration cycle is needed for every movment of the robot.  A way to combat this problem is by introducing splines.  With splines, the movment of the robot of the turn and the translational movement can be combined in one manuever.  Also, the curve is smooth, which allows it to accelerate and decelerate without wasting time.  A spline movement is roughly 1.5 times faster than traditional approaches, so the benefits are clear. 


## Math
Here is an example calculation of interpolating a spline.  Here, we interpolate a cubic spline that passes through three points: (1, 4), (2, 1), and (3,4).  It is easiest to set the domain for each segment from [0,1] as the interpolation becomes much easier.  In this case, there will be 2 segments, one from [1,2] and another one from [2,3].  The value, the deriviative, and the second derivative have to equal between the connection points of the two segments, which ensures continuity and that the curve is smooth.  We can get a few equations from this process and use a matrix solver to find the values of the coefficients.


This is great, but for a robot with a motion profile, the spline should be parameterized for a function of time.  So, there will be two equations, one for the x position on the field and the other one for the y position.  So, I

## Conclusion


## Reflection

