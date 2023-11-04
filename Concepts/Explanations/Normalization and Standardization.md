# Normalization and Standardization

1. https://en.wikipedia.org/wiki/Normalization_(statistics)
1. https://en.wikipedia.org/wiki/Feature_scaling


- In statistics and applications of statistics, normalization can have a range of meanings.

- In the simplest cases, normalization of ratings means adjusting values measured on different scales to a notionally common scale, often prior to averaging. 

- In more complicated cases, normalization may refer to more sophisticated adjustments where the intention is to bring the entire probability distributions of adjusted values into alignment. 

- In the case of normalization of scores in educational assessment, there may be an intention to align distributions to a normal distribution. 

- A different approach to normalization of probability distributions is quantile normalization, where the quantiles of the different measures are brought into alignment.

## Rescaling (min-max normalization)

- Also known as min-max scaling or min-max normalization, rescaling is the simplest method and consists in rescaling the range of features to scale the range in [0, 1] or [−1, 1]. 

- Selecting the target range depends on the nature of the data. 

> `x' = (x - min(x)) / (max(x) - min(x))`

- `min(x)` = minimum value of vector x

- `max(x)` = maximum value of vector x

## Mean normalization

> `x' = (x - avg(x)) / (max(x) - min(x))`

- `avg(x)` = average value of vector x 
    > `avg(x) = sum(x) / len(x)`

- `min(x)` = minimum value of vector x

- `max(x)` = maximum value of vector x

## Standardization (Z-score Normalization)

> `x' = (x - avg(x)) / std(x)`


- `avg(x)` = average value of vector x 
    > `avg(x) = sum(x) / len(x)`

- `std(x)` = standard deviation of vector x
    > `std(x) = sqrt(sum(sqr(x - avg(x))) / len(x))`

## Scaling to unit length

- Another option that is widely used in machine-learning is to scale the components of a feature vector such that the complete vector has length one. 

- This usually means dividing each component by the Euclidean length of the vector.

> `x' = x \ ||x||`
