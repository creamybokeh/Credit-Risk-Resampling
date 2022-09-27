# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

The purpose of the analysis was to try to predict the creditworthiness of borrowers based on historical lending activity data. We used supervised learning to run the data through several models, one using the data provided and another using oversampled data.
The financial data was stored on as a CSV file. It contained information such as loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debt and loan status. The loan status data was used as our y variable. A 0 in the column means the loan is healthy and a 1 means that the loan has a higher risk of default.
We first split the data into training and testing sets. As described above, for the labels set or (y) we used the loan_status column. The features or (X) was created from the remaining columns. We then created a logistic regression model with the original data and ran it through an accuracy score calculation, generated a confusion matrix and then printed a classificaiton report.
The data was then resampled and run through another logistic regression model. The data was resampled because there was a small number of high-risk loan labels and by resampling might help to increase the accuracy of the model.


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.

• The model 1 balanced accuracy score was approx. 95%.
• The model 1 precision score was 100% for healthy loans, 85% for high-risk loans and 99% average overall.
• The model 1 recall score was 99% for healthy lonas, 91% for high-risk loans and 99% average overall.


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

• The model 2 balanced accuracy score was approx. 99%.
• The model 2 precision score was 100% for healthy loans, 84% for high-risk loans and 99% average overall.
• The model 2 recall score was 99% for healthy lonas, 99% for high-risk loans and 99% average overall.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

In summary, model 2, the logistic regression model with resampled data seemed to perform better.
The accuracy score was about 4% higher, and while the precision was lower by 1% for the high-risk loan category, the recall for high-risk loans increased by 8% which means the model was able to accurately identify 99% of all high-risk loans, which is excellent. Overall, the models seem to perform better (but not really by much) when predicting the healthy loans but that is most likely because there is much more data it can sample from.
