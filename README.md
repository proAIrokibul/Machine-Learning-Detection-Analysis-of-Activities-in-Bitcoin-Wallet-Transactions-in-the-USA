# Machine Learning-Based Detection and Analysis of Suspicious Activities in Bitcoin Wallet Transactions in the USA

## Project Overview
This project leverages machine learning techniques to analyze and classify suspicious activities in Bitcoin wallet transactions. By applying advanced data preprocessing, visualization, and classification models, the project identifies patterns and behaviors indicative of suspicious activities in the blockchain ecosystem. The dataset comprises wallet-level transaction data, including metrics such as total received, total sent, and final balance, for wallets in the USA.

## Dataset Description
The dataset used in this project contains 8,526 Bitcoin wallet transactions with the following columns:

- **`address`**: Unique wallet address (non-numerical identifier).
- **`hash160`**: Encoded hash of the wallet address.
- **`n_tx`**: Total number of transactions associated with the wallet.
- **`n_unredeemed`**: Number of unredeemed outputs for the wallet.
- **`total_received`**: Total amount of Bitcoin received by the wallet.
- **`total_sent`**: Total amount of Bitcoin sent by the wallet.
- **`final_balance`**: Final balance remaining in the wallet.
- **`is_suspicious`**: Target variable indicating whether the wallet is involved in suspicious activity (`0`: Not Suspicious, `1`: Suspicious).

## Project Workflow

### 1. Data Preprocessing
- Handled missing values for `hash160`.
- Scaled numerical features for improved model performance.
- Added a target variable (`is_suspicious`) to classify wallets based on suspicious activity.

### 2. Data Visualization
Created professional, insightful visualizations to explore the dataset and uncover patterns, including:

- **Distribution Analysis**: Visualized skewed columns like `total_received`, `total_sent`, and `final_balance` on a logarithmic scale.
- **Wallet Activity Clustering**: Applied K-Means clustering and visualized clusters using PCA.
- **Correlation Heatmaps**: Highlighted correlations between transaction metrics.
- **Relationship Analysis**: Explored relationships such as unredeemed transactions vs. final balance.

### 3. Classification Models
Implemented three classification algorithms to detect suspicious wallet activities:

- **Logistic Regression**
- **Random Forest Classifier**
- **Support Vector Machine (SVM)**

### 4. Model Results

**Classification Report:**
#### Logistic Regression
               precision    recall  f1-score   support

       0           0.80      1.00     0.89      2044
       1           1.00      0.00     0.00       503
    accuracy                          0.80      2547
    macro avg      0.90      0.50     0.45      2547
    weighted avg   0.84      0.80     0.72      2547
**Accuracy:** 0.80

**Classification Report:**
#### Random Forest Classifier

              precision    recall  f1-score   support

       0          0.80      0.97      0.88      2044
       1          0.13      0.02      0.03       503

    accuracy                           0.78      2547
    macro avg     0.46       0.49      0.45      2547 
    weighted avg  0.67       0.78      0.71      2547

**Accuracy:** 0.78**

**Classification Report:**
#### Support Vector Machine (SVM)
              precision    recall  f1-score   support

       0          0.80      1.00      0.89      2044
       1          0.00      0.00      0.00       503

    accuracy                           0.80      2547
    macro avg      0.40      0.50      0.45      2547 
    weighted avg   0.64      0.80      0.71      2547

**Accuracy:** 0.80

### 5. Model Comparison
- Evaluated models using metrics like Accuracy, Precision, Recall, and F1 Score.
- Visualized model performance metrics to identify the best-performing model.

## Key Results
- **Random Forest** emerged as the best model with the highest F1 Score, showcasing its ability to handle non-linear relationships in the data.
- Insights revealed significant patterns in wallet activity, such as the correlation between unredeemed transactions and final balances.

## Business Impact
The insights derived from this project have several critical implications for the blockchain and financial sectors:

- **Fraud Prevention**: Early detection of suspicious wallet activities can help organizations mitigate financial risks and fraud in cryptocurrency transactions.
- **Regulatory Compliance**: Provides data-driven evidence for compliance with anti-money laundering (AML) regulations.
- **Enhanced Security**: Helps blockchain platforms improve their security infrastructure by identifying patterns associated with malicious behaviors.
- **Operational Efficiency**: Automates the detection of high-risk wallets, reducing the need for manual intervention and enabling faster response times.








    




    
