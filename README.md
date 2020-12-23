# Data Science Interview Questions

 When it comes to a job interview, it is essential to know what questions to expect and how to frame the correct answers.
I am building a list of questions with varying difficulty levels to help you prepare for data science and machine learning job interviews.

# Basics

Questions related to traditional machine learning and basics of data science.

## Q 1. What are the differences between supervised and unsupervised machine learning?

**Answer**
|**Supervised ML**|**Unsupervised ML**|
|--|--|
| Requires labelled training data |Requires unlabelled training data |
|The algorithm tries to predict based on what it learned from training data.| It is up to the algorithm tries to find structure/pattern in the data.|
|Types: Classification, Regression|Clustering, Association rule learning|
|Decision Tree, Naive Bayes, Random Forest| K-Means clustring, Apriori algorithm|

## Q 2 . What is a confusion matrix?

**Answer**
A confusion matrix is a table often used to understand the performance of a machine learning classification algorithm on a test set where we have the correct values. It not only tells us how many records the algorithm predicted correctly but breaks the performance into four sections:
 - True positive- Algorithm predicted say 'Yes' and actual value is 'Yes'
 - True negative- Algorithm predicted 'No' and actual values is 'No'
 - False positive- 'Yes' was predicted, but actual value was 'No'
 - False positive- 'No' was predicted but actual value was 'Yes'

Use cases:
1. A false positive in a drug test can result in jail for an innocent person.
2. A false negative in a covid-19 test can lead to an infected person remaining untreated and spreading the disease.

 
## Q 3 . Explain Decision trees in brief. 

**Answer**
Decision trees belong to a family of supervised machine learning algorithms. One can use decision trees on both classification and regression problems. 
A decision tree uses the training data to learn rules to predict the target variable. It builds the model in the form of a tree structure with a root node at its top, followed by child nodes and leaf nodes at the bottom. Gini impurity is a metric to find the best predictor for the target variable, which becomes the root. The subsequent child nodes are determined similarly. The leaf nodes decide the classification of the model.
A decision tree classifier breaks the dataset into smaller and smaller subsets and creates the tree from the top (also called root node) by asking simple decision-based questions. 

## Q 4 . Define overfitting and underfitting. 

**Answer**
Overfitting- A model is said to overfit when it performs well on the training set but poorly on the test/dev set. An overfit model has learned the dataset in so many details that it starts absorbing its noise and randomness too. So, the model considers this noise as a vital concept to predict the target variable. One way to prevent overfitting is to penalize parameters that lead to overfitting.<br>
Underfitting- When a model is performing poorly on both training and test data, it is called underfitting. An underfit model is unable to grasp the underlying trends that are needed to make correct predictions. It performs poorly even on previously seen data. One way to avoid underfitting is to increase the complexity of the model.
