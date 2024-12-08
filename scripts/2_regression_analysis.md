# Welcome to: Regression Analysis 🙌🏾
Once completed, you will be able to:
- ✅ Estimate a simple regression function to model the relationship between consumption and disposable income.
- ✅ Visualize fitted consumption values and residuals using line graphs.

... so, let's get started! 👻

---
### Estimating a Simple, Bi-variate Linear Regression Function:
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
1. The $MPC$, Marginal Propensity of Consumption, is described as the amount by which consumption increases for each unitary increase in income. In other words, it is the gradient of the function, determined by the co-efficient of income: $\beta_1$ in our OLS estimated regression model.
   - In our regression on **STATA**, we can find this as the (estimated) co-efficient of income = `0.9260782`. This means, for every increase in income by 1 unit, consumption increases by `0.9260782`. This is our $MPC$. 

2. To determine the significance of our slope parameter, $\beta_1$, we need to look at the: t-tests and p-values.
   - For example, we observe that for our independent variable of income, the t-value is `105.10`. From statistical testing knowledge, we know that this is significant since it is very large and we are highly likely to have sufficient evidence whereby we can reject the null hypothesis. We can confirm this from carrying out a t-test using standard errors as follows:

   - $H_0: \beta_1 = 0$
   - $H_a: \beta_1 \neq 0$
   - This is a two-tailed test, so we must divide our significance level by 2, $0.025$.
   - Our $d.f$ = $n - 2 = 62 - 2 = 60$. Our t-value is $2.000$ (using t-tables from Dr Ercolani - my lecturer [here](Statistical_Tables.pdf)).
   - Our t-statistic: $t = \frac{\hat{\beta}_1 - \beta_1}{SE(\hat{\beta}_1)}$ and then substitute our values accordingly: $t = \frac{0.936 - 0}{0.00889} = 105.23$
   - 105.2 > 2.0
   - From this, we can conclude that the slope parameter is indeed significant. There is sufficient evidence to reject the null hypothesis.
   - From our p-values, we can conclude significance. Our significance level is assumed to be 5% = 0.005. The p-value is 0.000, which is lower than this. This tells us that income has a significant impact on our dependent variable consumption.
   

3. Mostly similar to question two, but in addition to that however, we can see that the confidence interval is relatively narrow. If you also pay attention, you can see the co-efficient lies within it. This suggests significance: we are 95% confident that the true value of our co-efficient lies within this range - if our estimated OLS co-efficient lies within this confidence band, it is likely that our true value does also. These all point to the same conclusion of significance.

4. We can use the R squared value to determine this. This equals 0.9946, in other words, over 99% of variation in consumption, can be explained by income. This suggests an almost perfect fit: the model almost always explains the variation in consumption (as caused by the independent variable of income)

- ✅ You have successfully modelled a regression function to estimate the relationship between consumption and income. Well done, keep going! 😄

---

### Visualising Fitted Values and Line Graphs: 😵‍💫
- Now, as econometricians (you are one if you're completing this!) we want to observe the fitted values of the dependent variable and their residuals. We do this because fitted values show how well our regression line matches the actual data. By plotting these against observed values, we can visually see how closely the model captures the relationship.

- We firstly need to generate two new variables, paste the following code into your `.do` file.
``` stata
predict fitted_consumption, xb
```
This will retrieve the fitted values.
``` stata
predict resids, residuals
```
This will retrieve the residuals.

Hint: Do not run the code yet - enter the next part I'm about to show you, then run it. 

If you've already run it, don't worry 🤪. Simply remove this code from your `.do` file and run again, as **STATA** has already generated the variables (you can see this in the right hand side of the main area). Re-running it without deletion of the `predict` code for the next part will produce an error.

We've now created two new variables within **STATA**. These are `fitted_consumption` and `resids`. Let's plot this so we can visualise the data.

``` stata
twoway (line consumption year)(line fitted_consumption year)(line resids year)
```

- What this does is create three lines with year as our indendepent variable. One for consumption, one for fitted consumption and another for our residuals. 

#### Your graph should look like this: [Click Here](Images_RA/Fitted_Consumption_Consumption_Resids_Line_Graph_RA.png)

How do we interpret this? 
  - As you can see, our consumption line is purple and represents the actual data for consumption over this time period. The 'linear predictions' blue line shows the values *predicted* by our regression model based on income. It closely follows our consumption data which tells us that this model estimated using OLS, fits our data very well. We would expect this, as our R squared value is very high. 🤯
  - Our green line of residuals shows the differences between our observed values of consumption, and our linear predicted values. They show the part of variation in consumption which is NOT explained by income. This is relatively small and stable around zero, suggesting that the model caputures most of our variation very well.
    
## ✅ Well Done! You've completed this section!



