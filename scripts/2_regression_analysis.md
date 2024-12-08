# Welcome to: Regression Analysis 🙌🏾
Once completed, you will be able to:
- ✅ Estimate a simple regression function to model the relationship between consumption and disposable income.
- ✅ Visualize fitted consumption values and residuals using line graphs.

... so, let's get started! 👻

---
### Estimating a simple, bi-variate linear regression function:
- Our aim is to estimate the parameters in a consumption function of the form:
### $consumption_{t} = \beta_0 + \beta_1 \text{income}_t + \epsilon_t$

#### Like with the previous task, create a new `.do` file: ideally titled 'Regression Analysis' in **STATA**

- To create this, we need to ensure our first variable (consumption) is defined as a dependent variable. By default, **STATA** includes a constant term $\beta_0$ in the regression. This acts as our 'y-intercept' as with the traditional $y = mx +c$

Type the following code into your `.do` file:
``` stata
reg consumption income
```
This regresses our dependent variable, consumption, on our independent variable, income. You will produce a table that looks like this: [Click Here](Images_RA/Consumption_Income_Regression_RA.png)

Now, let's dive deeper into the analysis of this data. I will create some questions, and at the end of the section, are their corresponding answers. Take some time to think about it before having a look. 👀

---

#####  1. What do the results say about our $MPC$ for this dataset?
#####  2. Is the slope parameter significant? What does that say about how income determines consumption?
#####  3.  Can you see how t-statistics, their P-values and their 95% confidence bands tell the same story about significance?
#####  4. What proportion of the variation in consumption, is explained by variation in income?

---

Answers: 🎓
1. The $MPC$, Marginal Propensity of Consumption, is described as the amount by which consumption increases for each unitary increase in income. In other words, it is the gradient of the function, determined by the co-efficient of income: $\beta_1$ in our regression model.
   - In our regression on **STATA**, we can find this as the co-efficient of income = `0.9260782`. This means, for every increase in income by 1 unit, consumption increases by `0.9260782`. This is our $MPC$. 

2. To determine the significance of our slope parameter, $\beta_1$, we need to look at the: t-test, R-squared, Adj R-Squared and p-values, alongside the realistic scope of the confidence bands.
   - For example, we observe that for our independent variable of income, the t-value is `105.10`. From statistical testing knowledge, we know that this is significant since it is very large and we are highly likely to reject the null hypothesis. However we can confirm this from carrying out a t-test using standard errors as follows:
   - $H_0: \beta_1 = 0$
   - $H_a: \beta_1 \neq 0$
   - This is a two-tailed test, so we must divide our significance level by 2 to determine the t value. D.f = n-1 = 61. Our t-value is 2.000 (using t-tables, from my lecturer's materials, [here:](Statistical_Tables.pdf))


