# credit-risk-classification

## Background

In this project, machine learning techniques were used to train and evaluate a model based on loan risk. A dataset of historical lending activity from a peer-to-peer lending services company was used to build a model that can identify the creditworthiness of borrowers.

### Overview of the Analysis

* The purposre of this analysis was to make and train a model which will be able to predict the nature of the loan i.e. whether a loan is healthy loan or a high risk loan. 
* Dependant variable (y value) in this analysis was the "loan status" indicating if a loan is healthy or at high risk.
* Independent Variables (x values) were loan size, interest rate, borrower income, debt to income ratio, number of accounts and derogatory marks.
* This data was split into training and testing sets. This training set wass used to create Logistic Regression Model using the LogisticRegression module from scikit-learn. Using the testing feature data (X_test) and the fitted model, predictions on the testing data labels (y_test) were generated. Finally the model's performance was evaluated using confusion matrix and classification report.
* Two Logistic Regression models were created by using the original data set and resampled data using RandomOverSampler module from imbalanced-learn. In the end, their results were compared.

Below are the results showing comparison of two models.

### Results

#### Logistic Regression Model using the original data:

*  Balanced Accuracy Score: 95%
*  Precision : Healthy Loan - 100%
               High Risk loan - 85%
*  Recall : Healthy Loan - 99%
            High Risk loan - 91%
*  f1-score : Healthy Loan - 100%
              High Risk loan - 88%
              
#### Logistic Regression Model using the Oversampled data:

*  Balanced Accuracy Score: 99%
*  Precision : Healthy Loan - 99%
               High Risk loan - 99%
*  Recall : Healthy Loan - 99%
            High Risk loan - 99%
*  f1-score : Healthy Loan - 99%
              High Risk loan - 99%           
              
              
### Summary  

Using Logistic Regression Model using the original data, the balanced accuracy score is 95% which states that the model performs well with the given data. 

The Logistic regression model predicts `0` (healthy loan) with 100% precision whereas it predicts `1` (high-risk loan) with only 85% precision which shows that the model would predict loan's status as healthy better than the loan's status as high risk. It may be because the given data is highly imbalanced as total number of healthy loans are very high compared to the total number of high risk loans. 

The recall for healthy loan is 99% and recall for high risk loan that is 91%. This shows that 99% of healthy loan predictions made out of all predictions that could have been made are correct and also 91% of high risk loan predictions made out of all predictions that could have been made are correct but less compared to the predictions of healthy loan.

By looking at f1 scores we can say that overall predictions for healthy loan is better compared to high risk loans.

The balanced accuracy score generated for oversampled data is 99% which is better than the balanced accuracy score of model with original training data. For this case, the logistic regression model fit with oversampled data works well in terms of predicting both the `0` (healthy loan) and `1` (high-risk loan) with 99% of accuracy and recall compared to 85% recall using logistic regression model with original data.

So overall I can say that oversampling the data helps in getting higher balanced accuracy and recall scores. It is very important to predict both high risk loans and healthy loans correctly so the accuracy and recall value must be as high as possible which here in this case using the model with oversampled data is fulfilled.



