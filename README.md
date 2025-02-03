# Machine-Learning: Regression Analysis
# 🔷 Predicting Power Plant Energy Output Using Regression and KNN

## 🔷 Project Overview
This project analyzes the **Combined Cycle Power Plant** dataset to predict the net hourly electrical energy output (EP) using **linear regression** and **KNN regression**. The dataset includes ambient environmental variables such as **temperature (T), pressure (AP), humidity (RH), and exhaust vacuum (V)**.

---

## 🔷 Dataset Description
The dataset consists of **hourly observations** collected from a power plant over **six years (2006-2011)** when operating at full load. It includes the following features:
- **Temperature (T)** - Ambient temperature in °C
- **Ambient Pressure (AP)** - Pressure in millibar
- **Relative Humidity (RH)** - Percentage of humidity
- **Exhaust Vacuum (V)** - Steam exhaust vacuum pressure
- **Net Electrical Output (EP)** - The target variable, representing the energy output in MW

**Source:** [UCI Machine Learning Repository - Combined Cycle Power Plant Dataset](https://archive.ics.uci.edu/ml/datasets/Combined+Cycle+Power+Plant)

---

## 🔷 Libraries Used
The following Python libraries were utilized for analysis and modeling:
- `numpy` - Numerical operations
- `pandas` - Data manipulation
- `matplotlib` & `seaborn` - Data visualization
- `sklearn` - Machine learning models (Linear Regression, KNN)
- `scipy.stats` - Statistical analysis
- `statsmodels.api` - Regression modeling

---

## 🔷 Steps Taken to Accomplish the Project

### 🔶 1. Data Preprocessing and Exploratory Data Analysis (EDA)
- Loaded and explored the dataset to understand variable distributions.
- Checked for missing values and performed data cleaning.
- Visualized relationships between features using **pairwise scatterplots**.
- Computed **summary statistics** (mean, median, quartiles) for all variables.

### 🔶 2. Simple Linear Regression Analysis
- Fitted **individual linear regression models** for each predictor against `EP`.
- Identified **statistically significant** predictors based on p-values.
- Analyzed **outliers and leverage points** affecting the regression models.

### 🔶 3. Multiple Linear Regression Analysis
- Built a multiple regression model using **all four predictors**.
- Performed hypothesis testing to check if predictors significantly contribute to the model.
- Compared **univariate regression coefficients** with multiple regression coefficients.
- Created a **coefficient comparison plot** to visualize changes.

### 🔶 4. Nonlinear & Interaction Effects Analysis
- Examined **nonlinear relationships** by fitting polynomial regression models.
- Evaluated the significance of adding **quadratic and cubic terms** to each predictor.
- Tested for **interaction effects** between predictors and their impact on `EP`.

### 🔶 5. Model Refinement & Performance Evaluation
- Split the dataset into **70% training and 30% test**.
- Removed **insignificant predictors** based on p-values.
- Trained and tested the final multiple regression model.
- Reported **Mean Squared Error (MSE)** for training and test sets.

### 🔶 6. K-Nearest Neighbors (KNN) Regression
- Implemented **KNN regression** with normalized and raw features.
- Optimized the **value of k** by evaluating test errors for `k ∈ {1, 2, ..., 100}`.
- Plotted **test error vs. 1/k** to determine the best performing model.

### 🔶 7. Comparison of KNN and Linear Regression
- Compared **test errors** between **KNN regression and multiple linear regression**.
- Analyzed the performance of different models for power plant energy prediction.

---

## 🔷 Key Findings
- **Temperature (T)** had the strongest negative correlation with energy output.
- **Exhaust Vacuum (V)** had a significant nonlinear relationship with `EP`.
- Adding **interaction terms and polynomial features** improved regression accuracy.
- **KNN regression with optimal k** performed competitively with linear regression but was more sensitive to feature scaling.
- **Linear regression** remained interpretable and performed well without requiring hyperparameter tuning.

---

## 🔷 Conclusion
- The **multiple linear regression model with interaction terms** provided the **best predictive performance**.
- **KNN regression** offered comparable accuracy but required careful selection of `k` and feature scaling.
- **Polynomial regression and interaction terms** captured complex relationships in the data.

---
