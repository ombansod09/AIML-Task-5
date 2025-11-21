# AIML-Task-5
# Heart Disease Prediction: A Comparative Analysis of Tree-Based Models

**Project Status:** Completed
**Domain:** Healthcare Analytics / Machine Learning

## 1. Project Overview
This repository contains a machine learning pipeline designed to predict the incidence of heart disease based on lifestyle factors. The project focuses on the application and comparison of two supervised learning algorithms: **Decision Trees** and **Random Forests**.

The primary objective is to demonstrate the trade-offs between model interpretability and predictive performance (bias-variance trade-off) in a regression setting using real-world data.

## 2. Dataset Description
The analysis utilizes the `heart.data.csv` dataset.
* **Target Variable (`heart.disease`):** A continuous variable representing the severity or risk rate of heart disease.
* **Features:**
    * `biking`: Percentage of the population that bikes.
    * `smoking`: Percentage of the population that smokes.

## 3. Methodology

### 3.1 Data Preprocessing
* Data ingestion using Pandas.
* Feature selection and separation of target variables.
* Train-Test split (80/20 ratio) to ensure robust model evaluation.

### 3.2 Model Development
Two distinct models were developed for comparative analysis:
1.  **Decision Tree Regressor:** Configured with a maximum depth of 3 (`max_depth=3`) to mitigate overfitting and enhance interpretability.
2.  **Random Forest Regressor:** An ensemble of 100 decision trees (`n_estimators=100`) utilized to improve generalization and reduce variance through bootstrap aggregating (bagging).

### 3.3 Evaluation Metrics
Models were evaluated using:
* **Mean Squared Error (MSE):** To quantify the average squared difference between estimated values and the actual value.
* **R-squared ($R^2$):** To determine the proportion of variance in the dependent variable that is predictable from the independent variables.
* **5-Fold Cross-Validation:** Performed on the Random Forest model to validate stability.

## 4. Key Findings

### Model Performance
* **Decision Tree:** Provided a baseline for prediction. While highly interpretable, it exhibited limitations in capturing complex non-linear patterns compared to the ensemble method.
* **Random Forest:** Demonstrated superior performance with a lower Mean Squared Error (MSE). The ensemble approach effectively neutralized the individual biases of single trees.

### Feature Importance
Analysis of the Random Forest feature importance scores revealed:
* **Smoking:** Positive correlation with heart disease rates (Primary Risk Factor).
* **Biking:** Negative correlation with heart disease rates (Primary Mitigating Factor).

## 5. Project Structure
```bash
├── heart.data.csv          # Dataset
├── analysis.py             # Source code for training and visualization
├── output_tree.png         # Visualization of the Decision Tree
├── output_importance.png   # Feature Importance Plot
└── README.md               # Project documentation
