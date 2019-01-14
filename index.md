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

## How Can Splines Be Utilized in the Context of Robotics?

We can first look at ways for robots to travel between between two points.  There are a quite of few methods that exist for robots to travel between points.  A simple approach is to use a sequence of straight lines and turns that the robot travels on.  To go accurately to the points with the straight lines and turns, the robot can slow down as it reaches the desired end point using a PID controller (which was actually my project last year).  This is a viable approach in many cases for traveling to a point with a robot.

However, when a high speed is used with these traditional methods, the robot typically falters due to many limitations ranging from effeciency losses, the higher acceleration causing the wheels to slip, and outside forces like the force of friction.

A proposed solution to this problem would to create a motion profile for the robot based off of its physical constraints.  This ramps up and ramps down the speed of the robot; it makes the robot follow a trapezoidal profile which is pictured below.  

However, this is only some of the solution to the problem, and alone, it even exacerbates the issue that we were trying to solve in making the robot faster; this is because a full acceleration and deceleration cycle is needed for every movment of the robot.  A way to combat this problem is by introducing splines.  With splines, the translation of the robot in the x and y direction is taken care of, 


## Math


## Conclusion


## Reflection

