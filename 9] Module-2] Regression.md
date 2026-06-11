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

# Best Fit Line
- The best fit line is the line with the smallest MSE.
- The algorithm adjusts:
```math
Intercept (b₀)
Slope (b₁)
```
- until the error becomes as small as possible.

---

# Example of linear Regression -
## Problem Statement

Suppose we want to predict a student's marks based on the number of hours they study.

### Training Data

| Hours Studied (x) | Marks (y) |
|------------------|-----------|
| 1 | 30 |
| 2 | 40 |
| 3 | 50 |
| 4 | 60 |
| 5 | 70 |

Where:

- x = Hours Studied (Input Feature)
- y = Marks (Output)

## Step 1: Observe the Pattern

Looking at the data:

| Hours | Marks |
|--------|--------|
| 1 | 30 |
| 2 | 40 |
| 3 | 50 |
| 4 | 60 |
| 5 | 70 |

Notice:

- Hours increase by 1
- Marks increase by 10

This indicates a **linear relationship**.

## Step 2: Find the Equation of the Line

Linear Regression finds an equation of the form:

```math
y = mx + c
```

Where:

- m = Slope of the line
- c = Intercept


### Calculate the Slope (m)

```math
m = \frac{\text{Change in Marks}}{\text{Change in Hours}}
```

Using two points:

```math
m = \frac{40 - 30}{2 - 1}
```

```math
m = \frac{10}{1}
```

```math
m = 10
```

### Calculate the Intercept (c)

Use any point from the dataset.

Take:

```math
x = 1,\quad y = 30
```

Substitute into:

```math
y = mx + c
```

```math
30 = 10(1) + c
```

```math
30 = 10 + c
```

```math
c = 20
```

## Step 3: Final Linear Regression Equation

```math
y = 10x + 20
```

- This is the model learned from the data.



## Step 4: Verify the Equation

For x = 1:

```math
y = 10(1) + 20
```

```math
y = 30
```

✓ Correct

For x = 2:

```math
y = 10(2) + 20
```

```math
y = 40
```

✓ Correct

For x = 3:

```math
y = 10(3) + 20
```

```math
y = 50
```

✓ Correct

The line perfectly fits the training data.

## Step 5: Make a New Prediction

Suppose a student studies for **6 hours**.

Use:

```math
y = 10x + 20
```

Substitute x = 6:

```math
y = 10(6) + 20
```

```math
y = 60 + 20
```

```math
y = 80
```

### Prediction

If a student studies for **6 hours**, the predicted marks are:

```math
80
```

## How the Model Learns

Initially, the model does not know:

```math
m = 10,\quad c = 20
```

It starts with random values.

Example:

```math
y = 5x + 10
```

This produces inaccurate predictions.

The model then:

1. Makes predictions.
2. Calculates errors.
3. Computes MSE (Mean Squared Error).
4. Adjusts m and c.
5. Repeats the process.

Eventually it finds:

```math
y = 10x + 20
```

which gives the minimum error.

---

## Visualization

Training points:

```text
(1,30)
(2,40)
(3,50)
(4,60)
(5,70)
```

Graph:

```text
Marks
70 |                    *
60 |                *
50 |            *
40 |        *
30 |    *
   +-------------------------
      1  2  3  4  5  Hours
```

Linear Regression finds the best-fit straight line through these points.

---

## Real-World Example: House Price Prediction

| House Size (sq ft) | Price ($) |
|-------------------|------------|
| 1000 | 200000 |
| 1200 | 240000 |
| 1500 | 300000 |

Linear Regression learns:

```math
Price = m(Size) + c
```

Using this equation, it can predict the price of a new house based on its size.

---

# Key Takeaway

Linear Regression learns a straight-line equation:

```math
y = mx + c
```

from historical data and uses it to predict continuous values.

### In This Example

- Input = Study Hours
- Output = Marks
- Learned Equation = `y = 10x + 20`
- Prediction for 6 hours = `80 marks`

This is a complete Linear Regression workflow: **Data → Learn Equation → Predict New Values**.







