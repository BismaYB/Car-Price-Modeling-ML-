# Car-Price-Modeling-ML-

## Project Overview

This project aims to model the pricing of cars in the American market using various regression techniques. The goal is to identify the significant factors influencing car prices, enabling a Chinese automobile company to strategically enter the U.S. market. The insights gained from this analysis will help the company adjust its design and business strategies to align with the preferences and pricing dynamics of American consumers.

## Dataset Description

Source: The dataset was collected by an automobile consulting firm through market surveys across the American market.
File: CarPrice_Assignment.csv

Target Variable: price - The selling price of the car.

Independent Variables: The dataset includes various features related to car specifications, such as:

Engine Type: Information about the type of engine (e.g., gas, diesel).
Horsepower: Engine horsepower.
Body Style: Car body type (e.g., sedan, hatchback).
Drive Wheel Configuration: Drive system of the car (e.g., front-wheel, rear-wheel).
Car Dimensions: Dimensions like length, width, and height.
Fuel System: Type of fuel system used in the car.

## 1. Data Loading and Preprocessing

Objective: Load and clean the dataset to prepare it for modeling.

Loading the Data: The dataset was loaded into a pandas DataFrame for easy manipulation and analysis.

Encoding Categorical Variables: Categorical variables were encoded using one-hot encoding to convert them into numerical format suitable for machine learning models.

Feature Scaling: All numerical features were scaled using StandardScaler to standardize the data, ensuring that features contribute equally to the model.

## 2. Model Implementation

Objective: Implement multiple regression models to predict car prices.

Linear Regression: A basic model to understand the linear relationship between the features and the target variable.

Decision Tree Regressor: A non-linear model that uses a tree-like structure to make predictions.

Random Forest Regressor: An ensemble learning method that builds multiple decision trees and merges them to improve accuracy.

Gradient Boosting Regressor: Another ensemble method that builds trees sequentially, where each tree corrects the errors of its predecessor.

Support Vector Regressor: A model that uses hyperplanes to predict the target variable with the goal of minimizing errors.

## 3. Model Evaluation

Objective: Compare the performance of all models using key evaluation metrics.

Evaluation Metrics:
R-squared (R²): Measures the proportion of the variance in the target variable that is predictable from the independent variables.

Mean Squared Error (MSE): Measures the average squared difference between the actual and predicted values.

Mean Absolute Error (MAE): Measures the average absolute difference between the actual and predicted values.

Findings:
Linear Regression: Showed poor performance, likely due to multicollinearity among features or the presence of outliers.

Decision Tree Regressor: Provided a decent R² score, but there were concerns about overfitting.

Random Forest Regressor: Demonstrated the best performance with the highest R² score and the lowest MSE and MAE, indicating a good fit to the data.

Gradient Boosting Regressor: Performed well, but slightly less accurate than Random Forest.

Support Vector Regressor: Underperformed with a negative R², indicating that the model did not fit the data well.

## 4. Feature Importance Analysis

Objective: Identify the significant variables affecting car prices.

RandomForestRegressor was used to compute feature importances based on how much each feature contributes to reducing the prediction error.

Visualization: A bar plot was created to visualize the top 10 most important features.
Findings:

Top Features: The most influential features included engine size, horsepower, curb weight, and highway mpg. These variables had the highest impact on predicting car prices.

## 5. Hyperparameter Tuning

Objective: Optimize the performance of the best-performing model (Random Forest Regressor) by tuning its hyperparameters.

Used GridSearchCV to explore a grid of hyperparameters, including:

Number of estimators (n_estimators)

Maximum depth of the trees (max_depth)

Minimum samples required to split an internal node (min_samples_split)

Minimum number of samples required to be at a leaf node (min_samples_leaf)

Whether bootstrap samples are used (bootstrap)

The model was cross-validated to ensure that the tuning process generalized well to unseen data.

Findings:
Best Parameters: The optimal hyperparameters were found, leading to an improved R² score and reduced errors on the test set.

Performance Gain: After tuning, the Random Forest model's performance on the test set showed a noticeable improvement in all key metrics.

Visualizations

Model Performance Comparisons:

Bar Plots: Visualized the R², MSE, and MAE for each of the five models, making it easy to compare their performance.
Feature Importance:

Bar Plot: Displayed the top 10 most important features in predicting car prices, highlighting key variables that should be prioritized in car design and pricing strategies.

## Conclusion and Insights

Best Model: The Random Forest Regressor emerged as the best model, accurately predicting car prices with an R² score of 0.953 after hyperparameter tuning.

Significant Variables: Key factors influencing car prices include engine size, horsepower, curb weight, and fuel efficiency (highway mpg). These insights can help the company design vehicles that meet market demands while optimizing pricing strategies.

Actionable Insights: The company can use these findings to adjust car designs, focusing on the identified significant features to appeal to the U.S. market and set competitive prices.
