# Manhattan distance

https://simple.wikipedia.org/wiki/Manhattan_distance

- The manhattan distance is a different way of measuring distance. It is named after the grid shape of streets in Manhattan

- This distance can be imagined as the length needed to move between two points in a grid where you can only move up, down, left or right.


```python

def manhattan_distance(x1, x2):
    if len(x1) != len(x2):
        raise Exception("Length mismatch!")

    return sum([abs(x1[i] - x2[i]) for i in range(len(x1))])

# 2-D
A = [1, 2]
B = [4, 5]
dist = manhattan_distance(A, B)

# 3-D
A = [1, 2, 3]
B = [4, 5, 6]
dist = manhattan_distance(A, B)
```

