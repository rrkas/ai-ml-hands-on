# K-Nearest Neighbors

https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm

In statistics, the k-nearest neighbors algorithm (k-NN) is a non-parametric supervised learning method first developed by Evelyn Fix and Joseph Hodges in 1951, and later expanded by Thomas Cover. It is used for classification and regression. In both cases, the input consists of the k closest training examples in a data set. The output depends on whether k-NN is used for classification or regression:

- In k-NN classification, the output is a class membership. An object is classified by a plurality vote of its neighbors, with the object being assigned to the class most common among its k nearest neighbors (k is a positive integer, typically small). If k = 1, then the object is simply assigned to the class of that single nearest neighbor.

- In k-NN regression, the output is the property value for the object. This value is the average of the values of k nearest neighbors. If k = 1, then the output is simply assigned to the value of that single nearest neighbor.

k-NN is a type of classification where the function is only approximated locally and all computation is deferred until function evaluation. Since this algorithm relies on distance for classification, if the features represent different physical units or come in vastly different scales then normalizing the training data can improve its accuracy dramatically.

Both for classification and regression, a useful technique can be to assign weights to the contributions of the neighbors, so that the nearer neighbors contribute more to the average than the more distant ones. For example, a common weighting scheme consists in giving each neighbor a weight of 1/d, where d is the distance to the neighbor.

The neighbors are taken from a set of objects for which the class (for k-NN classification) or the object property value (for k-NN regression) is known. This can be thought of as the training set for the algorithm, though no explicit training step is required.

A peculiarity of the k-NN algorithm is that it is sensitive to the local structure of the data.

## Cases

1. Imbalance Data

   - Example:

     - Total 1000 data points
     - 950 data points of one class
     - 50 data points of another class

   - Model will be biased towards the class with more data points

   - Solutions:
     - Under-sampling
       - Take almost equal number of data points from all class, even if it means ignoring extra data points from categories having more data points
       - **Disadvantage:** Losing Data
     - Over-sampling
       - Duplicate lesser data to match bigger data
       - Or, Assign greater weights to lesser data points

1. More number of Classes

   - Number of classes: c
   - Solutions:
     - Probability
     - **One-vs-Rest or (OVR), also called One-vs-All (OVA) strategy**: Convert it into binary classifier by keeping one class as target class and rest all classes as common class
     - One-Hot Encoding
     - Assigning values that makes sense:
       - average of that category
       - rank of the class

1. Time based data splitting

   - data is date-time dependent
   - random splitting may not be the best solution
   - splitting data based on time:
     - data before t - 20 days = train
     - data after t - 20 days = test

1. Data that cannot be converted to vectors

   - Example: Pharmacy data, cannot convert paracetamol into a vector
     - But we can get a similarity metrics among different chemicals and salts and use that data for classification

1. Scaling and column standardization

   - data values of different columns having large difference in min and max
   - model becomes biased towards column dominating the result
   - Example: Col1 = 0-10000, col2 = 0-1
   - Solution: Normalization, Standardization, etc

1. Curse of High Dimensions

   - if n (number of data points/ records) is fixed and we increase the dimension of the data, the performance/ accuracy will decrease
   - Higher dimensions also can lead to over-fitting.
   - Solutions:
     - Use [Cosine Similarity](../../../Concepts/Explanations/Cosine%20similarity.md) instead of [Euclidean Distance](../../../Concepts/Explanations/Euclidean%20distance.md)

1. Bias-Variance Trade-off

   - Higher Bias = under-fitting
   - Higher Variance = over-fitting
   - Generalization error = bias<sup>2</sup> + variance + irreducible error
     - bias error = due to simplifying assumptions
