# Car Price Prediction Project

![Car Price Prediction](carpricepredictionimage.jpg)

This project aims to predict car prices using various regression techniques, including linear regression, ridge regression, and lasso regression. The analysis includes data cleaning, exploratory data analysis, feature engineering, and model comparison.

## Table of Contents

1. [Data Understanding and Exploration](#data-understanding-and-exploration)
2. [Data Cleaning](#data-cleaning)
3. [Data Preparation](#data-preparation)
4. [Model Building and Evaluation](#model-building-and-evaluation)
   - [Linear Regression](#linear-regression)
   - [Ridge Regression](#ridge-regression)
   - [Lasso Regression](#lasso-regression)
5. [Results Comparison](#results-comparison)

## Data Understanding and Exploration

- Dataset overview: 205 rows, 26 columns
- Exploratory data analysis using correlation matrices and heatmaps
- Identification of key variables affecting car prices

Key insights from correlation analysis:
- Price is highly positively correlated with carwidth, curbweight, enginesize, horsepower, wheelbase, and carlength
- Price is negatively correlated with citympg and highwaympg (approximately -0.70)
- Many independent variables are highly correlated, indicating potential multicollinearity issues

## Data Cleaning

- Handling misspellings in car company names
- Converting categorical variables to appropriate data types
- Extracting company names from the 'CarName' column

## Data Preparation

- Feature engineering: creating dummy variables for categorical features
- Scaling numerical features
- Splitting data into training and testing sets

## Model Building and Evaluation

### Linear Regression

- Implementation of basic linear regression model
- Evaluation using R2 score, RSS, and RMSE

### Ridge Regression

- Hyperparameter tuning using GridSearchCV
- Model fitting with optimal alpha value
- Comparison of performance metrics with linear regression

### Lasso Regression

- Hyperparameter tuning using GridSearchCV
- Model fitting with optimal alpha value
- Evaluation of feature selection capabilities

## Results Comparison

- Comparison of all three models using R2 score, RSS, and MSE
- Analysis of coefficient changes after regularization
- Ridge regression performed better in terms of R2 score and RSS compared to linear regression and lasso regression
- Lasso regression demonstrated effective feature selection by reducing some coefficients to zero

Key findings:
- The high correlation between price and variables like carwidth, curbweight, enginesize, and horsepower indicates that car size, weight, and engine power are strong predictors of price
- The negative correlation with mpg suggests that more economical cars tend to be cheaper
- The presence of multicollinearity among independent variables justifies the use of regularization techniques (Ridge and Lasso)

This project provides insights into the effectiveness of different regression techniques for car price prediction and demonstrates the impact of regularization on model performance and feature selection. It also highlights the importance of understanding variable relationships in predictive modeling.
