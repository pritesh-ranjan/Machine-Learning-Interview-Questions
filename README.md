
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
A *confusion matrix* is a table often used to understand the performance of a machine learning classification algorithm on a test set where we have the correct values. It not only tells us how many records the algorithm predicted correctly but breaks the performance into four sections:
 - True positive- Algorithm predicted say 'Yes' and actual value is 'Yes'
 - True negative- Algorithm predicted 'No' and actual values is 'No'
 - False positive- 'Yes' was predicted, but actual value was 'No'
 - False positive- 'No' was predicted but actual value was 'Yes'

Use cases:
1. A false positive in a drug test can result in jail for an innocent person.
2. A false negative in a covid-19 test can lead to an infected person remaining untreated and spreading the disease.

![image of a confusion matrix](resources/confusion_matrix.jpg?raw=true)

 
## Q 3 . Explain Decision trees in brief. 

**Answer**
*Decision trees* belong to a family of supervised machine learning algorithms. One can use decision trees on both classification and regression problems. 
A decision tree uses the training data to learn rules to predict the target variable. It builds the model in the form of a tree structure with a root node at its top, followed by child nodes and leaf nodes at the bottom. Gini impurity is a metric to find the best predictor for the target variable, which becomes the root. The subsequent child nodes are determined similarly. The leaf nodes decide the classification of the model.
A decision tree classifier breaks the dataset into smaller and smaller subsets and creates the tree from the top (also called root node) by asking simple decision-based questions. 
![image of a decision trees](resources/decision_trees.png?raw=true)

## Q 4 . Define overfitting and underfitting. 

**Answer**
*Overfitting*- A model is said to overfit when it performs well on the training set but poorly on the test/dev set. An overfit model has learned the dataset in so many details that it starts absorbing its noise and randomness too. So, the model considers this noise as a vital concept to predict the target variable. One way to prevent overfitting is to penalize parameters that lead to overfitting.<br>
*Underfitting*- When a model is performing poorly on both training and test data, it is called underfitting. An underfit model is unable to grasp the underlying trends that are needed to make correct predictions. It performs poorly even on previously seen data. One way to avoid underfitting is to increase the complexity of the model.

## Q 5 . Define bias and variance?

**Answer**
*Bias*: It's the difference between the predicted value and the actual (known) value of the test set. Thus, we can also call it an error of the model. Bias occurs due to certain assumptions it makes while training on the data. High bias leads to underfitting and poor performance on training data.<br>
*Variance*:  When the model learns from the randomness and noise of the training data, it is called variance. A model with high variance has a very complex fit on the training data and performs poorly on unseen data but well on the training data. This phenomenon is also known as overfitting. Another way to look at variance is the inconsistency of the model predictions. 

## Q 6 . What is bias-variance tradeoff?

**Answer**
If our model is too simple and has fewer parameters, it can high bias and low variance. Then again, if a model is complex and has too many parameters, it's likely to have high variance and low bias. If one tries to decrease the bias, it increases its variance and vice-versa. This relationship between bias and variance is called the bias-variance tradeoff.

## Q 7 . How can we avoid overfitting?

**Answer**
If our model performs better on the training data and poorly on the test/unseen data, it is a sign of overfitting. Some popular techniques for avoiding overfitting are:
 - Cross-validation
 - Increase training data
 - Reducing model complexity by reducing parameters (say decreasing the number of splits, etc in a decision tree)
 - Early stopping
 -  Regularization

## Q 8 . How do you handle/impute missing data?

**Answer**
Often our dataset has some rows where the values are either missing (null/NaN/None or blank) or unreliable data. We should handle these before trying to train a model:

 - Replace with a mean/median of the feature in question. Sometimes we can also use the mean of a specific group. For example, in a column of salary, we can replace it with the average salary within that post/skillset instead of the whole column.
 - Replace with the most common (mode) value.
 - Replace with zero or another constant based on expert knowledge of the field. For example, in a column of the number of reviews, we can replace it with zero if it is missing. The intuition is that if a product has missing data in the 'number of reviews' column, it is likely to have never been reviewed.
 - We can also use sklearn's KNNImputer to impute missing values.

## Q 9 . Explain the difference between K nearest neighbours and K means clustering??

**Answer**
|**KNN**|**K-Means**  |
|--|--|
| It is a supervised classification/regression algorithm. | It is an unsupervised clustering algorithm. |
| Predicts the class, etc by combining the class of ***k*** nearest data points. | Tries to find groups of similar datapoints and creates ***k*** such clusters.|

## Q 10 . What is normalization? When do you need it?

**Answer**
_Data normalization_ is a technique often used during the data preparation phase of building a machine learning model. We use it to shift the values of some features in a dataset into the same scale so that our model understands the importance of these features and does not lean towards certain features just because they have larger values.

It is usually required when features have different ranges or units (of measurement).

For example, we have a dataset where _Age_ and _Salary_ are two features. Now the age ranges from 18 to 55, whereas the Salary ranges from 20,000 to 5,00,000. We can see the difference in values and ranges in the two features. Our model is likely to be more affected by the Salary feature because it has larger values. But this does not necessarily mean that one is more important than the other. Once we normalize these features and bring them to the same scale, the model's prediction accuracy is likely to improve.

## Q 11 . What is meant by the phrase “Curse of Dimensionality”.

**Answer**
We need features to predict our target variable. The phrase _Curse of Dimensionality_ refers to the increase in error when our dataset has too many features.
Theoretically, more dimensions allow for more information, but this rarely helps, as it adds unwanted noise. Machine learning algorithms are harder to train on data with high dimensions and often result in low accuracy and high running time.
To avoid this, we should use dimensionality reduction techniques like feature selection using *PCA* (principal component analysis).

## Q 12 . Define feature selection. What algorithm or techniques are generally used to perform feature selection.

**Answer**
While building a machine learning model, it’s quite rare that all features are needed. The process by which we reduce the number of input features is called _feature selection_. It not only reduces noise in the data but also reduces the computational cost of developing the model.

Some popular feature selection methods:
-   Principal component analysis
-   Filtering features with high correlation (like Pearson correlation) to the target variable
-   Feature importance with respect to the target variable
-   Wrapper methods like Forward feature selection and Backward elimination

## Q 13 . What is One-hot encoding?

**Answer**
