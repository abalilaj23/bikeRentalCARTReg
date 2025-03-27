# Compare Regression with CART Predictor: BlueBike Rentals Case

## Introduction

This project analyzes BlueBike rental data using two predictive modeling techniques: Ordinary Least Squares (OLS) Regression and Classification and Regression Trees (CART). The goal is to compare their performance in predicting bike rentals based on various weather and temporal factors.

## Dataset

The dataset `rentals_weather.csv` contains 8,603 observations with the following attributes:

- **rentals**: Number of bikes rented (dependent variable)
- **month, day, hour, day_of_week, weekend**: Temporal features
- **temp, temp_wb, rel_humidity, windspeed, precipitation**: Weather-related features

## Methodology

### Data Preparation

- Categorical variables were converted to appropriate types.
- Data was split into training (70%) and testing (30%) sets.

### OLS Regression Model

- A multiple linear regression model was built using all predictors.
- The model achieved an Adjusted R² of 0.687 on training data.
- The Out-of-Sample R² (OSR²) on test data was 0.68.

### CART Regression Model

- A decision tree model was trained with default settings.
- The initial tree overfitted, achieving OSR² of 1.0 on training data and 0.78 on test data.
- Cost Complexity Pruning (CCP) was used to control overfitting.

## Key Findings

- The CART model initially overfitted but outperformed OLS regression on the test data when tuned.
- OLS regression provides interpretability, while CART captures complex patterns in the data.
- Further tuning of the decision tree (e.g., pruning, setting max depth) is necessary to balance bias-variance tradeoff.
