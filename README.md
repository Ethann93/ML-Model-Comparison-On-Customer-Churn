# Machine Learning Model Comparison On Customer Churn

## Introduction

This project aims to compare four different machine learning models to predict customer churn in a bank. The models considered are Decision Tree, Random Forest, XGBoost, and a tuned Decision Tree. The ultimate goal is to select the best-performing model based on the F1 score and use it to visualize feature importance and confusion matrix plots.

## Data Loading and Exploration

The dataset, named 'Churn_Modelling.csv,' is loaded using Pandas and dataset was extracted from Kaggle website: https://www.kaggle.com/datasets/shubh0799/churn-modelling. 
A preliminary exploration is performed to understand the data structure, data types, and summary statistics.

## Modelling

### Feature Engineering

The initial dataset is refined by removing irrelevant columns ('RowNumber', 'CustomerId', 'Surname').

### Feature Transformation

Categorical variables are transformed into numerical representations using one-hot encoding.

### Train-Test Split

The dataset is split into training and testing sets, with 80% of the data used for training and 20% for testing.

## Model Building - Decision Tree

A Decision Tree model is built using the default hyperparameters. Performance metrics, including accuracy, precision, recall, and F1 score, are calculated. A confusion matrix plot is generated to analyze the model's performance.

## Tuned Decision Tree

A hyperparameter tuning process is performed using GridSearchCV to optimize the Decision Tree model. The best hyperparameters and their corresponding F1 score are displayed.

## Random Forest & Cross Validation

A Random Forest model is built with hyperparameter tuning using GridSearchCV. Cross-validation is employed to find the best hyperparameters. The results, including accuracy, precision, recall, and F1 score, are presented.

## Cross Validation

A separate validation dataset is created to evaluate the Random Forest model's performance on unseen data. The model is trained using GridSearchCV with the predefined validation split, and the F1 score and other metrics are recorded.

## XGBoosting

An XGBoost model is built with hyperparameter tuning using GridSearchCV. The best hyperparameters and corresponding F1 score are displayed.

## Results

The F1 scores, along with other performance metrics, for each model are presented in a tabular format. The models are sorted by F1 score in descending order.

## Confusion Matrix and Feature Importance

The confusion matrix and feature importance plots are generated for the champion model, which is the Random Forest model validated on a separate dataset. The confusion matrix provides insights into the model's performance in predicting churn, and the feature importance plot identifies the most significant features in predicting customer churn.

## Discussion

The project demonstrates a systematic approach to model comparison, hyperparameter tuning, and evaluation using various performance metrics. The Random Forest model, validated on a separate dataset, is identified as the champion model based on the highest F1 score. Feature importance analysis highlights critical features contributing to customer churn prediction. The confusion matrix provides insights into the model's strengths and weaknesses in classifying customers as churners or non-churners.
