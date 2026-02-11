# Developer Salary Analysis: ROI of Education and Experience

## Business Questions
This analysis focuses on three primary career pillars using the 2023 Stack Overflow Developer Survey:
1. **Experience:** What is the specific dollar value of each year of coding experience?
2. **Education:** Is there a significant salary ROI for a Master’s degree over a Bachelor’s?
3. **Work Environment:** How does the "Remote Premium" compare to Hybrid and In-person roles?

---

## Final Data Preparation Summary

The cleaning and manipulation phase is now complette. 

### Feature Summary:
* **Salary**: Filtered to a range of $20,000 to $250,000 to focus on full-time professional compensation.
* **YearsCode**: Transformed from a string-based survey response into a continuous numeric float.
* **Is_USA**: A binary feature engineered from the original 'Country' column. This simplifies the model while capturing the significant salary difference between the United States and other global markets.
* **RemoteWork**: Standardized into three clean categories: **Remote**, **Hybrid**, and **In-person**. This allows for the quantification of the "Remote Premium" or "In-person Discount."
* **EdLevel**: Refined to a head-to-head comparison between **Bachelors** and **Masters** degree holders, directly addressing the research question regarding the ROI of a higher degree.

### Data Integrity:
I have removed all missing values (NaNs) from these specific features, ensuring that the final model trains on a complete and verified dataset. The result is a high-quality CSV file ready for statistical modeling and visualization.

---

## Key Modeling Results
After training a Linear Regression model (R-squared: 0.40), the following feature impacts were identified:

* **Is_USA**: +$65,634.72
* **RemoteWork_Remote**: +$3,609.01
* **EdLevel_Masters**: +$2,184.44
* **YearsCode**: +$1,421.95 (per year)
* **RemoteWork_In-person**: -$12,049.58

---

## Project Structure
* `data.ipynb`: Notebook 1 (Cleaning and EDA)
* `model.ipynb`: Notebook 2 (Modeling and Results)
* `cleanData.csv`: Final cleaned dataset
* `survey_results_public.csv`: original dataset
* `README.md`: Project documentation

---

## Acknowledgments

* **Data Source:** This project utilizes the **2023 Stack Overflow Annual Developer Survey** dataset. The data is provided by Stack Overflow and is accessible through their [official insights page](https://insight.stackoverflowstackexchange.com/survey).
* **Project Framework:** This analysis was developed as part of the **Udacity Data Science Nanodegree** program, following the CRISP-DM methodology for data science projects.