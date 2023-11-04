# Hamming distance

https://en.wikipedia.org/wiki/Hamming_distance

- In information theory, the Hamming distance between two strings of equal length is the number of positions at which the corresponding symbols are different. 

- In other words, it measures the minimum number of substitutions required to change one string into the other, or the minimum number of errors that could have transformed one string into the other.

```python
def hamming_distance(string1: str, string2: str) -> int:
    """Return the Hamming distance between two strings."""

    if len(string1) != len(string2):
        raise ValueError("Strings must be of equal length.")

    dist_counter = 0
    for n in range(len(string1)):
        if string1[n] != string2[n]:
            dist_counter += 1

    return dist_counter
```

