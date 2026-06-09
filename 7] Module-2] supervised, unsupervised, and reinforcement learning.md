# Comparison Between Supervised, Unsupervised, and Reinforcement Learning

Machine Learning algorithms can be broadly categorized into **Supervised Learning**, **Unsupervised Learning**, and **Reinforcement Learning** based on how they learn from data and receive feedback.

| Feature | Supervised Learning | Unsupervised Learning | Reinforcement Learning |
|----------|-------------------|----------------------|-----------------------|
| **Definition** | Learning from labeled data where the correct output is known. | Learning from unlabeled data to discover hidden patterns and relationships. | Learning by interacting with an environment and receiving rewards or penalties. |
| **Training Data** | Labeled Data | Unlabeled Data | Environment Interactions |
| **Correct Answers Available** | Yes | No | No Direct Answers |
| **Learning Approach** | Learns the mapping between inputs and outputs. | Learns the underlying structure of data. | Learns through trial-and-error. |
| **Feedback Mechanism** | Immediate feedback through error calculation. | No explicit feedback. | Feedback in the form of rewards and penalties. |
| **Objective** | Predict accurate outputs for new data. | Discover hidden patterns and insights. | Maximize cumulative rewards over time. |
| **Human Involvement** | High (requires labeled data). | Low (data does not need labels). | Minimal (focuses on reward design). |
| **Output** | Predicted values or class labels. | Clusters, groups, associations, anomalies. | Optimal actions or policies. |
| **Error Measurement** | Difference between predicted and actual output. | No direct error measurement against known answers. | Measured using reward signals and long-term performance. |
| **Decision Making** | Based on learned examples. | Based on discovered patterns. | Based on learned strategies and experiences. |
| **Data Requirement** | Requires large amounts of labeled data. | Requires large amounts of unlabeled data. | Requires interaction data from the environment. |
| **Learning Process** | Learns from examples provided by a teacher. | Learns independently by finding patterns. | Learns by trying actions and observing outcomes. |
| **Adaptability** | Limited to patterns seen in training data. | Can uncover unknown structures in data. | Continuously improves through experience. |
| **Real-World Examples** | Email spam detection, house price prediction, image classification, medical diagnosis. | Customer segmentation, market basket analysis, anomaly detection, recommendation systems. | Self-driving cars, robotics, game playing, resource optimization. |
| **Common Algorithms** | Linear Regression, Logistic Regression, Decision Trees, Random Forest, SVM, Neural Networks. | K-Means, Hierarchical Clustering, DBSCAN, PCA, Association Rule Learning. | Q-Learning, SARSA, Deep Q Networks (DQN), Policy Gradient Methods. |

* learns through **interaction, rewards, and penalties** to make optimal decisions.
