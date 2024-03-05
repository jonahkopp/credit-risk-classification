# credit-risk-classification

# Credit Risk Classification Report

## Overview of the Analysis

The goal of this analysis was to predict the health of loans using loan and user data. Our data contained loans that were deemed high risk or healthy and some associated data about the loan and the user that took out the loan. This data included user income, debt-to-income ratio, interest rate of the loan, derogatory marks, and more.

We hypothesize that with this data, we can construct a model that will predict the high risk vs healthy loan status using these same variables so we can understand the risk profile of the loans we give.

One note on the data is that it is unbalanced: most loans are healthy. The model may be biased if we ignore this fact.

To build this model, first we gathered the input data and split it into a testing set and a training set. The training set was then used to train a logistic regression model whose goal was to classify the loan status (healthy or high risk) of a given loan in that dataset.

Following model training, we then used the model to predict the loan status of the test set loans. We compared those predictions with the actual loan statuses of those loans to determine model accuracy.

## Results

We looked at the balanced accuracy score, confusion matrix, and precision and recall scores to judge the effectiveness of the model. These were calculated by predicting the loan status of loans in the test set and comparing those predictions to the actual observations.

* Logistic Regression Model:
  * Balanced accuracy was 95%. The accuracy was slightly higher on healthy loans and slightly lower on high-risk loans.
  * The confusion matrix (printed below) shows us that there are extremely low rates of false positives (that is, a loan that was predicted to be healthy but was in fact low risk). This rate is 0.5%.
  * The false negative rate is much higher, at 9%. This means that we would have assessed these loans as high-risk when in fact they were healthy.
  * The precision of the model on healthy loans is 99.7%. This is the proportion of healthy loan predictions that were in fact healthy loans.
  * The recall of the model on healthy loans is 99.5%. THis means that 99.5% of healthy loans were correctly identified as healthy loans.
  * The precision and recall of the high-risk loans is slightly worse, at 84.7% and 91.0% respectively. This demonstrates that the model is not as accurate when it comes to these loans.


Confusion Matrix:
| Prediction / Actual | Healthy | High-Risk |
| -------- | ------- | ------- |
| Healthy | 18663  | 102    |
| High-Risk | 56 | 563     |


## Summary

Overall the model has very high accuracy. To determine if it is suitable to use, we need to know the business impact of following it's recommendations. For example, we need to know how much money we stand to lose from loans that are high-risk but are incorrectly labeled as healthy, because this will happen. Perhaps we should look at the false predictions and see if they are larger or smaller loans than average, as that would give us a way to size the risk.

But overall, as a way to estimate which loans will be healthy and which will be high risk, this is a great model.