# Time-Series Regression Analysis in Stata

This repository contains a detailed guide and Stata scripts to analyze the Keynesian consumption function using time-series data.

## How to Get Started

### Prerequisites
To follow along, you will need:
- **Stata**: Installed on your computer.
- **Workshop Dataset**: A time-series dataset containing UK economic variables (final consumption expenditure, disposable income, prices, and interest rates) from 1960 to 2021.

---

### Step 1: Download the Dataset
1. Click on `Workshops dataset.xlsx` to open the file preview.
2. Click the **Download** button (usually a downward arrow or "Download Raw" option) to save the file to your computer.

---

### Step 2: Import the Dataset into Stata
1. **Open Stata**.
2. Click on `File` → `Import` → `Excel Spreadsheet`. This will open the import dialog box.
3. Browse to the location where you saved `Workshops dataset.xlsx` and select the file.
4. In the import dialog:
   - Check the box **Import first row as variable names**.
   - Click **OK** to import the dataset.
5. Verify that the data has been imported correctly by:
   - Clicking on `Data Editor (Browse)` in Stata.
   - Ensuring that the columns (e.g., `year`, `consumption`, `income`) match the dataset.

---

### Step 3: Save the Dataset as a `.dta` File
To streamline future usage, save the imported dataset in Stata format:
1. In the command window, type:
   ```stata
   save "data/workshop_data.dta", replace

---

### Step 4: Begin to execute the '.do' files within 'scripts/' and get modelling!
1. Once you have downloaded the datasets and are ready to start writing out the necessary code, open your choice of `.do` file within the `scripts` directory. I reccommend working through the code in order of the `README.md` file within this repository.
2. There are **four** different files within `scripts`:
   - `1_explanatory_data_analysis.do`
   - `2_regression_analysis.do`
   - `3_data_transformation.do`
   - `4_testing_assumptions.do`
3. Work your way down each file within this directory. Each file has a set of instructions that will enable you to carry out the necessary statistical modelling. Start with the `1_explanatory_data_analysis.do` file within `scripts`: complete this first, and then move onto the next (`2_regression_analysis.do` etc. etc.)


