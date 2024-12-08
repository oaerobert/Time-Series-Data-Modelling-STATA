# Welcome to: Regression Analysis 🙌🏾
Once completed, you will be able to:
- ✅ Estimate a simple regression function to model the relationship between consumption and disposable income.
- ✅ Visualize fitted consumption values and residuals using line graphs.

... so, let's get started! 👻

---
### Estimating a simple, bi-variate linear regression function:
Our aim is to estimate the parameters in a consumption function of the form:
### $consumption_{t} = \beta_0 + \beta_1 \text{income}_t + \epsilon_t$

#### Like with the previous task, create a new `.do` file: ideally titled 'Regression Analysis' in **STATA**

To create this, we need to ensure our first variable (consumption) is defined as a dependent variable. By default, **STATA** includes a constant term $\beta_0$ in the regression. This acts as our 'y-intercept' as with the traditional $y = mx +c$

Type the following code into your `.do` file:
``` stata
reg consumption income
```
This regresses our dependent variable, consumption, on our independent variable, income. You will produce a table that looks like this: [Click Here](Images_RA/Consumption_Income_Regression_RA.png)

