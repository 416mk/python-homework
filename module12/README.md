Module-12-Challenge
In this repository you will find a .ipynb file named credit_risk_resampling.ipynb, in this file we are tasked with dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

Part 1 Split the Data into Training and Testing Sets
We will create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns. We will check the balance of the labels variable (y) by using the value_counts function. We will then split the data into training and testing datasets by using train_test_split.

Part 2 Create a Logistic Regression Model with the Original Data
In this part we will fit a logistic regression model by using the training data (X_train and y_train). Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model. We will then Evaluate the model’s performance by doing the following:

Calculate the accuracy score of the model.

Generate a confusion matrix.

Print the classification report.

Lastly answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

Part 3 Predict a Logistic Regression Model with Resampled Training Data
Well start off by using the RandomOverSampler module from the imbalanced-learn library to resample the data. We will then sse the LogisticRegression classifier and the resampled data to fit the model and make predictions. We will then Evaluate the model’s performance by doing the following:

Calculate the accuracy score of the model.

Generate a confusion matrix.

Print the classification report.

Lastly answer the following question: How well does the logistic regression model, fit with oversampled data, predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

Part 4 Credit Risk Analysis Report
Overview of the Analysis
In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

Explain the purpose of the analysis.
The goal of the analysis is to build a model that can identify the creditworthiness of borrowers.

Explain what financial information the data was on, and what you needed to predict.
The analysis financial data, include information about loan_size,interest_rate,borrower_income,debt_to_income,num_of_accounts, derogatory_marks,total_debt. We are trying to predict a certain outcome based on the available financial data. In this case, we are looking to predict whether a loan is healthy or high-risk.

Provide basic information about the variables you were trying to predict (e.g., value_counts).
E.G. (Value Counts)

0 75036

1 2500

Name: loan_status, dtype: int64

Indicating two classes: 0 and 1. Class 0: There are 75,036 instances labeled as 0. This class represents loans that are considered healthy. Class 1: There are 2,500 instances labeled as 1. This class represents high-risk loans.

The dataset seems imbalanced, with a significantly larger number belonging to class 0 compared to class 1.

Describe the stages of the machine learning process you went through as part of this analysis.
Data Collection: Gathering financial data that includes both features and the target variable.

Data Splitting: Splitting the dataset into training and testing sets.

Model Selection: In this case, the models we used are Logistic Regression and Resampling.

Briefly touch on any methods you used (e.g., LogisticRegression, or any resampling method).
LogisticRegression: Used for multiclass classification tasks.It models the probability of a certain class.

Resampling: Used to address class imbalance issues, ensuring the model is not biased towards the majority class.

Results
Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

Machine Learning Model 1:
Description of Model 1 Accuracy, Precision, and Recall scores.
(-------------------------------------------------------------------------------------------------------------------------------)

Balanced Accuracy Score:

Overall: 0.95

A balanced accuracy score of 0.95 indicates strong overall performance in correctly classifying instances from both classes

(-------------------------------------------------------------------------------------------------------------------------------) Precision and Recall Scores: Class 0 (Healthy Loan)

Precision: 1.00 (100%): Model 1 correctly predicts 100% of all healthy loans.

Recall: 0.99 (99%): Model 1 identifies 99% of the actual healthy loans.

(-------------------------------------------------------------------------------------------------------------------------------)

Precision and Recall Scores: Class 1 (Risky Loan)

Precision: 0.85 (85%): When Model 1 predicts a high-risk loan, it is correct 85% of the time.

Recall: 0.91 (91%): Model 1 correctly identifies 91% of the actual high-risk loans.

(-------------------------------------------------------------------------------------------------------------------------------)

Overall Metrics (avg / total) for both classes.

Precision: 0.99 (99%)

Recall: 0.99 (99%)

(-------------------------------------------------------------------------------------------------------------------------------)

Machine Learning Model 2:
Description of Model 2 Accuracy, Precision, and Recall scores.
Balanced Accuracy Score:

Overall: 0.99

A balanced accuracy score of 0.99 indicates strong overall performance in correctly classifying instances from both classes

(-------------------------------------------------------------------------------------------------------------------------------)

Precision and Recall Scores: Class 0 (Healthy Loan)

Precision: 1.00 (100%): Model 2 correctly predicts 100% of all healthy loans.

Recall: 0.99 (99%): Model 2 identifies 99% of the actual healthy loans.

(-------------------------------------------------------------------------------------------------------------------------------)

Precision and Recall Scores: Class 1 (Risky Loan)

Precision: 0.84 (84%): When Model 2 predicts a high-risk loan, it is correct 84% of the time.

Recall: 0.99 (99%): Model 2 correctly identifies 99% of the actual high-risk loans.

(-------------------------------------------------------------------------------------------------------------------------------)

Overall Metrics (avg / total) for both classes.

Precision: 0.99 (99%)

Recall: 0.99 (99%)

(-------------------------------------------------------------------------------------------------------------------------------)

Summary
Summarize the results of the machine learning models, and include a recommendation on the model to use, if any.

Which one seems to perform best? How do you know it performs best?
Model 2 has a higher balanced accuracy score (0.99) compared to Model 1 (0.95). Higher balanced accuracy indicates better performance.

Precision and Recall (Class 1): Model 2 has a higher recall for Class 1 (high-risk loan) compared to Model 1 (0.99 vs. 0.91). However, Model 1 has a slightly higher precision for Class 1 (0.85 vs. 0.84).

Based on the balanced accuracy score and the recall for Class 1, Model 2 appears to perform better overall. The higher balanced accuracy suggests better overall classification performance, and the higher recall for Class 1 indicates that Model 2 is better at identifying high-risk loans.

Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the 1's, or predict the 0's? )
In this scenarios where the positive class (1) represents such as fraud detection, accurately identifying and predicting the positive class is essential to prevent consequences associated with false negatives. Conversely, where the negative class (0) represents the majority class, correctly identifying and predicting the negative class is crucial to avoid unnecessary disruptions, even if it means tolerating some false positives.

Recommendation of the models please justify your reasoning.
Both models demonstrate strong overall performance, with high balanced accuracy scores, precision, and recall for the positive class (1). However, Model 2 displays a slightly higher balanced accuracy and superior recall for the positive class, indicating better performance in identifying high-risk loans. Therefore, I recommend using Model 2 for predicting loan status.

End of Module 12

was helped by ai services, blackbox and chatgpt inspiration as well and some tips and tricks from other students of the class!