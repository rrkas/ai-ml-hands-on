# Confusion matrix

https://en.wikipedia.org/wiki/Confusion_matrix

![Confusion matrix](../../Images/Confusion%20matrix.webp)

In the field of machine learning and specifically the problem of statistical classification, a confusion matrix, also known as error matrix, is a specific table layout that allows visualization of the performance of an algorithm, typically a supervised learning one; in unsupervised learning it is usually called a matching matrix.

## Formulas

General
- `P = FN + TP`
- `N = FP + TN`

1. Sensitivity, Recall, Hit Rate, or True Positive Rate (TPR)
    > `TPR`  
    > `= TP / P`  
    > `= TP / (TP + FN)`  
    > `= 1 - FNR`

1. Specificity, Selectivity or True Negative Rate (TNR)
    > `TNR`  
    > `= TN / N`  
    > `= TN / (TN + FP)`  
    > `= 1 - FPR`

1. Precision or Positive Predictive Value (PPV)
    > `PPV`  
    > `= TP / (TP + FP)`  
    > `= 1 - FDR`

1. Negative Predictive Value (NPV)
    > `NPV`  
    > `= TN / (TN + FN)`  
    > `= 1 - FOR`

1. Miss Rate or False Negative Rate (FNR)
    > `FNR`  
    > `= FN / P`  
    > `= FN / (FN + TP)`  
    > `= 1 - TPR`

1. Fall-Out or False Positive Rate (FPR)
    > `FPR`  
    > `= FP / N`  
    > `= FP / (FP + TN)`  
    > `= 1 - TNR`

1. False Discovery Rate (FDR)
    > `FDR`  
    > `= FP / (FP + TP)`  
    > `= 1 - PPV`

1. False Omission Rate (FOR)
    > `FOR`  
    > `= FN / (FN + TN)`  
    > `= 1 - NPV`

1. Positive Likelihood Ratio (LR+)
    > `LR+ = TPR / FPR`

1. Negative Likelihood Ratio (LR-)
    > `LR- = FNR / TNR`

1. Prevalence Threshold (PT)
    > `PT = sqrt(FPR) / (sqrt(TPR) + sqrt(FPR))`

1. Threat Score (TS) or Critical Success Index (CSI)
    > `TS = CSI = TP / (TP + FN + FP)`

1. F1-Score
    > `F1 `  
    > `= (2 * PPV * TPR) / (PPV + TPR)`
    > `= 2TP / (2TP + FP + FN)`