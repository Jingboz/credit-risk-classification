# Module 12 Report Template

## Overview of the Analysis

The analysis is mainly for establishing a machine learning model to predict borrowers future fulfillment behaviours based on various financial aspects. The financial information includes borrowrers loan size, interest rate, their income, number of accounts, derogatory marks and total debt. And whether the loan status is healthy or not is what needs to be predicted. The loan status is categoried into "0" which is healthy loan and "1" which is in high risk stage. Among the dataset, there are 75036 clients who have healthy loan and 2500 have high-risk loan.

We adapted two different logistic regression models. In the first model, datasets were randomly selected and splited by 75% and 25% for training and testing respectively. We trained the model by training datasets and predicted by testing datasets to see the accuracy. By contrast, the second model was fed by the oversampled version of training datasets by using RandomOverSampler, which means the number of 0 and 1 of labels data should be identical. Finally, we tested the model accuracy and confusion matrix by using the testing datasets.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Accuracy score is 0.992, which is pretty accurate as a logistic regression model.
  * For the healthy loan, precision is 1 and recall is 0.99. It indicates that this model can accurately determine the clients have healthy loan, but will miss some potential healthy borrowers.
  * For the high-risk loan, precision is 0.85 and recall is 0.91. It indicates that most of high-risk loan can be identified, but still has 9% miss catch and 15% incorrect rejections.

* Machine Learning Model 2:
  * Accuracy score is 0.994, which is even better than the first model in terms of the accuracy.
  * For the healthy loan, precision is 1 and recall is 0.99. It indicates that this model can accurately determine the clients have healthy loan, but will miss some potential healthy borrowers.
  * For the high-risk loan, precision is 0.84 and recall is 0.99. It indicates that most of high-risk loan can be identified. The 1% of miss catch can be ignored and the 15% incorrect rejections is not too bad in terms of protacting from high-risk borrowers.


## Summary

Overall, the second model performs better, since it has better accuracy which is 99.4%. Although the precision number is a bit lower than the first one, given the business purposes of loaning, it is better to reject an incorrectly predicted healthy behaviour customer than to accidently borrow money to a high-risk client. So it is more important to predict the "0" in this model and get the recall value of "0" as high as possible.

Thus, the oversampled model is recommended to be used in this case.