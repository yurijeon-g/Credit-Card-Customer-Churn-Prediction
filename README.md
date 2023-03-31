# Credit-Card-Customer-Churn-Prediction
This notebook goes through various machine learning techniques such as Random Forest and LightGBM to predict whether a customer would churn. The best roc-auc score models' hyperparameters were tuned in an attempt to get better evaluation metrics.

## Overview

In this project, I aim to perform a comprehensive exploratory data analysis (EDA) on a credit card dataset, using visualization techniques. Through univariate and bivariate analyses, I aim to extract valuable insights from the data that will reveal the behavior of customers who have churned. By understanding these patterns, we can provide better services to these customers and potentially reverse their decisions. Additionally, I intend to use this data to build a model that predicts customer churn the bank can use to reduce customer churn.

## Dataset
The dataset consists of information on 10,000 customers, including their age, salary, marital status, credit card limit, credit card category, etc. Only 16.07% of customers have churned, thus the dataset has a class imbalance. In order to increase predictive and classification efficacy of the models, techiques such as oversampling the training set was applied.

## Aim 
The main objective in this business scenario is to recognize clients who are at risk of churning. In the event that we inaccurately forecast a non-churning client as churned, it will not have significant negative impacts on our business. However, if we incorrectly predict a churning customer as non-churning, it could have detrimental consequences. Therefore, in order to prevent such situations, it is crucial to ensure a high recall score (true positives divided by true positives plus false negatives).

## Notebook
Check out the notebook for this project [here](https://github.com/yurijeon-g/Credit-Card-Customer-Churn-Prediction/blob/main/customer-churn-prediction.ipynb)

## Project Insights

The LGBM Classifier model was the best in its churn prediction with its ROC-AUC Score: 94 and Precision, Recall and F1 scores being 0.95 ,0.97,0.96.

However it should be noted that besides the Logistic Regression model, all the applied ML models had great scores for f1, precision and recall. LGBM was chosen for its slightly higher roc-auc score although Random Forest Classifier had a higher recall score.

Features importance when it comes to predicting customer churn were as follows: 
![image](https://user-images.githubusercontent.com/123054352/229087784-195b075b-6b6f-4a06-9f43-7f0a4dcd8d4e.png)
Surprising most categorical features such as age and gender or credit card type were less important in determing credit card customer churn. 
The most significantly important feature was total transaction amount which had almost twice the importance value of the next most important feature.

