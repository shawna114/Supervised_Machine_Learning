# Supervised Machine Learning Homework - Predicting Credit Risk

Objective: Building a machine learning model that attempts to predict whether a loan from LendingClub will become high risk or not while comparing outcomes from the Logistic Regression and Random Forest Classifier models.

## Overview

LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.

## Data

An entire year's worth of data (2019) was used to predict the credit risk of loans from the first quarter of the next year (2020). The two CSVs used were undersampled to give an even number of high risk and low risk loans. In the original dataset, only 2.2% of loans are categorized as high risk. For a truly accurate model, special techniques need to be used on imbalanced data. Undersampling is one of those techniques. Oversampling and SMOTE (Synthetic Minority Over-sampling Technique) are other techniques that are also used.

## Preprocessing: Converting categorical data to numeric

A training set from the 2019 loans by creating 'dummy' fields to convert the categorical data to numeric columns. Similarly, a testing set from the 2020 loans was created with 'dummy' fields. There were categories in the 2019 loans that do not exist in the testing set. Fitting the training set and trying to score it on the testing set in its original form would result in an error. Code was used to fill in the missing categories in the testing set. 

## Considering the models

Two models were created and compared for the data sets provided: a logistic regression, and a random forests classifier. Predictions were made prior to creating, fitting, and scoring the models on which would perform better. 

## Fit a LogisticRegression model and RandomForestClassifier model

A LogisticRegression model was created, fitted to the data, and scored. The same was completed for a RandomForestClassifier. Predictions were made on which model performed better. 

## Revisit the Preprocessing: Scale the data
'Standard Scaler' was used to scale the training and testing sets. A prediction was made on how scaling will affect model accuracy prior to re-fitting the LogisticRegression and RandomForestClassifier models on the scaled data.

## Model Comparison

It was determined that the unscaled random forest model was the most accurate when compared with scaled and unscaled models for both classifiers.

Model Scores:
* Logistic Regression:          56%
* Random Forest:                64%
* Scaled Logistic Regression:   56%
* Scaled Random Forest:         50%
