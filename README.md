# Quora Question Pair Similarity

[Quora Question Pairs- kaggle](https://www.kaggle.com/competitions/quora-question-pairs/overview)

### **Problem statement**
* Predict if the questions asked in Quora are duplicates of the existing questions. 
* This could be useful to instantly provide answers to questions that have already been answered.

### **Mapping real world problem to ML problem**
* Binary Classification problem: In this case study, we predict whether a pair of questions are duplicates or not.

### **Business objectives**
*   The cost of a mis-classification can be high.
    (Customer disappointment if non-duplicates are classified as duplicates)
*   Provide the probability that a pair of questions can be duplicates so that a custom threshold can be chosen.
*   No-strict latency requirements (can take few seconds)
*   Interpretability is partially important. (Not needed for the Customer)

### **Performance metric**
* Binary Cross entropy
* Binary confusion matrix

### **Overview of the Data set**
- Data in train.csv
- Train.csv contains 5 columns : qid1, qid2, question1, question2, is_duplicate
- Size of Train.csv - 60MB
- Number of rows in Train.csv = 404,290

#### Description of columns:

* qid1 : unique ID of question number 1
* qid2 : unique ID of question number 2
* question1 : Textual content of question1
* question2 : Textual content of question2
* is_duplicate : target variable 
* 0 : Pair of questions are not duplicate
* 1 : Pair of questions are duplicate

**Train-Test Split:** 
    We build train and test by randomly splitting in the ratio of 70:30
