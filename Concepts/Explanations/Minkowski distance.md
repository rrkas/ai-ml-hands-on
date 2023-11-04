# Minkowski distance

https://en.wikipedia.org/wiki/Minkowski_distance


The Minkowski distance or Minkowski metric is a metric in a normed vector space which can be considered as a generalization of both the Euclidean distance and the Manhattan distance.


```python
from math import *
from decimal import Decimal

def p_root(value, root):
    root_value = 1 / float(root)
    return round(Decimal(value) ** Decimal(root_value), 3)


def minkowski_distance(x, y, p_value):
    return p_root(
        sum(pow(abs(a - b), p_value) for a, b in zip(x, y)),
        p_value,
    )


# Driver Code
vector1 = [0, 2, 3, 4]
vector2 = [2, 4, 3, 7]
p = 3
print(minkowski_distance(vector1, vector2, p))
```
