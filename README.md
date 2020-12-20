# Machine Learning Interview Questions

I am preparing for data science and ML jobs and I would like to share this with everyone. Here are a list of question and answers that I have collected/prepared which can be very helpful while preparing for interviews.

# Basics

Questions related to traditional machine learning and basics o data science.

## Q 1. What are the differences between supervised and unsupervised machine learning?

**Answer**
|**Supervised ML**|**Unsupervised ML**|
|--|--|
| Requires labelled training data |Requires unlabelled training data |
|This means we know the correct answer to a record data and tries to predict an answer based on what it learned from training data.| The correct answer is not known and it is up to the algorithm tries to find structure/pattern in the data.|
|Types: Classification, Regression|Clustering, Association rule learning|

## Q 2 . What is a confusion matrix?

**Answer**
A confusion matrix is a table that is often used to understand the preformance of a machine learning classification algorithm on a test set where we have the correct values. It not only tells us how many records the algorithm predicted correctly, but breaks the preformance into four sections:
 - True positive- Cases predicted say 'Yes' and actual value is 'Yes'
 - True negative- Cases predicted 'No' and actual values is 'No'
 - False positive- 'Yes' was predicted, but actual value was 'No'
 - False positive- 'No' was predicted but actual value was 'Yes'

Use cases:
1. A false positive in a drug test can result in jail for an innocent person
2. A false negative in a covid-19 test can lead to an infected person remaining untreated and spreading the disease.

 
## Q 3 . Explain Decision trees. 

**Answer**
