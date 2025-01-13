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

#### Logistic Regression
          precision    recall  f1-score   support

       0       0.80      1.00      0.89      2044
       1       1.00      0.00      0.00       503
       
    accuracy                           0.80      2547
    macro avg       0.90      0.50     0.45      2547
    weighted avg    0.84      0.80     0.72      2547
