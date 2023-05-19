# Credit-Risk-Classification_SupervisedML

- - -

## Overview of the Analysis

- Purpose
The porpose of this analysis is to review the Logisitc Regression Machine Learning Model in use for prodicting if a loan would be a good investment for a lender based off 1.loan size, 2.interest rate, 3.income, 4.debt-to-income ratio, 5.number of accounts, 6.derogatory marks, and 7.total_debt. 

- What is being predicted?
Using a dataset from a peer-to-peer lending services company that provides samples and a target column labeled `loan_status` we will be training the model to predict with a `0` being a "healthy loan" or a `1` being a "high-risk loan" on a separate portion of the data that will not be used in the training process.

- Goal
Idealy I would like to see an accuracy rate as close to 100% as possible with a low false-positive rate which would get customer loan applications rejected and a low false-negative rate which would be bad for the financial institution's bottom line.

- Steps
1. Load dataset.
2. Split data into portions; data to train the model with and data to test the model once trained.
3. Sample test with training data to pick optimal solver for logisitic regression model.
4. Train model with original training data.
5. Test trained model on test dataset.
6. Resample the training data & ensure equal number of data points.
7. Train model on resampled training data.
8. Test model trained on resampled training data on test dataset.

See instructions below for more in depth information on the steps.

- Measuring
from `SKLearn`:
1. `balanced_accuracy_score`, `confusion_matrix`, `classification_report` will be used to compare the two instances of the logisitic regression model. 
2. `train_test_split` will be used to split training and testing data points. 
3. `cross_val_score` will be used to test and pick the optimal solver for the model.
from `imblearn.over_sampling`:
4. `RandomOverSampler` will be used to oversample the training dataset for the oversampled instance of the model.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

### Machine Learning Model 1:
- Model was trained on a data sample of the original dataset.
- Prediciton Satisitics:
![ClassificationMatrix1](/Credit_Risk/classification_reports_screen_shots/Screenshot_Model_1.png)

- Results of the model on testing sample:
![CM1](/Credit_Risk/classification_reports_screen_shots/Screenshot_CM_1.png)

### Machine Learning Model 2:
- Model was trained on a resampled dataset of the training dataset.
- Prediciton Satisitics:
![ClassificationMatrix2](/Credit_Risk/classification_reports_screen_shots/Screenshot_Model_2.png)

- Results of the model on testing sample:
![CM2](/Credit_Risk/classification_reports_screen_shots/Screenshot_CM_2.png)


## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

- - -

## Instructions

The instructions for this Challenge are divided into the following subsections:

- Split the Data into Training and Testing Sets

- Create a Logistic Regression Model with the Original Data

- Predict a Logistic Regression Model with Resampled Training Data

- Write a Credit Risk Analysis Report

### Split the Data into Training and Testing Sets

Open the starter code notebook and use it to complete the following steps:

1. Read the `lending_data.csv` data from the Resources folder into a Pandas DataFrame.

2. Create the labels set (`y`) from the “loan_status” column, and then create the features (`X`) DataFrame from the remaining columns.

3. Split the data into training and testing datasets by using `train_test_split`.

### Create a Logistic Regression Model with the Original Data

1. Use your knowledge of logistic regression to complete the following steps:

2. Fit a logistic regression model by using the training data (`X_train` and `y_train`).

3. Save the predictions for the testing data labels by using the testing feature data (`X_test`) and the fitted model.

    - Evaluate the model’s performance by doing the following:

    - Calculate the accuracy score of the model.

    - Generate a confusion matrix.

    - Print the classification report.

4. Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

### Write a Credit Risk Analysis Report

Write a brief report that includes a summary and analysis of the performance of the machine learning models that you used in this homework. You should write this report as the README.md file included in your GitHub repository.

Structure your report by using the report template that Starter_Code.zip includes, ensuring that it contains the following:

1. An overview of the analysis: Explain the purpose of this analysis.

2. The results: Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.

3. A summary: Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.

- - -

## References
Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.

- - -

© 2023 edX Boot Camps LLC