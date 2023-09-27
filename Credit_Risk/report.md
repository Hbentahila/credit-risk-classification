# Credit Risk Classification

## Overview of the Analysis

 - The purpose of this analysis is to build, train and evaluate a model able to identify the creditworthiness of borrowers and whether a loan is healthy or high risk for defaulting based on a dataset of historical lending activity from a peer-to-peer lending services company.
 - The dataset includes a couple of features that will help us build our credit risk classification model: loan size,	interest rate, borrower income,	debt to income,	num of accounts, derogatory marks, total debt.
 - The variable we are trying to predict ('y') is "loan_staus" and it should be noted that in the dataset: a value of 0 in the “loan_status” column means that the loan is healthy and a value of 1 means that the loan has a high risk of defaulting.
 - The dataset is imbalanced and counts 75036 healthy loans and 2500 high risk loans
 - To build our model, we went through the following stages :
     1. Separate the labels set (y) from our features (X)
     2. Split the Data into Training and Testing Sets
     4. Decide on a machine learning algorithm
     5. Fit/train the model using the original data and the resampled data and save the predictions for each model
     6. Evaluate each model using the balanced accuracy score, the confusion matric and the classification report (Precision, Recall, F1-score)
     7. Compare both models
 - To build our model, we are using the supervised machine learning algorithm "LogisticRegression". We will be predicting with Logistic Regression trained on original data as well as using resampled training data to adress class imbalance.

## Results

1. Machine Learning Model 1: Logistic Regression with the original data

   * Balanced accuracy score : 0.95
   * Precision: '0': 1.00 / '1': 0.85
   * Recall: '0': 0.99 / '1': 0.91
   * F1-score: '0': 1.00 / '1': 0.88

2. Machine Learning Model 2: Logistic Regression witht the resampled data

   * Balanced accuracy score : 0.99
   * Precision: '0': 1.00 / '1': 0.84
   * Recall: '0': 0.99 / '1': 0.99
   * F1-score: '0': 1.00 / '1': 0.91

## Summary

In predicting healthy loans ('0'), Model 1 has performed exceptionally well, achieving high precision (100%), recall(99%), and f1-scores (100%). However, for high risk loans ('1'), the results are less satisfying but the model was still able to perform well with a precision of 85%, recall of 91%, and f1-score of 88%. Also, it is important to note that even though both classes are imbalanced, we were able to get a balanced accuracy score of 95%, which confirms that the model is performing very well in terms of correctly classifying healthy and high-rsik loans but this score can be improved.

Similarly, in predicting healthy loans ('0'), Model 2 has performed exceptionally well, achieving high precision (100%), recall(99%), and f1-scores (100%). Also, for high risk loans ('1'), the results remained less satisfying compared to the first model, with a decreased precision (84%), an improved recall (99%) and f1-score (91%). However, the balanced accuracy score got improved (95% Vs 99%). Overall, we can observe an improved accuracy in detecting high risk loans with this model.

Both models have a high precision and are great at predicting healthy loans, however, they are both less accurate when it comes to predicting high risk loans. This is a good indicator as there is less risk in classifying a healthy loan as high risk rather than classifying a high risk loan as healthy. 

We may want to consider Model 2, even though the precision remained almost the same, it improved the recall as well as the balanced accuracy score. Also we may want to try other algorithms and see if we can get better results in predicting high risk loans.