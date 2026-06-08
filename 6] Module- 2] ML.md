# Machine Learning Systems Are Trained and Used for Prediction -
- Machine Learning (ML) is a branch of Artificial Intelligence that enables computer systems to learn from data and improve their performance without being explicitly programmed for every possible scenario. 
- Instead of relying solely on predefined rules, machine learning systems identify patterns, relationships, and trends within data and use this knowledge to make predictions or decisions when presented with new information.

- The primary objective of machine learning is to develop models that can generalize from historical data and accurately predict outcomes for unseen data. This capability makes machine learning useful in a wide range of applications, including healthcare, finance, transportation, cybersecurity, e-commerce, and scientific research.
- The process of building and using a machine learning system generally involves the following stages:

    Data Collection and Preparation
    Model Training
    Model Evaluation
    Model Optimization
    Prediction and Deployment
    How Machine Learning Systems Are Trained

- Training is the process through which a machine learning model learns patterns and relationships from historical data.

## 1. Data Collection and Preparation
- Data serves as the foundation of every machine learning system. The quality and quantity of data directly affect the performance of the model.

- Data Collection

- Relevant data is gathered from various sources such as:
  Databases
  Sensors
  Websites
  Mobile applications
  Business transactions
  Medical records
  Social media platforms
  Data Preparation
- Raw data often contains errors and inconsistencies. Therefore, it must be prepared before training.
- This process includes:
- Data Cleanin - Removing:

    Duplicate records
    Incorrect values
    Inconsistent information
    Irrelevant data
    Handling Missing Values

- Missing information may be:

    Removed
    Replaced with estimated values
    Filled using statistical techniques
    Data Transformation

- Data may need to be converted into a suitable format for machine learning algorithms.
- Examples include:
   - Converting text into numerical values
   - Scaling numerical features
   - Encoding categorical variables
   - Data Splitting

- The dataset is divided into:
- **Training Dataset**
- Used to teach the model.
- Typically:

    70%–80% of total data.

- **Testing Dataset**
- Used to evaluate the model after training.
- Typically:

    20%–30% of total data.

- This separation ensures that the model is evaluated on data it has never seen before.

## 2. Model Training

- During training, a machine learning algorithm analyzes the training data and attempts to learn underlying patterns and relationships.
- The learning process varies depending on the machine learning approach being used.

### Supervised Learning
- Supervised Learning is a machine learning technique in which the model is trained using labeled data.
- Labeled data means that every training example contains:

    Input data
    Correct output (target value)

- The model learns the relationship between inputs and outputs so that it can predict outputs for new inputs.

#### How Supervised Learning Works
- Step 1] Provide training examples containing:
- Input → Correct Output

- Example:

      House Size	Price
      1000 sq ft	₹30 lakh
      1500 sq ft	₹45 lakh
      2000 sq ft	₹60 lakh

- Step 2] The model makes predictions.
- Step 3] Predictions are compared with actual outputs.
- Step 4] The error is calculated.
- Step 5] The model adjusts its internal parameters to reduce future errors.

- This process continues repeatedly until the model achieves satisfactory accuracy.

- Examples of Supervised Learning
- Email Spam Detection

      Input:
      
      Email text
      
      Output:
      
      Spam or Not Spam
      
      Medical Diagnosis
      
      Input:
      
      Patient symptoms and test results
      
      Output:
      
      Disease prediction
      
      House Price Prediction
      
      Input:
      
      Property characteristics
      
      Output:
      
      Estimated price
      
      Credit Risk Assessment
      
      Input:
      
      Customer financial information
      
      Output:
      
      Low-risk or High-risk borrower

## Types of Supervised Learning
#### Classification
- Predicts categories.
- Examples:

    Spam / Not Spam
    Disease / No Disease
    Fraudulent / Legitimate
    Regression

- Predicts continuous numerical values.

- Examples:

        House prices
        Temperature forecasts
        Sales predictions

## Unsupervised Learning
- Unsupervised Learning is a machine learning approach in which the model is trained using unlabeled data.
- Unlike supervised learning, no correct answers are provided.
- The objective is to discover hidden structures, patterns, and relationships within the data.

