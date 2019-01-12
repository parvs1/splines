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

We can first look at ways for robots to travel between between two points.  There are a quite of few methods that exist for robots to travel between points.  A simple approach is to use a sequence of straight lines and turns that the robot travels on.  This is a viable approach in a few cases 


### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/psdev1/splines/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
