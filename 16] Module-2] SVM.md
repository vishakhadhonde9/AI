# Support Vector Machine (SVM)-
- Support Vector Machine (SVM) is a supervised machine learning algorithm used for: Classification, Regression and Outlier Detection
- It is mainly used for classification problems.
- The goal of SVM is to find the best boundary (hyperplane) that separates different classes with the maximum margin.

## Hyperplane -
- Hyperplane is the decision boundary that separates different classes in a dataset.
- The main goal of SVM is to find the best hyperplane that maximizes the distance (margin) between classes.
- For a 2D dataset:
  
          w₁x₁ + w₂x₂ + b = 0

        Where:
            x = Input features
            w = Weight vector
            b = Bias
## Margin -
- Margin is the distance between the hyperplane and the nearest data points from both classes.
- SVM tries to find the hyperplane with the maximum margin because a larger margin usually leads to better classification and less overfitting.
- Small Margin: The boundary is very close to the points.
- Large Margin: The boundary is farther from both classes. SVM prefers the large-margin hyperplane.

# Types of Support Vector Machine (SVM)
### 1. Linear SVM
- A Linear SVM is used when the data can be separated by a straight line (in 2D), a plane (in 3D), or a hyperplane (in higher dimensions).
- In this case, the classes are linearly separable, meaning a single straight decision boundary can correctly divide the data into different classes.

### 2. Non-Linear SVM
- A Non-Linear SVM is used when the data cannot be separated by a straight line or a simple hyperplane.
- In such cases, SVM uses the Kernel Trick to transform the data into a higher-dimensional space where a linear separation becomes possible.


# Example -






