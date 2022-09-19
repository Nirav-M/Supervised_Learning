# Supervised_Learning_Challenge

  The purpose of this challenge was to develop a machine learning model that produces accurate classification predictions, given an imbalanced dataset. The data we were working with is loan information from a peer to peer lending platform, and the imbalance is that the platform's healthy loans greatly outnumber the risky loans. Using the value_counts function we were able to see that there were 75,036 healthy loans, and 2500 high risk loans. The goal was to correctly sort the healthy loans from the high risk loans. In order to determine whether a loan was healthy or risky, we used the input variables of loan size, interest rate, income, the debt to income ratio, the number of accounts the borrower has, derogatory marks (such as late payments or defaults), and total debt. These variables were used to determine the loan status represented as either a 0 for healthy loans, or a 1 for the high risk loans. 

  The first model we ran simply split the data into train and test categories, then we fit the train data to a logistic regression machine learning model, and predicted the results of the test data. The second model incorporated the RandomOverSampler function to resample the input data and match the number of risky loans to the number of healthy loans. We then fit the oversampled data to the logistic regression model and predicted the loan status of the test data. 
  
## Results 

Precision = True Positives / (True Positives + False Positives)
Recall = True Positives / (True Positives + False Negatives)

Machine Learning Model 1: 
  * Balanced accuracy score: 0.9520479254722232
  * Healthy loans precision score: 1.00
  * Healthy loans recall score: 0.99
  * High risk loans precision score: 0.85
  * High risk loans recall score: 0.91
  
Machine Learning Model 2:
  * Balanced accuracy score: 0.9936781215845847
  * Healthy loans precision score: 1.00
  * Healthy loans recall score: 0.99
  * High risk loans precision score: 0.84
  * High risk loans recall score: 0.99

## Summary

  The second machine learning model that included oversampling of the train data was better at predicting high risk loans. This is shown in the classification report as the precision and recall scores for the healthy loans (0 label) remained the same. However, the recall score for the high risk loans (1 label) improved from 0.91 to 0.99 using the second logistic regression model. Additionally, the precision score for the high risk loans in the second model only dropped from 0.85 to 0.84. This indicates that of all the high risk loans present in the dataset, the model was able to correctly identify 8% more of these loans, with only a 1% decrease in the precision. This would allow the lending platform to identify and avoid more high risk loans, which would lead to fewer late payments or defaults over time, increasing the platform's revenue. Therefore, I would recommend the second logistic regression model. 

