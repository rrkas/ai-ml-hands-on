# Imputation

https://en.wikipedia.org/wiki/Imputation_(statistics)

- In statistics, imputation is the process of replacing missing data with substituted values. 

- When substituting for a data point, it is known as "unit imputation"; when substituting for a component of a data point, it is known as "item imputation". 

- There are three main problems that missing data causes: 
    - missing data can introduce a substantial amount of bias
    - make the handling and analysis of the data more arduous 
    - create reductions in efficiency

- Because missing data can create problems for analyzing data, imputation is seen as a way to avoid pitfalls involved with listwise deletion of cases that have missing values. 

- That is to say, when one or more values are missing for a case, most statistical packages default to discarding any case that has a missing value, which may introduce bias or affect the representativeness of the results. 

- Imputation preserves all cases by replacing missing data with an estimated value based on other available information. 

- Once all missing values have been imputed, the data set can then be analysed using standard techniques for complete data.

- There have been many theories embraced by scientists to account for missing data but the majority of them introduce bias. 

- A few of the well known attempts to deal with missing data include: 
    - hot deck and cold deck imputation
    - listwise and pairwise deletion
    - mean imputation
    - non-negative matrix factorization
    - regression imputation
    - last observation carried forward
    - stochastic imputation
    - multiple imputation

## Listwise (complete case) deletion

- By far, the most common means of dealing with missing data is listwise deletion (also known as complete case), which is when all cases with a missing value are deleted. 

- If the data are missing completely at random, then listwise deletion does not add any bias, but it does decrease the power of the analysis by decreasing the effective sample size. 

- For example, if 1000 cases are collected but 80 have missing values, the effective sample size after listwise deletion is 920. 

- If the cases are not missing completely at random, then listwise deletion will introduce bias because the sub-sample of cases represented by the missing data are not representative of the original sample (and if the original sample was itself a representative sample of a population, the complete cases are not representative of that population either).

- While listwise deletion is unbiased when the missing data is missing completely at random, this is rarely the case in actuality.

## Hot-deck

- A once-common method of imputation was hot-deck imputation where a missing value was imputed from a randomly selected similar record. 

- The term "hot deck" dates back to the storage of data on punched cards, and indicates that the information donors come from the same dataset as the recipients. 

- The stack of cards was "hot" because it was currently being processed.

## Cold-deck

- Cold-deck imputation, by contrast, selects donors from another dataset. 

- Due to advances in computer power, more sophisticated methods of imputation have generally superseded the original random and sorted hot deck imputation techniques. 

- It is a method of replacing with response values of similar items in past surveys. 

- It is available in surveys that measure time intervals.


## Mean substitution

- Another imputation technique involves replacing any missing value with the mean of that variable for all other cases, which has the benefit of not changing the sample mean for that variable. 

- However, mean imputation attenuates any correlations involving the variable(s) that are imputed. 

- This is because, in cases with imputation, there is guaranteed to be no relationship between the imputed variable and any other measured variables. 

- Thus, mean imputation has some attractive properties for univariate analysis but becomes problematic for multivariate analysis.

## Non-negative matrix factorization

- Non-negative matrix factorization (NMF) can take missing data while minimizing its cost function, rather than treating these missing data as zeros that could introduce biases. 

- This makes it a mathematically proven method for data imputation. 

- NMF can ignore missing data in the cost function, and the impact from missing data can be as small as a second order effect.

## Regression

- Regression imputation has the opposite problem of mean imputation. 

- A regression model is estimated to predict observed values of a variable based on other variables, and that model is then used to impute values in cases where the value of that variable is missing. 

- In other words, available information for complete and incomplete cases is used to predict the value of a specific variable. 

- Fitted values from the regression model are then used to impute the missing values. 

- The problem is that the imputed data do not have an error term included in their estimation, thus the estimates fit perfectly along the regression line without any residual variance. 

- This causes relationships to be over identified and suggest greater precision in the imputed values than is warranted. 

- The regression model predicts the most likely value of missing data but does not supply uncertainty about that value.


## Multiple imputation

In order to deal with the problem of increased noise due to imputation, Rubin (1987) developed a method for averaging the outcomes across multiple imputed data sets to account for this. All multiple imputation methods follow three steps.

1. Imputation -  Similar to single imputation, missing values are imputed. However, the imputed values are drawn m times from a distribution rather than just once. At the end of this step, there should be m completed datasets.

1. Analysis -  Each of the m datasets is analyzed. At the end of this step there should be m analyses.

1. Pooling - The m results are consolidated into one result by calculating the mean, variance, and confidence interval of the variable of concern or by combining simulations from each separate model.

Multiple imputation can be used in cases where the data are missing completely at random, missing at random, and missing not at random, though it can be biased in the latter case. One approach is multiple imputation by chained equations (MICE), also known as "fully conditional specification" and "sequential regression multiple imputation." MICE is designed for missing at random data, though there is simulation evidence to suggest that with a sufficient number of auxiliary variables it can also work on data that are missing not at random. However, MICE can suffer from performance problems when the number of observation is large and the data have complex features, such as nonlinearities and high dimensionality.
