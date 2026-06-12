# Decision Tree -
- Decision Tree is a supervised machine learning algorithm used for both classification and regression problems.
- It used to make predictions by repeatedly splitting data into smaller groups based on conditions or rules.
- It has a tree-like structure where each node represents a decision, each branch represents the outcome of that decision, and each leaf node represents the final prediction.

# Components of Decision Tree -
## 1. Root Node -
- The topmost node of the tree.
- Represents the entire dataset.
- The first feature is selected here to split the data.

## 2. Internal Node (Decision Node) -
- Represents a condition or test on a feature.
- Used to further split the data into smaller subsets.

## 3. Branch
- Represents the outcome of a decision or test.
- Connects one node to another.

## 4. Leaf Node (Terminal Node)
- The final node of the tree.
- Contains the prediction or decision.
- No further splitting occurs.

# Types of Decision Tree-
## 1. Classification Trees: 
- Used when the target variable is categorical (discrete).
- The tree splits the data to sort instances into distinct classes or categories (e.g., predicting whether an email is "Spam" or "Not Spam").
## 2.Regression Trees: 
- Used when the target variable is continuous (numerical).
- The tree predicts real numbers by splitting the data into regions and averaging the values within those regions (e.g., predicting house prices or temperature)

# Mathematical Concepts -
## Entropy -
- Entropy is a measure of impurity, uncertainty, or disorder in a dataset.
- In a Decision Tree, entropy helps us determine how mixed the classes are in a dataset.
    - Low Entropy → Data is pure (mostly one class)
    - High Entropy → Data is mixed (many classes)
- The goal of a Decision Tree is to reduce entropy at every split.

        Entropy(S) = -P(Yes)log₂(P(Yes))
                     -P(No)log₂(P(No))

- Entropy = 0, Means all samples belong to one class.
- Entropy = 1, Means data is equally mixed, maximum uncertainty.

## Information Gain -
- Information Gain is the reduction in entropy achieved after splitting a dataset on a feature.
- A Decision Tree chooses the feature with the highest Information Gain because it provides the best separation of classes.

        Information Gain = Entropy(Parent) - Weighted Entropy(Children)

-  Weighted Entropy - is the average entropy of all child nodes, where each entropy is weighted according to the proportion of records in that child node.

        Weighted Entropy =
        (Weight of Child 1 × Entropy of Child 1)
        +
        (Weight of Child 2 × Entropy of Child 2)
        +
        ...
        +
        (Weight of Child n × Entropy of Child n)

## Gini Index -
- Gini Index measures the impurity of a dataset. A lower Gini value indicates a purer node, while a higher Gini value indicates a more mixed node.

      Gini(S) = 1 - Σ(pi²)
      
      Where:
      
      S  = Dataset
      pi = Probability of class i
      n  = Number of classes

# Steps -
- Predict whether a person will buy a laptop (Yes/No) based on their Age, Income, and Student status using a Decision Tree Classification model.

| Age    | Income | Student | Buy Laptop |
|--------|--------|---------|------------|
| Young  | High   | No      | No         |
| Young  | High   | Yes     | No         |
| Middle | High   | No      | Yes        |
| Old    | Medium | No      | Yes        |
| Old    | Low    | Yes     | Yes        |
| Old    | Low    | Yes     | No         |
| Middle | Low    | Yes     | Yes        |
| Young  | Medium | No      | No         |

## Step 1: Calculate Entropy/Impurity of dataset -

- Count Target Classes:

    - Yes = 4  
    - No  = 4  

- Probabilities:

        - P(Yes) = 4/8 = 0.5  
        - P(No)  = 4/8 = 0.5  
        
- Entropy Formula:

        Entropy(S) = -P(Yes)log₂(P(Yes))-P(No)log₂(P(No))
        
        Entropy(S) = -(0.5 × log₂0.5)-(0.5 × log₂0.5)
                   = 0.5 + 0.5
                   = 1
## Step 2: Calculate Entropy of all attribute of Age -
- **Age = Young**   
   
        No
        No
        No
       Entropy = 0

- **Age = Middle**

        Yes
        Yes
       Entropy = 0

- **Age = Old**

            Yes
            Yes
            No
        
          Probabilities: P(Yes)=2/3
                         P(No)=1/3

#### Information Gain for Age

        IG(Age) = 1 - 0.344
                = 0.656       
                  
        Entropy: = -(2/3)log₂(2/3)-(1/3)log₂(1/3)
                 ≈ 0.918
        
## Step 3: Check Feature "Income"
- **Income = High**
  
        No
        No
        Yes
       Entropy: ≈ 0.918

- **Income = Medium**

        Yes
        No
        Entropy:= 1
  
- **Income = Low**

        Yes
        Yes
        No
        Entropy:≈ 0.918
        
        Weighted Entropy = (3/8 × 0.918)+(2/8 × 1)+(3/8 × 0.918)
                         = 0.938

        Information Gain
        IG(Income)= 1 - 0.938 = 0.062

## Step 4: Check Feature "Student"
- **Student = Yes**

        No
        Yes
        No
        Yes
  
        Yes = 2
        No  = 2
        Entropy:= 1

- **Student = No**

        No
        Yes
        Yes
        No
        Yes = 2
        No  = 2
       Entropy:= 1
        
        Weighted Entropy = (4/8 × 1)+(4/8 × 1)
                         = 1
        Information Gain
        IG(Student) = 1 - 1
                    = 0
  
Step 5: Compare Information Gain
Feature	Information Gain
Age	0.656
Income	0.062
Student	0
Best Feature
Age

because it has the highest Information Gain.

So Age becomes the Root Node.

Decision Tree Construction
                    Age
               /      |      \
          Young    Middle     Old
            |         |         |
           No        Yes    Income
                            /    \
                        Medium   Low
                          |        |
                         Yes      Mixed
Predicting a New Record

Suppose:

Age	Income	Student
Middle	High	Yes

Tree Traversal:

Age = Middle
      ↓
     Yes

Prediction:

Buy Laptop = Yes
What Happened Mathematically?
Calculated Parent Entropy = 1.
Computed Information Gain for all 3 features:
Age = 0.656
Income = 0.062
Student = 0
Chose the feature with the highest Information Gain.
Split the dataset using that feature.
Repeated the process for child nodes until leaf nodes were reached.
Final Formula Used

Entropy

Entropy(S) = - Σ Pi log₂(Pi)

Information Gain

IG = Entropy(Parent)
     - Weighted Entropy(Children)

The feature with the maximum Information Gain becomes the next decision node in the tree.
