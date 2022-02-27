# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
  This analysis focuses on the classification problem related to credit riak, wherein the healthy loans easily outnumber the risky loans. This type of a problem is inherently imbalanced and the goal here to use techniques to train and evaluate models with imbalanced classes.
* Explain what financial information the data was on, and what you needed to predict.
  The dataset consist of lending data with features such as loan_size, interest_rate etc on the loan. The target variable is loan_status which the value that needs to be predicted.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
"loan_status" is the value to be predicted.
0    75036
1     2500
Name: loan_status, dtype: int64
* Describe the stages of the machine learning process you went through as part of this analysis.
The process followed model-fit-predict stages. First the data was split into training and test datasets. Next a logistic regression model was created and fitted with the X_test values. The last step was to predict using this model and derive model performance such as accurancy and confusion matrix.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
The model was built using logistic regression on the original dataset and logistic regression with resampling the data. Both models were compared to understand if one predicts the credit risk for unhealthy loans better.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  Accuracy - 0.9889115309798473
  pre       rec       spe        f1       geo       iba       sup

          0       1.00      0.99      0.98      1.00      0.99      0.98     18765
          1       0.84      0.98      0.99      0.91      0.99      0.98       619

avg / total       0.99      0.99      0.98      0.99      0.99      0.98     19384

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  Accuracy - 0.9936781215845847
  pre       rec       spe        f1       geo       iba       sup

          0       1.00      0.99      0.99      1.00      0.99      0.99     18765
          1       0.84      0.99      0.99      0.91      0.99      0.99       619

avg / total       0.99      0.99      0.99      0.99      0.99      0.99     19384


## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
For this instance there is minimal difference in precision and recall values when logistic regression model is fit with oversampled data. There is not a significant advantage gained by oversampling the data as the original model itself was highly predictive.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
In this case, it was more important to predit "1" or unhealthy loans.

If you do not recommend any of the models, please justify your reasoning.
