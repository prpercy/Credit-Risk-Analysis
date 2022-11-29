# Report Analysis

## Overview of the Analysis

* Purpose

Technology is making in-roads in finance industry. Financial industry has been using traditional methods to analyse credit risk for loan origination and underwriting. However with advances in technology, industry could use non-traditionals approaches towards credit risk analysis and as a consequence can extend credit to parties that were not part of their scope earlier. By using a dataset of historical lending activity from a peer-to-peer lending services company, this analysis builds a model that can identify the creditworthiness of borrowers. 

* Data
Analysis uses data already loaded in excel file (lending_data.csv).  Data has information available for 75,036 healthy loans and 2,500 high risk loans. Information contains features such as loan size, interest rate, borrower income, debt to income, number of accounts, deregatory marks and total debt.

* Exercise
In our exercise, Loan status ( 0 - healthy loans  vs 1 - high risk loans) is variable that needs to be predicted using financial information (features) such as loan size, interest rate, borrower income, debt to income, number of accounts, deregatory marks and total debt. Our prediction focus is towards high risk loans (i.e. loan status = 1).

* ML Process & Method
The model uses a logistic regression to predict the loan status. This is a type of statistical model used for classification and predictive analytics. Logistic regression estimates the probability of an event occurring based on a given dataset of various variables. Logistic regeression models's predicted variabes are either 0 or 1, as the model predicts whether an outcome will happen or not. Following exercise is performed to analyse health vs high risk loans using logistic regression model. Analysis also accounts for data imbalance (as very few data points are available for the high risk loans) using statistical sampling techniques (such as random over sampling). Towards the end of exercise, analysis checks the efficiency of model using various metrics such as Accuracy, Precision and Recall.


## Results

* Machine Learning Model 1:
  * Using logistic regression model historical data is analysed. 
  * Initially historical data has been split into train and test sections. 
  * 'Train' section data is used to fit/train the model and test section data is used to figure out the predictive power of the model.
  * The predictive power of the model is measured using following metrics:
      * Accuracy score: 95.2% accuracy score suggests that model was able to predict true positive and true negatives approx. 95% times.
      * Precision score: Model was able to predict healthy loans 100%, whereas for high risk loans of all predicted high risk loans approx. 85% were actually high risk loans.
      * Recall score: Model was able to identify 91% of high risk loans correctly. 



* Machine Learning Model 2: section data 
  * Similar to model 1, logistic regression model is used to analze historical data, however to address lower number of data points for high risk loans (Data has approx. 75k healthy loans whereas only 2.5k high risk loans - classic class imbalance case), random oversampling technique is used to inflate data points for high risk loans.
  * Resampled data (which has same number of data points for the healthy loans and high risk loans) is used to train the model
  * Test section data is used to figure out the predictive power of the model.
      * Accuracy score: 99% accuracy score suggests that model was able to predict true positive and true negatives approx. 99% times (better performance than Model 1).
      * Precision score: Model was able to predict healthy loans 100%, whereas for high risk loans of all predicted high risk loans approx. 84% were actually high risk loans. (Precision deteriorated compared to model 1 for high risk loan identification).
      * Recall score: Model was able to identify 99% of high risk loans correctly (a material improvement compared to model 1). 

## Summary

Model 2 (which uses random oversampling to account for data imbalance of high risk loans) performs better by identifying 99% of high risk loans correctly (vs 91% in Model 1). However if we were to focus on predicting healthy loans correctly, Model 1 would have been better.
