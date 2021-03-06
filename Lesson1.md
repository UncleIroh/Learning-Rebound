# Lesson 1 - The physics of generating initial conditions for orbits
## Lesson 1 Video
[![Alt text](/L1.png)](https://www.youtube.com/watch?v=6MvrhPKIt6s&feature=youtu.be)So let's start with the math of generaing orbits.
## The Physics
We start with a few givens the mass of each body (M1,M2), the eccentricity of the orbit (e), and the semi-major axis (a). Using these we calculate q1 and q2 which are M1/M2 and M2/M1 respectively. We use these to calculate initial conditions when both planets are on the x-axis and one has a positive y velocity and the other has a negative because the math is the simplest.

Here's how that would look in python:
```python
# Constants
G = 39.43163873354829472 #I'll explain why this isn't 6.67e-11 later
M1 = 1
M2 = 10
q1 = M1/M2
q2 = M2/M1
a=5
e=0 #Circular Orbit
# Generation Initial Conditions
RadiusOfM1 = (1.0-e)*a/(1.0+q1)
VelocityOfM1 = (G*(M1+M2)/a)**.5 * (((1.0+e)/(1.0-e)))**.5 / (1.0+q1)
RadiusOfM2 = (1.0-e)*a/(1.0+q2)
VelocityOfM2 = (G*(M1+M2)/a)**.5 * (((1.0+e)/(1.0-e)))**.5 / (1.0+q2)
```


So now we have our initial conditions for a system that looks like this:

![2bodyimage](https://raw.githubusercontent.com/UncleIroh/Learning-Rebound/master/2Body%20copy.png)

[Continue to Lesson 2](/Lesson2.md)
