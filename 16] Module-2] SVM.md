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

# Non-Linear SVM -
- A normal Support Vector Machine (SVM) works well when data can be separated using a straight line (2D) or a plane (3D).
- Sometimes data looks like this:

             Blue
          Blue   Blue
      
            Red
         Red   Red

- No straight line can separate them. Linear SVM fails.
- **The Problem with Transformation:**
- Suppose we have: 1000 features and we transform them to: 10,000 features
- This requires:

      Huge memory
      Huge computation
      Slow training
## Kernel Trick
- The Kernel Trick allows SVM to work in higher dimensions without actually creating those dimensions.
- Instead of explicitly calculating φ(x), SVM directly computes K(xi,xj), called the Kernel Function.

**Kernel Function:**

        K(x,y) = φ(x) · φ(y)
        
        Where:
        
        x = first data point
        y = second data point
        φ = transformation function

- Kernel computes the inner product in higher-dimensional space.

# Types of Kernel -
## 1. Linear Kernel?
- The Linear Kernel is the simplest kernel used in SVM.
- It does not transform data into a higher-dimensional space.
- Instead, it calculates the similarity between two points using their dot product.

      K(x,z)=x⋅z
      
      where:
      
      x = first data point
      z = second data point
      x⋅z = dot product

      For two vectors:
      x = (x₁, x₂, ..., xₙ)
      z = (z₁, z₂, ..., zₙ)
      
      Dot Product:
      x · z = x₁z₁ + x₂z₂ + ... + xₙzₙ
      
## 2.Polynomial Kernel-
- Polynomial Kernel is a kernel function that allows SVM to learn non-linear relationships between features.
- Instead of separating data with a straight line, it creates a curved decision boundary.
- Polynomial Kernel implicitly maps data into a higher-dimensional feature space without actually creating the new features.      

        K(x,z) = (x · z + c)^d
        
        where:
            x = first data point
            z = second data point
            c = constant term
            d = degree of polynomial    
              
- **Dot Product (x⋅z):** ### measures how similar two vectors are.

      For:
      x = (x₁, x₂)
      z = (z₁, z₂)
      Dot Product: x · z = x₁z₁ + x₂z₂

- Imagine two arrows: 

      Same direction → large positive dot product
      Opposite direction → negative dot product
      Perpendicular → zero

- **Constant c:** 

        Common Values:
        c = 0 --> Only higher-order polynomial terms.
        c = 1 --> Includes lower-order terms and bias. Most commonly used.
        
- **Degree d:**
- d determines the complexity of the decision boundary
- d=1 behaves like a linear model.
-  Decision boundary: Straight line.
- d=2 Quadratic relationship.
- Decision boundary: Curved (parabolic).
- d=3 gives a cubic boundary.
- Higher values of d create more complex decision boundaries but may lead to overfitting.      


## RBF (Radial Basis Function) Kernel -
- RBF (Radial Basis Function) Kernel, also called the Gaussian Kernel, is the most popular and widely used kernel in SVM.
- It is used when the data is not linearly separable and the relationship between features is complex.

        K(x,z) = e^(-γ||x-z||²)

          The result is always between: 0<K(x,z)≤1
          Value close to 1 → points are very similar.
          Value close to 0 → points are very different.
                  
        Where:
          x = first data point
          z = second data point
          γ (gamma) = controls how quickly similarity decreases with distance
          ||x-z||² = squared Euclidean distance between x and z
          ||x - z||² = (x₁ - z₁)² + (x₂ - z₂)² + ... + (xₙ - zₙ)²
          e = Euler's number (≈ 2.718)
          
 ## 4. Sigmoid Kernel
- Sigmoid Kernel is a non-linear kernel used in SVM that behaves similarly to the activation function used in neural networks.
- It transforms the similarity between two data points using the hyperbolic tangent (tanh) function.

      K(x,z) = tanh(α(x · z) + c)
      
      Where:
      
      - x = first data point
      - z = second data point
      - x · z = dot product between x and z
      - α (alpha) = slope parameter
      - c = constant (bias term)
      - tanh = hyperbolic tangent function       
- tanh function has an S-shaped curve similar to the sigmoid activation function used in neural networks.

     Output range: −1≤tanh(x)≤1


