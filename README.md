# Housing-price-prediction

## Goal
To predict the sale prices of houses in Ames dataset from Kaggle.

## Primary model evaluation metric
Root Mean Squared Error (RMSE / RMSLE)

## Models tested
Lasso regression
Elastic Net regression
Kernel Ridge regression
Gradient Boosting regression
XGBoost
LightGBM
Stacked average model of above models

## Notebook organization
- Loading libraries
- Reading train and test files
- Data processing
    - Outliers
    - Log-transformation of target variable `SalePrice`
    - Combining the training and test datasets
    - Feature engineering
    - Correlation heatmap
    - Missing data and imputation
    - Transforming numerical variables
    - Label encoding categorial variables
    - Creating an additional feature: Total Square Footage
    - Checking for skewed numerical features
    - Box Cox Transformation of skewed features
    - Aquiring dummy categorical variables
    - Creating new training and test datasets
- Modeling
    - K-fold validaton
    - Base models
        - Lasso regression
        - Elastic Net regression
        - Kernel Ridge regression
        - Gradient Boosting regression
        - XGBoost
        - LightGBM
        - Base model scores evaluated on rmsle
    - Stacking the base models
        - Averaging the models
        - Meta model
        - Model evaluation
    - Ensembling the stacked model with XGBoost and LightGBM
    - Prediction
- Submission

## Findings and results
The most successful was the ensembling of the stacked regressor at 65% with XGBoost at 10% and LightGBM at 10%.
