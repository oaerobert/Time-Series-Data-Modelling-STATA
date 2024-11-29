# Regression Analysis 🦋
This repository contains my econometrics work conducted using **STATA**, focusing on analyzing the Keynesian consumption function. The dataset consists of annual data from the UK for the period **1960 to 2021**, with variables such as:

- Final consumption expenditure
- Disposable income
- Prices
- Interest rates

This is **time series data**, and the analysis aims to explore and demonstrate statistical techniques and tests used in econometrics.

---

## Key Objectives and Workflow

### 1. **Exploratory Data Analysis (EDA)**
   - Derive summary statistics to describe the dataset numerically.
   - Plot scatter and line graphs to visualize the data and explore relationships between variables.
   - Demonstrate correlation numerically through summary statistics.

### 2. **Regression Analysis**
   - Estimate a simple regression function to model the relationship between consumption and disposable income.
   - Visualize fitted consumption values and residuals using line graphs.

### 3. **Data Transformation**
   - Transform data using logarithms for better model interpretation.
   - Run multiple regressions and compare the results with manual calculations to verify the program's outputs.

### 4. **Testing Assumptions of Classical Linear Regression**
   - Examine what happens when the assumptions of the classical linear regression model are violated.

#### **Autocorrelation**
   - Test for autocorrelation in residuals using:
     - **Durbin-Watson test** (first-order autocorrelation).
     - **Breusch-Godfrey test** (higher-order autocorrelation).
   - Estimate the coefficient of autocorrelation using:
     - **Cochrane-Orcutt procedure**.
     - **Prais-Winsten method** (to retain initial observations).
   - Address false autocorrelation:
     - Add a lag of the dependent variable.
     - Test again with **Breusch-Godfrey** to check for significance.

#### **Heteroscedasticity**
   - Test for heteroscedasticity of the error term using:
     - **White's test**.
     - **Breusch-Pagan test**.
   - Demonstrate how the test regression is constructed using the dependent variable, regressors, and their products.

---

## Purpose
The purpose of this project is to:
- Assess the efficiency and validity of the **Ordinary Least Squares (OLS)** method when the classical linear regression assumptions are met or violated.
- Understand and demonstrate the impact of violations such as autocorrelation and heteroscedasticity on the efficiency of regression estimates.
- Show how to address these violations using statistical methods and transformations.

---

## Tools
This project uses:
- **STATA** for data analysis and visualization.
- Econometric techniques to evaluate the Keynesian consumption function and assess the validity of classical regression assumptions.
- Simply follow the folders, starting with 'data' to perform this time-series-modelling.

---

Feel free to clone, explore, and provide feedback or suggestions for further improvements. This repository is a demonstration of econometric concepts and their application to real-world data.
