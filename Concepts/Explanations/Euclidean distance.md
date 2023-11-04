# Euclidean distance

https://en.wikipedia.org/wiki/Euclidean_distance


- In mathematics, the Euclidean distance between two points in Euclidean space is the length of a line segment between the two points. 

- It can be calculated from the Cartesian coordinates of the points using the Pythagorean theorem, therefore occasionally being called the Pythagorean distance.

```python
# https://www.geeksforgeeks.org/python-math-dist-method/

import math 

# Two dimensional Point 
P = [3, 7]
Q = [-5, -9]

eDistance = math.dist(P, Q) 
print(eDistance)


# Three-dimensional point 
P = [3, 6, 9] 
Q = [1, 0, -2] 

eDistance = math.dist(P, Q) 
print(eDistance) 
```
