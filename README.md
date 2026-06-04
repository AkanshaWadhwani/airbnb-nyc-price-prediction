# Airbnb NYC Price Prediction: Data Cleaning, Leakage Detection, and Model Comparison

## Overview

Predicting Airbnb listing prices is a common machine learning problem, but model performance can be heavily influenced by data quality and feature selection.

This project analyzes Airbnb Open Data for New York City and develops regression models to predict listing prices. Along the way, extensive data cleaning, missing value handling, feature engineering, and model evaluation were performed.

A key contribution of this project is the identification and removal of **data leakage**, demonstrating how seemingly strong model performance can be misleading when target-related information is unintentionally included.

---

## Dataset

### Source

Airbnb Open Data – New York City Listings

### Objective

Predict Airbnb listing prices using:

* Property characteristics
* Location information
* Host-related attributes
* Review statistics
* Availability metrics

---

## Project Workflow

### 1. Data Cleaning

Several data quality issues were identified and corrected:

* Removed duplicate records
* Handled invalid negative values
* Standardized categorical labels
* Converted string-based currency fields into numerical values
* Corrected inconsistent spellings

---

### 2. Missing Value Treatment

Different missing-value strategies were explored, including:

* Statistical imputation
* KNN imputation
* Median-based replacement

Missing values were handled based on the characteristics of each feature.

---

### 3. Feature Engineering

Feature engineering steps included:

* One-hot encoding categorical variables
* Creation of model-ready numerical features
* Removal of redundant attributes
* Preparation of features for regression models

---

### 4. Exploratory Data Analysis (EDA)

EDA was performed to understand:

* Price distributions
* Neighborhood trends
* Availability patterns
* Relationships between listing attributes and price

Visualizations were used to identify important trends and anomalies.

---

## Data Leakage Investigation

During model development, unusually strong performance was observed.

Further investigation revealed that the **Service Fee** variable was highly correlated with the target variable (Price), resulting in data leakage.

### Why This Matters

Data leakage occurs when information unavailable at prediction time is inadvertently used during training.

This can produce unrealistically optimistic results and reduce real-world model reliability.

To ensure a fair evaluation, the leakage-inducing feature was removed and all models were retrained.

---

## Models Evaluated

The following regression models were compared:

* Linear Regression
* Random Forest Regressor
* XGBoost Regressor

---

## Evaluation Metrics

Model performance was evaluated using:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score

These metrics provide insight into prediction accuracy and generalization capability.

---

## Key Findings

### Data Quality Matters

Cleaning inconsistent records and handling missing values significantly improved dataset reliability.

### Leakage Can Mislead Results

Including Service Fee produced unrealistically strong performance. Removing the leakage source resulted in more trustworthy evaluation metrics.

### Model Comparison

Tree-based models demonstrated stronger predictive capability than linear models, suggesting the presence of nonlinear relationships within the data.

### Location Remains Important

Neighborhood and property-related characteristics contributed substantially to listing price prediction.

---

## Skills Demonstrated

* Data Cleaning
* Exploratory Data Analysis
* Feature Engineering
* Missing Value Imputation
* One-Hot Encoding
* Regression Modeling
* Data Leakage Detection
* Model Evaluation
* Machine Learning Workflow Design

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* Jupyter Notebook

---

## Future Improvements

Potential future extensions include:

* Hyperparameter optimization
* Advanced feature engineering
* Geographic feature enrichment
* Ensemble modeling approaches
* Explainable AI techniques such as SHAP

---

## Author

Akansha Wadhwani

AIML Undergraduate Student
Symbiosis Institute of Technology, Pune

Interested in Machine Learning, Data Science, and building reliable AI systems through practical experimentation.
