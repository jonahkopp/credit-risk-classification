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
  * The precision of the model on healthy loans is 99.5%. This is the proportion of healthy loan predictions that were in fact healthy loans.
  * The recall of the model on healthy loans was also over 99%. THis means that over 99% of healthy loans were correctly identified as healthy loans.



## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.