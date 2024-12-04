Hello! 👋🏾

This repository contains my most pivotal demonstration of time-series data modelling - it follows on from my second-year, econometrics work conducted using **STATA** where it's specialisation is on the Keynesian Consumption Function.

Whilst we were tasked to carry out basic functions with knowledge from the first half of the semester (approx. October 2024), I expanded this task based on my completed knowledge of the Econometrics module as of December 2024, to further enhance statistical accuracy. I decided to create this project to represent my passion for how Econometrics can be used in real-world scenarios using real data.

My question will therefore be:

## What are the key determinants of consumption in the UK? An Econometric Study of Disposable Income, Prices, Interest Rates between 1960 and 2021. ###

This project will employ time-series analysis to assess the relationships between the indepdent variables of disposable income, prices, interest rates and the dependent variable, consumption, between 1960 and 2021. 
I will use data from the Office of National Statistics (ONS) and Bank of England - they are widely reliable for utilising standardised methodologies and being transparent within their data collection processes. Whilst riogourously standardised, their reliance on estimation techniques such as inflation-adjusted disposable income may create marginal measurement errors. Like every set of data, there is still potential for misspecification and bias, however, these sources are often used by researchers and policymakers, making it highly credible for econometric analysis despite these limitations.

Here we will thoroughly explore the dataset using descriptive statistics, data visualisations, 

I will thoroughly explore 




---

Whilst beneficial, the nature of this methodology causes certain limitations to arise. These include, but are not limited to:

#### Limited observations
- The dataset covers data only provides 62 observations - it restricts the statistical power in detecting any true effects. Hypothesis tests may fail to reject the null hypothesis despite a true relationships existent between variables. Whilst a larger sample is preferred, we will leverage this model's simplicity to focus on studying long-term trends without the extra noise usually seen in higher-frequency data. 
  
#### Autocorrelation in residuals of time-series data: 
- A very simplistic example of AC is that today's inflation is a function of yesterday's inflation, instead of today's inflation being independent of yesterday's. When AC exists, OLS produces a large variance, reducing the efficacy of our estimator in drawing reliable conculsions between any independent and dependent variables. When we scale our sample size to represent the population statistics, our estimates will not be very close to their true values like we want.
Since we want to evaluate all evantualities, we will test for AC using:
     - **Durbin-Watson test** (first-order autocorrelation).
     - **Breusch-Godfrey test** (higher-order autocorrelation)
And apply GLS to estimate, given ρ (our auto-correlation co-efficient) is known. If ρ is unknown, we will use:
     - **Cochrane-Orcutt procedure** to estimate a value of ρ through convergence.
After, we can apply OLS to obtain co-efficients closest to their true values (given our sample size)

#### Multicollinearity Amongst Indendent Variables:
- Disposable income, prices, interest rates etc. quite often are highly correlated and multi-collinear, affecting CLRA within OLS. We can identify this from contradictory t-statistics and R-squared values, alongside large standard errors. 
This *can* be problematic (not always): we would be unable to isolate impacts of individual predictors on the dependent variable (in this context, consumption) - preventing us from understanding which of our indepedent variabes directly affect consumption and whether or not certain independent variables are at all relevant.
We may often find variables are insignificant in affecting our dependent variable from the t-tests, yet contradictingly, observe signficance from the high R-squared values.

We cannot completely erradicate any multi-collinearity we may observe, especially due to our smaller sample size. It does not completely invalidate our model, but it is important to be transparent so one can interpret the results appropriately. 

#### Heteroscedacity:
- Though our sample size is smaller relative to many other data anlysis out there, it spans over a lengthy duration of time which may encourage the variance of error terms to differ over time.

#### Structural Breaks:

- Economic events may create structural breaks within the dataset. Think about it - the 2008 Financial Crisis was a global recession within out dataset of 1960 and 2021. It will have an effect on the independent variables we are testing - we can test for this using a:
    -**Chow Test**
#### Misspecification:

---

Why is having effective OLS useful?

We can highlight underlying trends between variables, faciliate economic interpretations which are potentially useful for policymakers and more easily identify any structural breaks or long-term growth patterns.

and draw conclusions such as how consumption may change in repsonse to a unit change in disposable income. This provides effective forecasting for consumer behaviour through economic parameters such as MPC, and validates Keynesian economics using real-world data, potentially allowing us to explore whether these traditional models need adjusting to contemporary economic conditions. 

---

Acknoledging limitations - why is this useful? What can this inform about future research?

What do I plan to do in the future should i acknowledge these limitations?

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

