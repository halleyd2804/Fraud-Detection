# Fraud-Detection
## Overview
This project implements a fraud detection system using machine learning models, including **Logistic Regression** and **Neural Networks**. The goal of this project is to predict fraudulent transactions based on various features.
The code is written in **Jupyter Notebooks** for easy exploration and experimentation.

---

## Table of Contents

1. [Dataset](#dataset)
2. [Models](#models)
3. [Evaluation](#evaluation)
 
---

## Dataset
**Associated Data Files:** 

1. `transactions.csv`: Each row denotes a transaction. The columns are as follows:

   - **TRANSACTION_ID**: A unique ID of the credit card transaction.
   - **TX_DATETIME**: Date and time of the transaction.
   - **CUSTOMER_ID**: ID of the credit card owner.
   - **TERMINAL_ID**: ID of the terminal where the transaction originated.
   - **TX_AMOUNT**: Amount of the transaction in dollars.
   - **TX_FRAUD**: Label denoting if the transaction was fraudulent (label of 1) or genuine (label of 0).

2. `card_data.csv`: This file contains pre-computed feature-engineered columns in addition to the ones listed above. The extra columns are as follows:

   - **IS_WEEKEND**: Denotes if the transaction occurred over a weekend (label of 1) or a weekday (label of 0).
   - **IS_WEDNESDAY**: Denotes if the transaction occurred on Wednesday.
   - **IS_NIGHT**: Denotes if the transaction occurred at night (label of 1) or during the day (label of 0).
   - **TX_HOUR**: The hour at which the transaction occurred.
   - **TX_DATE**: The date of the transaction (i.e., the date excluding time information).
   - **TX_WEEK**: The week of the transaction (i.e., the week number when the transaction occurred).
   - **TERMINAL_TOTAL_1D**: The number of transactions that occurred in the previous *day* for the associated terminal ID.
   - **TERMINAL_FRAUD_1D**: The number of fraudulent transactions that occurred in the previous *day* for the associated terminal ID.
   - **TERMINAL_RISK_1D**: The ratio of fraudulent transactions that occurred in the previous *day* for the associated terminal ID.
   - **CUSTOMER_TOTAL_1D**: The number of transactions that occurred in the previous *day* for the associated customer ID.
   - **CUSTOMER_FRAUD_1D**: The number of fraudulent transactions that occurred in the previous *day* for the associated customer ID.
   - **CUSTOMER_RISK_1D**: The ratio of fraudulent transactions that occurred in the previous *day* for the associated customer ID.
   - **TERMINAL_TOTAL_1W**: The number of transactions that occurred in the previous *week* for the associated terminal ID.
   - **TERMINAL_FRAUD_1W**: The ratio of fraudulent transactions that occurred in the previous *week* for the associated terminal ID.
   - **TERMINAL_RISK_1W**: The ratio of fraudulent transactions that occurred in the previous *week* for the associated terminal ID.
   - **CUSTOMER_TOTAL_1W**: The number of transactions that occurred in the previous *week* for the associated customer ID.
   - **CUSTOMER_FRAUD_1W**: The number of fraudulent transactions that occurred in the previous *week* for the associated customer ID.
   - **CUSTOMER_RISK_1W**: The ratio of fraudulent transactions that occurred in the previous *week* for the associated customer ID.
   - **SPENT_1D**: The average spent for the customer in the previous *day*.
   - **SPENT_1W**: The average spent for the customer in the previous *week*.

---

## Models
1. **Logistic Regression**
- A simple linear model used as a baseline for classification tasks.
2. **Neural Network**
- A feed-forward neural network used to capture non-linear relationships in the data.
This project compares the performance of these models with different parameters and inputs.

## Evaluation
This project uses **Area Under the Curve score** to determine the best model. The **AUC** is a metric that measures the performance of a classification model, where a higher AUC score indicates better model performance. 