### How Unsupervised Learning Works
- Step 1] Provide unlabeled data.
- Step 2] The algorithm analyzes similarities and differences.
- Step 3] The model automatically identifies patterns.
- Step 4] Data is grouped into meaningful categories or clusters.

- Examples of Unsupervised Learning
        Customer Segmentation- Customers are grouped according to:
        
        Age
        Income
        Purchasing behavior
        Market Basket Analysis
        
        Retailers identify products frequently purchased together.
        
        Example:
        
        Customers buying bread often buy milk.
        
        Anomaly Detection
        
        Detecting unusual activities such as:
        
        Credit card fraud
        Network intrusions
        Common Unsupervised Learning Algorithms
        K-Means Clustering
        Hierarchical Clustering
        DBSCAN
        Principal Component Analysis (PCA)

## Reinforcement Learning
- Reinforcement Learning (RL) is a machine learning approach in which an agent learns by interacting with an environment and receiving feedback in the form of rewards or penalties.
- The objective is to maximize long-term rewards through continuous learning.

### Components of Reinforcement Learning
- **Agent-** The learner or decision-maker.
- **Environment-** The world in which the agent operates.
- **Action-** A decision taken by the agent.
- **Reward-** Feedback received after performing an action.
- **Policy-** A strategy that determines which actions should be taken.

### How Reinforcement Learning Works
- The agent observes the environment.
- The agent selects an action.
- The environment responds.
- A reward or penalty is given.
- The agent updates its strategy.
- The process repeats continuously.
- Over time, the agent learns which actions produce the highest rewards.

- Examples of Reinforcement Learning
        Self-Driving Cars
        
        Rewards:
        
        Staying in lane
        Following traffic rules
        
        Penalties:
        
        Collisions
        Dangerous driving
        Robotics
        
        A robot learns:
        
        Walking
        Grasping objects
        Navigation
        Game Playing
        
        AI systems learn games such as:
        
        Chess
        Go
        Video games

## Trial-and-Error Learning
- Trial-and-error learning is a process in which a machine learning system repeatedly attempts different actions and learns from the outcomes.
- Successful actions are rewarded.
- Unsuccessful actions are penalized.
- Over time, the system gradually improves by selecting actions that produce better results.
- Example

        A robot learning to walk:
        
        Initial Attempts
        
        The robot falls frequently.
        
        Learning Phase
        
        Successful movements receive rewards.
        
        Improvement Phase

        The robot begins repeating successful behaviors.
        
        Eventually, the robot learns to walk effectively.

## Model Evaluation
- Model evaluation is the process of assessing how well a trained model performs on unseen data.
- The purpose is to determine whether the model can generalize beyond the training data.
- **Evaluation Process-**
- Step 1] Use testing data.
- Step 2] Generate predictions.
- Step 3] Compare predictions with actual outcomes.
- Step 4] Calculate performance metrics.

## Understanding Error in Machine Learning
- Error refers to the difference between the model's prediction and the actual value.
- It indicates how accurate or inaccurate a prediction is.

        Error Formula
        Error=Actual Value−Predicted Value
        
        Example
        
        Actual House Price = ₹50,00,000
        
        Predicted House Price = ₹48,00,000
        
        Error = ₹2,00,000

- The objective of training is to minimize this error as much as possible.

## How Models Improve Over Time
- Machine learning models improve through an iterative process.
- **Prediction-** The model makes predictions.
- **Error Measurement-** The prediction error is calculated.
- **Parameter Adjustment-** The algorithm modifies internal parameters.
- **Retraining-** The model learns from mistakes.
- **Re-evaluation-** Performance is measured again.
- This cycle continues until acceptable performance is achieved.
- This process is known as optimization.

## How Machine Learning Systems Are Used for Prediction
- Once training and evaluation are complete, the model is deployed into a real-world environment.
- When new data is received:

        The trained model analyzes the input.
        Previously learned patterns are applied.
        A prediction is generated.
        The prediction is delivered to users or systems.

- This process is called Inference.
- Examples include:
    
    Predicting stock prices
    Detecting spam emails
    Forecasting weather
    Diagnosing diseases
    Recommending products
    Identifying fraudulent transactions
