Hello! 👋🏾

This repository contains my most pivotal demonstration of time-series data modelling - it follows on from my second-year, econometrics work conducted using **STATA** where it's specialisation is on the Keynesian Consumption Function.

Whilst we were tasked to carry out basic functions with knowledge from the first half of the semester (approx. October 2024), I expanded this task based on my completed knowledge of the Econometrics module as of December 2024, to further enhance statistical accuracy. I decided to create this project to represent my passion for how Econometrics can be used in real-world scenarios using real data.

### What are the key determinants of consumption in the UK? An Econometric Study of Disposable Income, Prices, Interest Rates between 1960 and 2021. ###

This project will employ time-series analysis to assess the relationships between the independent variables of disposable income, prices, interest rates and the dependent variable, consumption, between 1960 and 2021. 


## Key Objectives and Workflow

### 1. **Exploratory Data Analysis (EDA)**
   - ✅ Derive summary statistics to describe the dataset numerically.
   - ✅ Plot scatter and line graphs to visualise the data, and then explore any relationships between variables.

### 2. **Regression Analysis**
   - ✅ Estimate a simple regression function to model the relationship between consumption and disposable income.
   - ✅ Visualize fitted consumption values and residuals using line graphs.

### 3. **Data Transformation**
   - ✅ Transform data using logarithms for better model interpretation.
   - ✅ Run multiple regressions and compare the results with manual calculations to verify the program's outputs.

### 4. **Testing Assumptions of Classical Linear Regression**
   - ✅ Examine what happens when the assumptions of the classical linear regression model are violated.

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

---
## How to get started.
1. Open the `datasets` folder within this repository.
2. Start with the `raw_dataREADME.md` file - it has a list of instructions on how to get started

