# Bank Term Deposit Subscription

## Problem Overview

This project focuses on predicting whether a customer will subscribe to a bank term deposit based on customer attributes and related information.
It is a **binary classification problem**:
- '1' → Customer subscribes to a term deposit  
- '0' → Customer does not subscribe  

The model is built using **Logistic Regression** on the Bank Marketing Dataset.


## Dataset Description

The dataset contains information about past customers.

### With Key Details:
- Total attributes: 17
- Target variable: 'y' (subscribed: yes or no)
- Feature types: numerical and categorical
- Contains class imbalance (majority: non-subscribers)

## Data Preprocessing

The dataset was cleaned and transformed before model training:

- Replaced unknown values using most frequent category strategy
- Removed features to reduce complexity
- Encoded categorical variables:
  - Binary encoding
  - One-hot encoding


## Handling Class Imbalance

The dataset is imbalanced, with significantly fewer positive cases (subscribers).

To address this:

- Data is balanced using SMOTE on training data
- This helps improve minority class learning by generating synthetic samples

## Model Training

- Model: Logistic Regression
- Trained model after being preprocessed, balanced on the training data

## Evaluation 

The model was evaluated using:

- Accuracy
- Precision, Recall, F1-score
- Confusion Matrix

## Results

- The model performs better in predicting the majority class, which is non-subscribers
- Performance on the minority class (subscribers) is comparatively lower
- This indicates that:
  - The dataset has class imbalance
  - Logistic Regression may underfit complex behavioral patterns
