# Loan Default Prediction

This project aims to predict the likelihood of borrowers defaulting on their loans using machine learning techniques. The workflow includes data preparation, feature engineering, model training, hyperparameter tuning, evaluation, and generating predictions. Below is an overview of the steps taken in this project.

## Overview

1. **Data Preparation**
   - Loaded training and test datasets.
   - Checked for and handled any missing values.
   - Explored the data through descriptive statistics and visualizations.

2. **Feature Engineering**
   - **Categorical Encoding:** Applied one-hot encoding to categorical variables.
   - **Interaction Features:** Created new features representing interactions between numerical variables to capture complex relationships.
   - **Data Splitting:** Split the training data into training and validation sets. Scaled the features for both training and test data.

3. **Model Training and Hyperparameter Tuning**
   - **Model Selection:** Used `XGBClassifier` for classification.
   - **Hyperparameter Tuning:** Conducted a randomized search to find the best hyperparameters using cross-validation.
   - **Model Evaluation:** Evaluated the model using ROC AUC and accuracy metrics on the validation set.

4. **Feature Importance**
   - Determined feature importance using the best model to understand which features contribute most to the predictions.
   - The top five most important features were:
     1. **Age_Income:** Interaction feature representing the product of age and income.
     2. **Age:** The age of the borrower.
     3. **InterestRate:** The interest rate of the loan.
     4. **LoanAmount:** The amount of the loan.
     5. **MonthsEmployed:** The number of months the borrower has been employed.

5. **Making Predictions**
   - Generated predictions on the test dataset.
   - Saved predictions in a CSV file for further analysis or submission.

## Results

- **Best Hyperparameters:** Found through randomized search, which improved the model performance.
- **ROC AUC Score:** The best ROC AUC score achieved was 0.7594.
- **Accuracy:** The model achieved an accuracy of 88.76% on the validation set.
- **Feature Importance:** The top five features identified by the model were:
  1. **Age_Income**
  2. **Age**
  3. **InterestRate**
  4. **LoanAmount**
  5. **MonthsEmployed**


## Acknowledgements

- [XGBoost Documentation](https://xgboost.readthedocs.io/)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
