# Explanatory Data Analysis 📈
By the end of this file, I am completely certain you will be able to:
  - ✅ Derive summary statistics to describe the dataset numerically.
  - ✅ Plot scatter and line graphs to visualise the data, and then explore any relationships between variables.
  - ✅ Demonstrate correlation numerically through summary statistics.

---

### Firstly, let's create a `Do-File`📝:
- By now, you should have already imported your data as per the instructions within `datasets`.
- Open **Stata** and open `Do-File Editor` (the pen and pencil icon in the top bar)
- Save the do file with your name of choice, I reccommend titling it `Explanatory_Data_Analysis.do` for easy access. Simply copy and paste the code within this file into **Stata** as you go along.
-  ###### Periodically ensure you save your titled `do-file` to avoid any losses! 😥

---
### Next, we shall calculate some summary statistics. 
1. Why? Calculating summary statistics helps us observe basic calculations within our dataset between a certain number of variables. If you wanted to obtain factors such as the sample size, the mean, standard deviation etc. - you would calculate a summary statistic to clearly derive simple conclusions within your data.
2. Suppose we wanted to observe the summary statistic of the independent variables `consumption` and `income`. We must paste the following code into the **Do-file** we just created:
   
   ```stata
   sum consumption income
    ```
   
3. The `sum` function is used before any of our independent variables (in this case, `consumption` and `income`) to calculate this. Note: this can be interchanged with any other variables within the dataset!
4. Save, and click `Execute`. View this in the main results window.
5. Your summary statistic should look something like this: [Click Here](Images_EDA/Summary_Statistics_EDA.png/)


### Bravo! Time to look at data correlation. 💡
1. If you want to observe how two variables are correlated, we use:
   
   ``` stata
   pwcorr consumption income
   ```
  
3. This will show a correlation matrix - the function `pwcorr` looks at the following variables (`comsumption`, `income`) to effectively evaluate and illutrate any correlations in a table.
4. Like before, click save and `Execute`. It will look like this: [Click Here](Images_EDA/Correlation_Matrix_EDA.png)

✅ You have successfully observed any correlation between variables.

### Let's get to plotting scatter and line graphs. 💻
1. Data Visualisation allows us to simplify very compelx data, and make it much easier to understand - we are going to look at plotting scatter and line graphs using our dataset so we can observe any relationships between variables more clearly.
2. So, we would usually want a time frequency on the x axis, with an appropriate scale for our data on the y axis. **Stata** will help us with the y axis, but we need to write a time frequency for the x axis. Given the data, let's do 'yearly'

   ``` stata
   twoway (line consumption year)(line income year)
   ```
3. In essence, `twoway` is the function that produces the line graph. `line consumption year` is the line corresponding to `consumption` measured across a yearly basis (hence, `year`). The same can be said for our `income` variable.
4. Save and `Execute` as per and you should get this: [View](Images_EDA/Scatter_Graph_EDA.png)

#### As you can see, the lines follow each other closely. 
#### Using your understanding of regression analysis - don't you think this is suggested by the data correlation values we coded and discovered earlier?

✅ Good job! 
