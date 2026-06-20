# Assignment 6: Model Evaluation, Explainability, and Fairness Reflection

## Dataset Description

This assignment uses a utility customer payment dataset containing demographic information, account details, billing information, payment history, and customer service interactions. The dataset includes both numerical and categorical variables and is used to predict whether a customer is likely to make a late payment in the following month.

The dataset contains 370 customer records and includes fairness-related attributes such as gender, age group, and region for fairness analysis.

## Target Variable

The target variable is:

late_payment_next_month

* 0 = Customer pays on time
* 1 = Customer makes a late payment

The objective of the model is to predict whether a customer will make a late payment in the next month.

## Model Used

A Decision Tree Classifier was used for this assignment.

The dataset was preprocessed by handling missing values, converting categorical variables into numerical format using one-hot encoding, and splitting the data into training and testing sets before model training.

## Main Evaluation Results

Model performance on the test dataset:

* Accuracy: 66.22%
* Precision: 71.11%
* Recall: 72.73%
* F1-Score: 71.91%

The confusion matrix results were:

* True Negatives (TN): 17
* False Positives (FP): 13
* False Negatives (FN): 12
* True Positives (TP): 32

Cross-validation results showed relatively consistent performance across different folds, suggesting moderate model stability.

## Main Business Interpretation

The model helps identify customers who may be at risk of making late payments. This allows the utility company to take proactive actions such as sending payment reminders, providing payment assistance, or monitoring higher-risk accounts. Feature importance, SHAP, and LIME analysis showed that variables such as previous late payments, monthly bill amount, autopay status, and customer support interactions play an important role in the model’s predictions. The fairness analysis showed some differences in prediction performance across gender, age groups, and regions. Although no severe bias was observed, the results suggest that fairness should continue to be monitored before using the model in real-world decision-making.

## One Limitation of the Model

One limitation of this model is that it shows some evidence of overfitting, as the training accuracy is higher than the testing accuracy. In addition, model performance varies across some demographic groups, indicating that further model tuning and fairness evaluation may be needed before deployment. Therefore, the current model should be considered an early prototype rather than a production-ready business solution.

