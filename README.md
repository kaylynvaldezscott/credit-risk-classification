# credit-risk-classification
Submitted by Kaylyn Valdez-Scott Date: 18-JAN-2024 Project Title: Module 20 Credit Risk Classification

**Purpose of project** : use various techniques to train and evaluate a model based on loan risk.

Assignment is broken down into 3 sections:

1. Split the Data into Training and Testing Sets
2. Create a Logistic Regression Model with the Original Data
3. Write a Credit Risk Analysis Report

**Overview of the Analysis**
Firstly, I looked at the data provided in the CSV to investigate factors related to:
- loan size
- interest rate
- borrower income
- debt to income ratio
- number of accounts the borrower holds
- derogatory marks against the borrower
- total debt
- status of loan

The financial information the data set presented was used in order to find out whether or not a borrower's loan would be a healthy or high-risk loan. To check the target values I would be using, I used y.value_counts() to see how much data we were working with. I began by splitting the presented data into two sections using scikit-learn and LogisticRegression. The first training set was used in order to create an initial Logistic Regression Model, and compare it to the next testing prediction model.  

<img width="1431" alt="Screenshot 2024-01-18 at 9 59 51 AM" src="https://github.com/kaylynvaldezscott/credit-risk-classification/assets/141589524/d8613605-12e5-4aec-a03d-b028901fa111">

I then calculated and printed the accuracy scores, and created a classification report to easily display and analyze the data. Analysis can be seen below under 'Results'. 

In order to make sure testing data had an equal value to compare to the Logistic Regression Model, I then used RandomOverSampler to resample the data. This information was based on the original data, but resampled for comparison and analysis. I then used this new resampled data to create the second Linear Regression Model labeled 'lr_resampled_model'.  

I again calculated and printed the accuracy scores, and created a second classification report to easily display and analyze the data. Analysis can be seen below under 'Results'.

<img width="1432" alt="Screenshot 2024-01-18 at 10 29 18 AM" src="https://github.com/kaylynvaldezscott/credit-risk-classification/assets/141589524/e1470120-f558-4618-9ee6-732bce1e6d3b">

**Results**
Machine Learning Model 1:

Accuracy:: 99% 
Precision: 100% for healthy loans, 87% for high risk loans
Recall: 100% for healthy loans, 89% for high risk loans

<img width="1155" alt="Screenshot 2024-01-18 at 10 33 35 AM" src="https://github.com/kaylynvaldezscott/credit-risk-classification/assets/141589524/41ac0708-3915-4930-8e04-1c4a21b995b4">


Machine Learning Model 2:

Accuracy: 99%
Precision: 99% for healthy loans, 99% for high risk loans
Recall: 99% for healthy loans, 99% for high risk loans

<img width="1160" alt="Screenshot 2024-01-18 at 10 34 25 AM" src="https://github.com/kaylynvaldezscott/credit-risk-classification/assets/141589524/161abfea-a407-4dd0-8b7d-8bd67ec63271">

**Summary**
In conclusion, through the analysis I can assume that Machine Learning Model 2 will perform best overall. With 99% accuracy and precision for both healthy and high-risk loans, there is a better probability of valid results compared to Model 1. Although Model 1 has higher precision for healthy loans, there is too much of a difference when looking at high-risk loans. 

Performance does depend on the problem we are trying to solve. For instance, if the goal was to look solely at high-risk loans in order to reduce the amount the company is taking on, Model 2 would be the one to look to. If we were taking a look at only healthy loans then Model 1 could be used. Since we are examining both here, I would recommend using Machine Learning Model 2. 

