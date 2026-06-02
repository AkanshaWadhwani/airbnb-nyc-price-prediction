Airbnb NYC Price Prediction
Project Overview

This project predicts Airbnb listing prices in New York City using machine learning techniques. The study focuses on:

Data cleaning and preprocessing
Missing value treatment
Outlier handling
Feature engineering
Data leakage detection
Comparison of linear and nonlinear regression models

The objective is to evaluate how different modeling approaches perform on real-world rental pricing data.

Dataset

Airbnb NYC Open Data contains information such as:

Neighbourhood
Room type
Availability
Number of reviews
Minimum nights
Host information
Geographic location

Target Variable:
price

Project Workflow
1. Data Cleaning
Removed duplicate records
Handled missing values
Treated outliers
Corrected inconsistent data types
2. Exploratory Data Analysis
Distribution analysis
Correlation analysis
Feature relationships
Price trend visualization
3. Leakage Detection
Potential leakage features were identified and removed to ensure fair model evaluation.
4. Feature Engineering
Encoding categorical variables
Scaling numerical features
Feature selection
5. Model Building

Linear Models:

Linear Regression

Nonlinear Models:

Random Forest Regressor

6. Model Evaluation

Metrics:

Linear Regression:
R2: -0.0008153622930815452
RMSE: 332.01507273241964

Random Forest:
R2: 0.3540999046498957
RMSE: 266.7248582122049
The nonlinear models significantly outperformed linear models, demonstrating their ability to capture complex relationships in Airbnb pricing data.

Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn

Future Improvements
Hyperparameter tuning
Deployment using Streamlit
Geographic feature engineering
Ensemble methods
