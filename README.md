Here is the updated **README.md** content in full Markdown format, reflecting a single-notebook structure and the final results of your analysis.

---

# ## Developer Salary Analysis: ROI of Education and Experience

### ## Business Questions

This analysis focuses on three primary career pillars using the **2023 Stack Overflow Developer Survey**:

1. **Experience:** What is the specific dollar value of each year of coding experience?
2. **Education:** Is there a significant salary ROI for a Master’s degree over a Bachelor’s?
3. **Work Environment:** How does the "Remote Premium" compare to Hybrid and In-person roles?

---

### ## Data Preparation Summary

The cleaning and manipulation phase is complete. All data processing and modeling are contained within a single notebook.

#### **Feature Summary:**

* **Salary**: Filtered to a range of **$20,000 to $250,000** to focus on full-time professional compensation.
* **YearsCodePro**: Transformed from string-based survey responses into continuous numeric floats to represent professional experience.
* **Is_USA**: A binary feature engineered from the 'Country' column to capture the significant salary variance between the US and global markets.
* **RemoteWork**: Standardized into three categories: **Remote**, **Hybrid**, and **In-person**.
* **EdLevel**: Refined to a head-to-head comparison between **Bachelor’s** and **Master’s** degree holders.

#### **Data Integrity:**

All missing values (NaNs) were removed from these specific features, ensuring the model trained on a verified dataset. This resulted in a high-quality analysis of professional salary drivers.

---


### ## Project Structure

* **`SalaryAnalysis.ipynb`**: The primary Jupyter Notebook containing data cleaning, Exploratory Data Analysis (EDA), and the Linear Regression model.
* **`Data/survey_results_public.csv`**: Original dataset from Stack Overflow.(compressed for github reasons)
* **`README.md`**: Project documentation and summary of findings.

---

### ## Acknowledgments

* **Data Source:** This project utilizes the **2023 Stack Overflow Annual Developer Survey** dataset. Accessible through the [official insights page](https://insight.stackoverflowstackexchange.com/survey).
---
