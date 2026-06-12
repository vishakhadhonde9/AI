# Ensemble Learning -
- Ensemble Learning is a machine learning technique where we combine multiple models (called weak learners) to build a strong model with better accuracy and stability.
- Instead of relying on one model, we use a group of models and aggregate their predictions.
## Classification (Ensemble Learning):

       ŷ = majority_vote(h₁(x), h₂(x), ..., h_T(x))

## Regression (Ensemble Learning):

      ŷ = (1/T) * Σ (t = 1 to T) h_t(x)


# Types of Ensemble Learning -
## 1. Bagging (Bootstrap Aggregation)
- Bagging is an ensemble learning technique in machine learning where multiple models are trained on different bootstrap samples (random samples with replacement) of the training data, and their predictions are combined to produce a final output.

# Random Forest -
- Random Forest is a supervised machine learning algorithm used for classification and regression tasks.
- A Random Forest is an ensemble of many decision trees, where:
   - Each tree is trained on a random sample of data
   - Each tree uses a random subset of features
   - Final output is combined from all trees.
 
# Working -
## 1. Bootstrap Sampling (Bagging)
- From original dataset:
   - Random samples are taken with replacement
   - Each sample trains one decision tree
## 2. Random Feature Selection
- At each split, Only a random subset of features is considered
- This increases diversity among trees.

## 3. Build Multiple Trees
- Each tree is grown independently.
- All trees learn different patterns.
## 4. Prediction
#### Classification (Majority Voting)-
- Final output is decided by majority vote of all trees:

      y^ = majority_vote(h1(x), h2(x), ..., hT(x))

#### Regression:
- Final output = Average of all trees

    y^ = (1/T) * Σ(ht(x)) , for t = 1 to T

    y^ = (1/T) * (h1(x) + h2(x) + ... + hT(x))







