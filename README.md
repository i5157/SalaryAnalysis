# Developer Salary Analysis: ROI of Education and Experience

## Project Motivation

This project provides a data-driven analysis of the factors influencing software developer compensation. Using the **2023 Stack Overflow Developer Survey**, I built a predictive model to quantify the financial impact of three specific career pillars:

1. **Experience:** The dollar value of each professional year in the industry.
2. **Education:** The ROI of a Master’s degree compared to a Bachelor’s.
3. **Environment:** The salary variance between Remote, Hybrid, and In-person work.

## Libraries Used

The following Python libraries were utilized for this analysis:

* **Pandas**: Data cleaning and feature engineering.
* **NumPy**: Numerical operations.
* **Matplotlib & Seaborn**: Data visualization.
* **Scikit-Learn**: Linear Regression modeling and evaluation.

---

## Data Preparation Summary

The dataset was cleaned and transformed using the following steps to ensure model integrity:

* **Handling Missing Values**: Rows with missing entries in key columns (`ConvertedCompYearly`, `YearsCodePro`, `EdLevel`, `RemoteWork`) were removed.
* **Salary Filtering**: Compensation was filtered to a range of **$20,000 to $250,000** to focus on professional full-time roles and remove extreme outliers.
* **Feature Engineering**:
* `YearsCodePro` was converted to numeric, handling "Less than 1 year" as **0** and "More than 50 years" as **51**.
* `Is_USA` was created to isolate the significant salary impact of the United States market.
* **One-Hot Encoding** was applied to `RemoteWork` and `EdLevel` for regression compatibility.



---

## Key Modeling Results

A Linear Regression model was trained with an **R-squared (Test) of 0.42**, indicating that these features explain approximately 42% of the variance in developer salaries.

**Model Intercept (Baseline):** $55,344.67

| Feature | Predicted Impact (USD) |
| --- | --- |
| **Is_USA** | +$65,346.63 |
| **EdLevel_Master's degree** | +$2,840.57 |
| **RemoteWork_Remote** | +$2,263.29 |
| **YearsCodePro (per year)** | +$1,663.14 |
| **RemoteWork_In-person** | -$11,593.83 |

---

## Summary of Results

### 1. Education ROI

Based on the visual analysis of the median salary, Bachelor’s degree holders in this specific subset show a higher median baseline. However, when controlling for experience and location in our regression model, a **Master's degree** provides a positive salary premium of approximately **$2,840**.

### 2. Work Environment & Experience

The data reveals a clear hierarchy in work environments. **Remote** roles sit at the top of the distribution with the highest median pay. Conversely, **In-person** roles suffer a significant "office penalty" of roughly **$11,593** compared to hybrid or remote counterparts. Furthermore, every year of professional experience adds an average of **$1,663** to a developer's annual salary.

---

## Files in the Repository

* **`SalaryAnalysis.ipynb`**: The primary Jupyter Notebook containing the data cleaning, EDA, and Linear Regression model.
* **`survey_results_public.csv`**: The original Stack Overflow 2023 survey dataset.(compressed for github reasons)
* **`README.md`**: Summary of the project findings and methodology.

## Acknowledgments

* **Data Source:** [2023 Stack Overflow Annual Developer Survey](https://insight.stackoverflowstackexchange.com/survey).
