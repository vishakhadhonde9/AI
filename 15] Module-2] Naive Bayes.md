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





