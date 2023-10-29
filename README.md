# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

The purpose of this analysis is to create a model that can accurately predict the outcome of a loan when given data about the borrower.
The data points included in this analysis are loan size, interest rate, borrower income, debt to income ratio, derogatory marks, number of accounts, total debt, and status of the loan. In the dataset there are a total of 75036 loans that are in good standing (marked as a "0") and 2500 loans not in good standing (Marked as a "1"). In this analysis we created a "y" variable that uses the "loan_status" column as the label variable we will be attempting to predict, and an "X" variable that will use all the other provided data for the machine learning model to base its decision on. We will split the data into training and testing datasets using the "train_test_split" library in python, so that our model can learn from the already provided data. Once we have the data split we can create the model instance, and fit the data into the model. This will teach the model about the current data, and allow it to make predictions when given new data. Finally, we will gather the final information about the model, such as the balanced accuracy score, and classification report. 

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  
  Balanced accuracy score: 0.9520479254722232
  
  Classification Report:
  [
                  precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                           0.99     19384
   macro avg       0.92      0.95      0.94     19384
weighted avg       0.99      0.99      0.99     19384]

* Machine Learning Model 2:
    Balanced accuracy score: 0.9936781215845847
  
  Classification Report:
  [
                  precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.99      0.91       619

    accuracy                           0.99     19384
   macro avg       0.92      0.99      0.95     19384
weighted avg       0.99      0.99      0.99     19384]
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
According to the classification reports provided, the logistic regression model used with the RandomOverSampler data performed better, and was more accurate when prediction the outcome of a loan. The performance of the models however, depends on which goal you are trying to achieve. If the main goal is to provide loans to only those who will most likely have a good standing loan, the model will likely predict the correct outcome, but if you are trying to give as many loans as possible and want to take a certain calculated risk on loans that may default, you may end up with more loans in default than anticipated, as the model can only predict loans that will go into default up to a .85 ratio. 
