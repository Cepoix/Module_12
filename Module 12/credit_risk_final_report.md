# Module 12 Credit Risk Report

## Overview of the Analysis

* **Purpose of the analysis** - The purpose of this analysis was to see if the Logistic Regression model can determine the risky loans and the healthy loans using the original dataset and the resamples data. The dataset was resampled to increase the size of the minoity class (risky lonas). 

* **The Dataset** - We performed analysis on a dataset consisting of 77,536 loans. The data includes columns for  loan_size, interest_rate, borrower_income, debt_to_income ratio, number_of_accounts, derotatory_marks, total_debt, and loan_status. We tried to predict the **loan_status**. 


* **Class Distribution** - Out of the 77,536 total loans, 75,036 are considered healthy (Class 0) and 2500 are categorized as unhealthy (Class 1). Becasue the nummber of healty loans clearly outnumber the number of riskly lons, we used the RandomOverSamples in one of the machine learning models.

* **Stages of the Machine Learning Process** - The stages are as follows: 

    - Prepare the data - Import the file, establish the DataFrame, evaluate the class counts and resample the data. We will be using RandomOverSampler from imbalanced-learn to increase the size of our minority class (risky loans).
    
    - Separate the data into features and labels - The labels are what you are attempting to predict. We are trying to determine the status of the as either healthy (0) or high-risk (1). 
    
    - We used the train_test_split function and separated the features and labels data into training and testing sets. 
    
    - We imported the machine learning model from the library - We imported the LogisticRegression from SKLearn. 
    
    - We instantiated the model.
    
    - Fit the model using the training data.
    
    - We can use the model to  make predictions. 
    
    - Laslty, we calculated and compared the metrics like accuracy score, a confusion matrix. 
    
* **Machine Learning Methods Utilized** - 

    The two models that we used are:

    - LogisticRegression model from SKLearn
    - RandomOverSampler from imbalanced-learn
    
    In addition, we used:
    
    - train_test_split from SKLearn
    
    

## Results

Blow, please see the accuracy scores and the precision and recall scores of all six machine learning models.

* Machine Learning Model 1 - Logistic Regression on the original data:
  
  - Accuracy score: 0.952048
  - Precision: Class 0: 1.00 Class 1: 0.85
  - Recall: Class 0: 0.99 Class 1: 0.91
  
* Machine Learning Model 2 - Logistic Regression on the resampled data:

  - Accuracy score: 0.993678
  - Precision: Class 0: 1.00 Class 1: 0.84
  - Recall: Class 0: 0.99 Class 1: 0.99

## Summary

The precision and the recall were close to perfect or close to 1 under both the original and oversampled data models - this pertains to the healthy loans. In contrast, the risky loans have a close enough precision  between the model using oversampled data (0.84) and the original data which is 0.85. Lastly, the recall number is much higher for the logistic regression model using oversampled data which is at 0.99 than the model using the original data which is at 0.91. In conclusion, the logistic regression model is a good indicator of predicting both healthy and high-risk loans. 

