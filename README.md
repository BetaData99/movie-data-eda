# movie-data-eda
IMDb Top 1000 Movies – Data Cleaning & Analysis

Project Overview:
This project explores the IMDb Top 1000 Movies dataset.  
The goal is to demonstrate skills in **data cleaning, exploratory data analysis (EDA), and visualization** using Python (Pandas, Matplotlib, Seaborn) and GitHub for project documentation.

Data Cleaning Process:
The raw dataset contained **missing values, inconsistent formats, and mixed data types**.  
I cleaned the data step by step in Jupyter Notebook:

1. **Released_Year**
   - Converted from text (e.g., `"2019 (I)"`) to numeric.
   - Coerced errors into `NaN` for consistency.

2. **Certificate**
   - Replaced invalid values (`16`, `"Passed"`) with `"Not Rated"`.
   - Filled missing entries with `"Not Rated"`.

3. **Runtime**
   - Removed `" min"` suffix.
   - Converted to numeric minutes.

4. **Meta_score**
   - Filled missing values with the mean.
   - Rounded to whole numbers (0–100 scale).

5. **Gross**
   - Stripped symbols (`$`, `,`, etc.).
   - Converted to numeric values.
   - Left missing values (`NaN`) in place to reflect films without reported earnings.

6. **No_of_Votes**
   - Kept raw integer values for analysis.
   - Created a display column with commas for readability (e.g., `10,562`).

7. **Duplicates**
   - Checked and removed any duplicate rows.

