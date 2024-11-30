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
1. If you want to observe how two variable are correlated, we use:
   ``` stata
   pwcorr consumption income
   ```
2. This will show a correlation matrix, illustrating any correlations between variables.
3. Like before, save and `Execute`. It will look like this: [Click Here](

