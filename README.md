# Delivery Duration Prediction

This is a Python code repository for predicting delivery duration based on historical data. The code involves data preprocessing, feature engineering, feature selection, and model selection. We use various regression models and scalers to find the best-performing model.

## Getting Started

To get started with this project, you'll need Python installed on your system. You can install the required libraries using the following command:

```bash
pip install numpy pandas matplotlib seaborn xgboost lightgbm scikit-learn statsmodels
```

You can download the dataset used in this code from [here](https://github.com/Mourya-wizard/Delivery-Duration-Prediction/blob/main/historical_data.csv) and place it in the same directory as the code.

## Code Overview

The code is divided into several sections:

1. **Data Loading and Initial Exploration**
   - Reads the historical data from a CSV file.
   - Performs basic data exploration.

2. **Feature Creation**
   - Converts date columns to datetime objects.
   - Calculates the target variable for regression, 'actual_total_delivery_duration'.
   - Creates additional features such as 'busy_dashers_ration' and 'estimated_non_prep_duration'.

3. **Data Preparation for Modeling**
   - One-hot encodes categorical variables like 'order_protocol', 'market_id', and 'store_primary_category'.
   - Fills missing values in 'store_primary_category' using the mode of 'store_id'.
   - Drops unnecessary columns.
   - Handles missing and infinite values.

4. **Correlation Analysis**
   - Computes and visualizes the correlation matrix.

5. **Feature Engineering**
   - Creates new features like 'percent_distinct_item_of_total' and 'avg_price_per_item'.
   - Drops some columns based on correlations.

6. **Variance Inflation Factor (VIF)**
   - Computes VIF to handle multicollinearity and selects relevant features.

7. **Feature Selection - Random Forest and Principal Component Analysis (PCA)**
   - Uses Random Forest to rank feature importances.
   - Performs PCA for feature reduction.

8. **Model Selection**
   - Includes regression models such as Ridge, Decision Tree, Random Forest, XGBoost, LGBM, and MLP.
   - Compares model performance using different feature sets and scalers.

## Running the Code

You can run the code by executing each section in a Jupyter Notebook or a Python environment. Make sure to adjust the file paths and parameters as needed.

## Conclusion

The best-performing model for delivery duration prediction is LGBM with the selected features and appropriate scaling. You can further fine-tune this model or use it as a starting point for your delivery duration prediction project.
