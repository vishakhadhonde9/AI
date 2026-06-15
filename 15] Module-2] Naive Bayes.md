# Naive Bayes Algorithm -
- Naive Bayes is a supervised machine learning classification algorithm based on Bayes' Theorem.
- It is called "Naive" because it assumes that all features are independent of each other, which is often not true in real-world data.
- It is widely used for:
  - Spam Detection
  - Sentiment Analysis
  - Document Classification
  - Medical Diagnosis
  - Recommendation System

# Bayes Theorem
- Naive Bayes is based on Bayes' theorem:

      P(C∣X)= P(X)/P(X∣C)×P(C)


Where:
  
   - P(C∣X) = Posterior Probability 
   - P(X∣C) = Likelihood
   - P(C) = Prior Probability
   - P(X) = Evidence​

- Suppose:

      C = Spam Email
      X = Contains the word "Free"

- Prior Probability P(C) = Probability that an email is spam before seeing any features.
- Likelihood P(X∣C) = Probability of seeing the word "Free" given that the email is spam. e.g.- P(Free∣Spam)
- Evidence P(X) = Probability of seeing the word "Free" in any email. e.g.- P(Free)
- Posterior Probability = Probability that the email is spam if it contains "Free". e.g. - P(Spam∣Free)

# Example-
- Suppose we want to predict whether a person will Play Cricket based on the weather.

| Weather | Windy | Play |
|----------|--------|------|
| Sunny | No | Yes |
| Sunny | Yes | No |
| Rainy | No | Yes |
| Rainy | Yes | No |
| Sunny | No | Yes |

## Step 1: Training Data
- This is the data used to train the model.
- Total Records = 5

| Play | Count |
|------|-------|
| Yes  | 3     |
| No   | 2     |

## Step 2: Calculate Prior Probabilities
- Prior Probability means probability of each class before seeing any feature.
- **Play = Yes**

      P(Yes)= 5/3 = 0.6

- **Play = No**

      P(No)= 5/2 = 0.4
## Step 3: Calculate Likelihood Probabilities
- Suppose we want to predict for:

      Weather = Sunny
      Windy = No

- Calculate feature probabilities for each class.
- **For Play = Yes**

| Weather | Windy |
|----------|--------|
| Sunny | No |
| Rainy | No |
| Sunny | No |

- Total Yes = 3
- Weather = Sunny
        
        P(Sunny∣Yes) = 3/2
        	​
- Windy = No

        P(NoWind∣Yes) = 3/3 = 1
        
- **For Play = No**

| Weather | Windy |
|---------|-------|
| Sunny   | Yes   |
| Rainy   | Yes   |

- Total No = 2

- Weather = Sunny

       P(Sun  ny∣No) = 2/1
  
- Windy = No

      P(NoWind∣No) = 2/0 = 0

## Step 4: Apply Bayes Theorem
- Formula:

      P(C|X) ∝ P(C) × P(X₁|C) × P(X₂|C)

- Calculate for Play = Yes

      P(Yes) × P(Sunny|Yes) × P(NoWind|Yes)
      = 0.6 × (2/3) × 1
      = 0.4

- Calculate for Play = No

      P(No) × P(Sunny|No) × P(NoWind|No)
      = 0.4 × (1/2) × 0
      = 0
## Step 5: Compute Posterior Probabilities

| Class | Score |
|--------|--------|
| Play = Yes | 0.4 |
| Play = No | 0 |

- These scores represent the posterior probabilities (up to a constant factor).

## Step 6: Choose Highest Probability Class
- Compare:

    ```text
    Play = Yes → 0.4
    Play = No  → 0
    ```
    Since:
    
    0.4 > 0
    
    Prediction:
    
    ```text
    Play = Yes
    ```








