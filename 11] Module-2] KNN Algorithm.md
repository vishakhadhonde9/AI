# K-Nearest Neighbors (KNN) Algorithm -
- K-Nearest Neighbors (KNN) is one of the simplest and easiest Machine Learning algorithms.
- It is a Supervised Learning algorithm used for:
  - Classification → Predicting categories/classes.
  - Regression → Predicting numerical values.
- KNN makes predictions based on the similarity between data points.
- KNN predicts the output of a new data point by looking at the K nearest data points in the training dataset.

### Why is it called K-Nearest Neighbors?
- **K-** Represents the number of neighbors considered.
- Example:
   - K = 3 → Consider 3 nearest neighbors.
   - K = 5 → Consider 5 nearest neighbors.
- **Nearest-** Nearest means the data points that are closest to the new data point.
- **Neighbors-** Neighbor means nearby data points.

## KNN Algorithm - Classification -
### Step 1: Choose a Value of K -
- The first step is to decide the number of neighbors (K) that will participate in the prediction.
- K is a positive integer.
- It represents how many nearby data points will be considered.
- The choice of K affects the model's performance.
- If Small K (e.g., K = 1),considers only one nearest neighbor, Sensitive to noise and Can lead to overfitting.
- If Large K (e.g., K = 15),considers many neighbors, produces more stable predictions, reduces the effect of noise, but may ignore local patterns and can lead to underfitting.
- If K is chosen as an odd number such as: K=3, 5, 7, 9
- Odd values are preferred in binary classification problems because they help avoid ties during majority voting.

### Step 2: Calculate Distance Between New Data Point and Training Data -
- After selecting K, calculate how far the new data point is from every training data point.
- The most commonly used distance measure is Euclidean Distance:
- Euclidean Distance Formula:

d(X,Y) = √[ Σ(i=1 to n) (xi - yi)² ]

- Expanded Form

d = √[(x1 - y1)² + (x2 - y2)² + ... + (xn - yn)²]

- Where:
  - xi = Feature value of the new data point
  - yi = Feature value of the training data point
  - n  = Number of features
  - d  = Distance between the two points
 
## Step 3: Sort Distances
- After calculating distances, arrange them from **smallest to largest**.

| Height | Class | Distance |
|----------|---------|----------|
| 160 | Short | 5 |
| 170 | Tall | 5 |
| 150 | Short | 15 |
| 180 | Tall | 15 |

- The closest points appear at the top of the list.

## Step 4: Select the K Nearest Neighbors
- Suppose: K = 3
- Take the first three rows from the sorted list.

| Height | Class | Distance |
|----------|---------|----------|
| 160 | Short | 5 |
| 170 | Tall | 5 |
| 150 | Short | 15 |

- These are the 3 nearest neighbors.

## Step 5: Count the Class Labels

- Now count how many neighbors belong to each class.

| Class | Count |
|---------|---------|
| Short | 2 |
| Tall | 1 |

- The algorithm simply counts the occurrences of each class.

## Step 6: Perform Majority Voting
- Select the class with the highest count.

| Class | Votes |
|---------|---------|
| Short | 2 |
| Tall | 1 |

- Since Short has more votes:
- **Prediction = Short**
- This process is called **Majority Voting**.

## Step 7: Assign the Predicted Class
- The new data point receives the class that won the vote.
### Example
- **New Person Height = 165**
- Nearest Neighbors: 
  - Short
  - Tall
  - Short

- Majority Vote:
  - Short = 2
  - Tall = 1

### Final Prediction -
```text
Predicted Class = Short
```




