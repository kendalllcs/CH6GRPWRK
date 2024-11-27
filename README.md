# SVM Digit Classification with PCA and Cross-Validation

## Members

- **Kendall Lawson** / [lawsonk22@students.ecu.edu](mailto:lawsonk22@students.ecu.edu)
- **Landon Brown** / [brownlan22@students.ecu.edu](mailto:brownlan22@students.ecu.edu)

## Overview

This project focuses on classifying handwritten digits using Support Vector Machines (SVM) with different kernel functions. We compared the performance of linear, radial basis function (RBF), and polynomial kernels. Principal Component Analysis (PCA) was applied to reduce data dimensionality while retaining 80% of the variance. After applying PCA, we used 5-fold cross-validation to evaluate the final accuracy of each model. Kernel parameters were tuned using the `RandomizedSearchCV` method.

## Cross-Validation Scores and Best Parameters

### Linear Kernel

- **Best C**: `78.38`
- **Mean Accuracy**: `95.12%`
- **Standard Deviation**: `1.20%`

### RBF Kernel

- **Best C**: `85.29`
- **Best gamma**: `0.0082`
- **Mean Accuracy**: `98.45%`
- **Standard Deviation**: `0.75%`

### Polynomial Kernel

- **Best C**: `65.47`
- **Best degree**: `3`
- **Mean Accuracy**: `96.78%`
- **Standard Deviation**: `1.10%`

## Best Performing Model

The best performing model is the **RBF Kernel SVM** with a Mean Accuracy of **98.45%**.

## Detailed Results Comparison

- **Linear Kernel**:
  - The linear kernel performed well with a high accuracy, indicating that the data is somewhat linearly separable after PCA.
  - Best parameter `C` was found to be `78.38` through hyperparameter tuning.

- **RBF Kernel**:
  - The RBF kernel outperformed the other kernels, suggesting that it can handle the non-linear relationships in the data effectively.
  - Best parameters were `C = 85.29` and `gamma = 0.0082`.

- **Polynomial Kernel**:
  - The polynomial kernel showed competitive performance, especially with a degree of `3`.
  - Best parameters were `C = 65.47` and `degree = 3`.

## Conclusion

After comparing the performance of different SVM kernels, we found that the **RBF Kernel** provided the highest mean accuracy with the lowest standard deviation, making it the best performing model for this classification task. The use of PCA effectively reduced the dimensionality of the data while retaining essential information, which contributed to the efficiency of the models.
