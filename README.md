# Bankruptcy-Prediction

his project looks at predicting bankruptcy for companies using machine learning models on financial data.

## Data
The data consists of financial metrics for companies over 5 years, with the target variable indicating whether the company went bankrupt in the 6th year. The train and test directories contain data files for each year from 1st through 5th.

## Data Fields:

  * Id - Company Identifier
  * X1-X64 - Financial metrics like profitability, liquidity, leverage etc.
  * Bankrupt - Target variable, 0/1 indicating bankruptcy

## Models
The following machine learning models are used:

 * Naive Bayes
 * Logistic Regression
 * SVM
 * Gradient Boosting
 * Neural Network
   
Grid search is implemented for hyperparameter tuning. Models are evaluated using accuracy, precision, recall, and ROC AUC.

## Usage
The main notebook contains the end-to-end workflow:

 1. Data Exploration
 2. Data Preprocessing
     * Handling class imbalance
     * Feature engineering
 3. Model Training and Evaluation
 4. Conclusions

## Results
Gradient boosting achieved the best performance with 62% recall, outperforming other models. Key findings:

* Class imbalance handled via SMOTE oversampling and recall score
* Parameter tuning improved baseline Seasonal Naive MAPE from 27.8% to 23.7% for SARIMA model
* Feature importance identified key financial metrics predicting bankruptcy
