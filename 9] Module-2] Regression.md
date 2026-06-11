# Linear Regression -
- Linear Regression is one of the simplest and most commonly used supervised machine learning algorithms.
- It is used to predict a continuous numerical value by finding the relationship between input variables (features) and an output variable (target).
- Linear Regression tries to draw the best-fit straight line through the data points so that we can predict future values.
- For example:
   - Predict house price based on house size
   - Predict salary based on years of experience
   - Predict sales based on advertising budget
   - Predict exam marks based on study hours.
- It is called:

    Linear because it assumes a linear relationship between input and output.
    Regression because it predicts a continuous value.

- A linear relationship means that when one variable changes, the other changes at a constant rate.
- The goal is to find the best straight line that represents the relationship between input and output.

## Mathematical Intitution -
- The equation of a straight line is:

      y=mx+c
      y=b0​+b1​x

      Where:
        y = Predicted output --> dependent variable
        x = Input feature --> independent variable
        b₀ = Intercept --> value of y when x = 0.
        - Graphically, it is where the line crosses the y-axis.
        b₁ = Slope (coefficient) --> Shows how much y changes when x increases by 1 unit.
        - Formula:
         Slope=Change in x / Change in y


## Error (Residual)
- The difference between actual and predicted value is called Residual or Error.
- Formula:

        Error=Actual−Predicted


 # Cost Function-
 - Cost Function is a mathematical function that measures how wrong a machine learning model's predictions are.
 - The most common cost function for Linear Regression is Mean Squared Error (MSE).
 - **Cost Function in Linear Regression-**
 - Mean Squared Error (MSE) is a metric used to measure how well a regression model is performing.
 - It tells us how far the predicted values are from the actual values on average.
 - A smaller MSE means the model is making better predictions.

## Mathematical Intitution -
- Suppose for one data point:
- Actual value = `y`
- Predicted value = `ŷ`

         Error (Residual):  = y - ŷ

- Suppose we have `n` observations.

| Observation | Actual (`y_i`) | Predicted (`ŷ_i`) |
|------------|------------|------------|
| 1 | y₁ | ŷ₁ |
| 2 | y₂ | ŷ₂ |
| 3 | y₃ | ŷ₃ |
| ... | ... | ... |
| n | yₙ | ŷₙ |


- Error for the i-th observation:

   ```math
   e_i = y_i - \hat{y}_i
   ```

- **Why We Don't Use Simple Sum of Errors-**
- If we add all errors:

```math
\sum_{i=1}^{n}(y_i-\hat{y}_i)
```
- Positive and negative errors can cancel out.
- Example:

```math
(+5) + (-5) = 0
```
- This incorrectly suggests there is no error.

- **Square Each Error-**
- To avoid cancellation, square every error:

```math
(y_i-\hat{y}_i)^2
```
- Now all errors become positive.

- **Sum All Squared Errors-**
- Add all squared errors:

```math
\sum_{i=1}^{n}(y_i-\hat{y}_i)^2
```

Expanded form:

```math
(y_1-\hat{y}_1)^2 +
(y_2-\hat{y}_2)^2 +
(y_3-\hat{y}_3)^2 +
\cdots +
(y_n-\hat{y}_n)^2
```
- This is called the **Sum of Squared Errors (SSE)**.


- **Take the Average-**
- To make the error independent of dataset size, divide by the number of observations `n`:

```math
\frac{1}{n}
\sum_{i=1}^{n}(y_i-\hat{y}_i)^2
```

---

# Final MSE Formula

```math
MSE =
\frac{1}{n}
\sum_{i=1}^{n}
(y_i-\hat{y}_i)^2
```

Where:

- `n` = Number of observations
- `y_i` = Actual value
- `ŷ_i` = Predicted value
- `(y_i - ŷ_i)` = Error (Residual)

---

