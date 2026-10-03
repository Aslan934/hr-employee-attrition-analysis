# HR Employee Attrition Analysis

A Python-based exploratory data analysis project focused on understanding **employee attrition and the factors associated with employee turnover**.

The project analyzes a 10,000-employee HR dataset and investigates attrition across departments, job roles, overtime status, demographics, income, employee satisfaction, workload, experience, and other workplace-related characteristics.

The analysis also applies **Chi-Square testing and correlation analysis** to evaluate statistical relationships between employee characteristics and attrition.

---

## Project Overview

Employee attrition is an important HR and business challenge because high employee turnover can increase recruitment costs, reduce productivity, and affect organizational performance.

The objective of this project is to:

* Understand the overall employee attrition rate.
* Identify differences in attrition across departments and job roles.
* Analyze the relationship between overtime and employee turnover.
* Compare attrition across gender and marital status groups.
* Investigate attrition patterns across different age groups.
* Compare income levels between employees who left and remained with the company.
* Analyze employee satisfaction and work-life balance.
* Examine workload-related indicators such as project count, working hours, and absenteeism.
* Compare employee experience and tenure characteristics.
* Test whether department and attrition are statistically associated.
* Identify numerical variables that have stronger relationships with attrition.
* Translate analytical findings into practical HR recommendations.

---

## Dataset

The dataset contains **10,000 employee records** and **26 variables** describing demographic, professional, financial, satisfaction, workload, and employment characteristics.

### Dataset dimensions

* **Rows:** 10,000
* **Columns:** 26
* **Target variable:** `Attrition`

### Main variables

| Category                  | Variables                                                                                                                |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Employee Information      | `Employee_ID`, `Age`, `Gender`, `Marital_Status`                                                                         |
| Organization              | `Department`, `Job_Role`, `Job_Level`                                                                                    |
| Compensation              | `Monthly_Income`, `Hourly_Rate`                                                                                          |
| Experience                | `Years_at_Company`, `Years_in_Current_Role`, `Years_Since_Last_Promotion`                                                |
| Satisfaction              | `Work_Life_Balance`, `Job_Satisfaction`, `Work_Environment_Satisfaction`, `Relationship_with_Manager`, `Job_Involvement` |
| Performance & Development | `Performance_Rating`, `Training_Hours_Last_Year`                                                                         |
| Workload                  | `Overtime`, `Project_Count`, `Average_Hours_Worked_Per_Week`, `Absenteeism`                                              |
| Mobility                  | `Distance_From_Home`, `Number_of_Companies_Worked`                                                                       |
| Target                    | `Attrition`                                                                                                              |

The `Attrition` variable indicates whether an employee left the organization:

* `Yes` — employee left
* `No` — employee remained

---

## Data Cleaning

The dataset was checked for common data-quality issues before performing the analysis.

The following checks were performed:

* Missing-value analysis
* Duplicate row detection
* Duplicate `Employee_ID` detection
* Data-type inspection
* Column-name cleaning

### Cleaning results

The dataset contained:

* **0 missing values**
* **0 duplicate rows**
* **0 duplicate Employee IDs**

Therefore, no major missing-value or duplicate-record treatment was required.

---

# Analysis

## 1. Data Overview

The project begins with a general exploration of the dataset using:

* Dataset dimensions
* First records
* Column names
* Data types
* Descriptive statistics
* Missing-value inspection

This provides an initial understanding of the dataset structure before performing the attrition analysis.

---

## 2. Overall Attrition Analysis

The overall number of employees who left and remained with the company was calculated.

### Result

* Employees who left: **1,997**
* Employees who remained: **8,003**
* Overall attrition rate: **19.97%**

Approximately 80% of employees remained with the organization, while approximately 20% left.

---

## 3. Attrition by Department

Attrition rates were calculated for each department.

The analysis compares:

* Employee count by department
* Employees who left
* Employees who remained
* Department-level attrition rate

### Key finding

Department-level attrition rates were relatively close to each other.

* **Highest:** Finance — **20.85%**
* **Lowest:** Marketing — **19.36%**

The relatively small difference suggests that department alone does not strongly differentiate employees who leave from those who remain.

---

## 4. Attrition by Job Role

Attrition rates were calculated for each `Job_Role`.

This analysis helps identify whether particular job roles have noticeably higher employee turnover.

The results are visualized to make differences between roles easier to identify.

---

## 5. Overtime and Attrition

Employees were divided into:

* Employees who work overtime
* Employees who do not work overtime

Their attrition rates were compared.

### Key finding

The attrition rates were very similar:

* Overtime: **20.07%**
* No overtime: **19.87%**

Within this dataset, overtime status alone does not appear to create a substantial difference in attrition.

---

## 6. Gender and Marital Status

Attrition rates were analyzed across:

### Gender

The analysis compares attrition rates between male and female employees.

### Marital Status

Employees were also compared according to their marital status.

### Key finding

No large differences in attrition were observed across gender or marital-status groups.

These variables therefore appear to have relatively weak relationships with attrition in this dataset.

---

## 7. Age Group Analysis

Employees were divided into age groups to investigate whether attrition patterns vary across different stages of their careers.

The attrition rate was then calculated for each age group and visualized.

This provides a more interpretable view of employee turnover than analyzing age only as a continuous numerical variable.

---

## 8. Monthly Income Analysis

Monthly income was compared between:

* Employees who left
* Employees who remained

The project also analyzes average monthly income by:

* Department
* Attrition status

### Key finding

Monthly income showed very little relationship with attrition in this dataset.

Therefore, salary alone does not appear to be a strong explanation for employee turnover.

---

## 9. Employee Satisfaction Analysis

Three satisfaction-related indicators were analyzed:

* `Job_Satisfaction`
* `Work_Life_Balance`
* `Work_Environment_Satisfaction`

Average scores were compared between employees who left and employees who remained.

This analysis helps evaluate whether workplace satisfaction and employee experience may be related to turnover.

### Key finding

`Job_Satisfaction` was among the variables showing a statistical relationship with attrition in the analysis, although the practical differences between groups were not large.

---

## 10. Workload Analysis

The project investigates whether workload-related indicators differ between employees who left and employees who remained.

The following variables were analyzed:

* `Project_Count`
* `Average_Hours_Worked_Per_Week`
* `Absenteeism`

These variables were compared across attrition groups and visualized.

The objective is to determine whether workload or attendance patterns provide meaningful signals of employee turnover.

---

## 11. Experience and Tenure Analysis

Employee experience was examined using:

* `Years_at_Company`
* `Years_in_Current_Role`
* `Years_Since_Last_Promotion`

The analysis compares these variables between employees who left and employees who remained.

This helps investigate whether organizational tenure, role tenure, and time since promotion are associated with employee attrition.

---

# Statistical Analysis

## 12. Chi-Square Test

A **Chi-Square Test of Independence** was used to determine whether `Department` and `Attrition` are statistically associated.

### Hypotheses

**Null hypothesis (H₀):**

> Department and Attrition are independent.

**Alternative hypothesis (H₁):**

> Department and Attrition are associated.

### Results

| Statistic          | Result |
| ------------------ | -----: |
| Chi-Square         | 1.9323 |
| p-value            | 0.7482 |
| Degrees of Freedom |      4 |

Using a significance level of **0.05**:

`p-value = 0.7482 > 0.05`

Therefore, the null hypothesis is not rejected.

### Conclusion

There is **no statistically significant relationship between Department and Attrition** in this dataset.

---

## 13. Correlation Analysis

A correlation matrix was created for the relevant numerical variables.

A correlation heatmap was used to visualize relationships between variables.

The analysis specifically examined whether numerical variables have strong relationships with employee attrition.

### Key finding

No numerical variable demonstrated a strong correlation with attrition.

This suggests that employee attrition cannot be adequately explained by a single numerical factor.

Instead, multiple employee and workplace characteristics should be considered together.

---

# Key Findings

The main findings from the analysis are:

### 1. Overall attrition

The overall employee attrition rate is **19.97%**, with 1,997 employees leaving and 8,003 remaining.

### 2. Department

Department-level attrition rates are relatively similar.

Finance has the highest attrition rate at **20.85%**, while Marketing has the lowest at **19.36%**.

### 3. Overtime

Overtime and non-overtime employees have almost identical attrition rates:

* Overtime: **20.07%**
* No overtime: **19.87%**

### 4. Demographics

Gender and marital status do not show large differences in attrition rates.

### 5. Job role and satisfaction

Job Role and Job Satisfaction are among the variables that show statistical relationships with attrition, although the practical differences between groups are relatively small.

### 6. Income

Monthly Income has very little relationship with attrition.

### 7. Numerical variables

Correlation analysis indicates that no numerical variable has a strong relationship with attrition.

### 8. Department statistical test

The Chi-Square test indicates that Department and Attrition do not have a statistically significant relationship:

**p-value = 0.7482**

---

# Business Recommendations

Based on the findings, the following HR actions are recommended:

### 1. Monitor Job Role and Job Satisfaction

HR teams should regularly monitor job-role-specific attrition and employee satisfaction.

Roles with relatively higher attrition should be investigated to identify potential organizational or employee-experience issues.

### 2. Implement Regular Employee Feedback

Regular employee feedback surveys can help identify dissatisfaction before it results in employee turnover.

Potential approaches include:

* Employee engagement surveys
* Satisfaction surveys
* Manager feedback
* Career-development discussions
* Exit-interview analysis

### 3. Build an Attrition Risk Monitoring System

Instead of relying on a single variable, organizations can combine multiple indicators to identify employees who may have a higher risk of leaving.

Potential indicators include:

* Job satisfaction
* Job role
* Tenure
* Promotion history
* Workload
* Absenteeism
* Work-life balance
* Employee-manager relationship

This could eventually be developed into an HR analytics or machine-learning based employee attrition prediction system.

---

# Technologies & Libraries

The project was developed using Python and the following libraries:

* **Python**
* **Pandas** — data manipulation and analysis
* **NumPy** — numerical operations
* **Matplotlib** — data visualization
* **Seaborn** — statistical visualization
* **SciPy** — statistical testing

---

# Project Structure

```text
hr-employee-attrition-analysis/
│
├── data/
│   ├── employee_attrition_dataset_10000.csv
│   └── README.md
│
├── notebooks/
│   └── hr_analysis.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

### `data/`

Contains the dataset used for the analysis.

### `notebooks/`

Contains the complete Jupyter Notebook with the analysis, visualizations, statistical tests, and conclusions.

### `README.md`

Provides documentation, methodology, findings, and business recommendations.

### `requirements.txt`

Contains the Python dependencies required to reproduce the analysis.

---

# How to Run the Project

## 1. Clone the repository

```bash
git clone https://github.com/Aslan934/hr-employee-attrition-analysis.git
```

## 2. Navigate to the project

```bash
cd hr-employee-attrition-analysis
```

## 3. Install dependencies

```bash
pip install -r requirements.txt
```

## 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
notebooks/hr_analysis.ipynb
```

## 5. Run the notebook

Run the notebook cells sequentially to reproduce the analysis.

---

# Analytical Workflow

The project follows this general workflow:

```text
Raw HR Dataset
      ↓
Data Overview
      ↓
Data Cleaning
      ↓
Exploratory Data Analysis
      ↓
Attrition Analysis
      ↓
Employee Group Analysis
      ↓
Satisfaction & Workload Analysis
      ↓
Experience & Tenure Analysis
      ↓
Chi-Square Test
      ↓
Correlation Analysis
      ↓
Key Findings
      ↓
Business Recommendations
```

---

# Limitations

The analysis is primarily exploratory and statistical.

The findings should therefore be interpreted as **relationships observed in the dataset rather than proof of causation**.

In particular:

* A correlation does not imply causation.
* A single variable should not be used as a definitive explanation for employee turnover.
* Small differences in attrition rates may have limited practical significance even when statistical relationships exist.
* The analysis does not build a predictive machine-learning model.
* Further analysis could evaluate interactions between multiple employee characteristics.

---

# Future Improvements

Potential extensions of this project include:

* Building an employee attrition prediction model.
* Applying Logistic Regression, Random Forest, XGBoost, or other classification algorithms.
* Performing feature engineering.
* Encoding categorical variables.
* Evaluating feature importance.
* Using train/test splits and cross-validation.
* Comparing classification metrics such as Precision, Recall, F1-score, and ROC-AUC.
* Building an interactive Power BI dashboard.
* Creating an employee attrition risk scoring system.
* Developing an HR monitoring dashboard for management.

---

# Conclusion

This project demonstrates how Python-based data analysis can be used to investigate employee attrition and identify potential HR insights.

The analysis found an overall attrition rate of **19.97%**, while department-level differences were relatively small and Department was not statistically associated with Attrition according to the Chi-Square test.

The results also indicate that no single numerical variable strongly explains employee turnover. This supports a more holistic HR analytics approach in which multiple employee, workplace, satisfaction, workload, and career-development factors are considered together.

The project demonstrates practical skills in:

* Data cleaning
* Exploratory data analysis
* Group-based analysis
* Data visualization
* Statistical hypothesis testing
* Correlation analysis
* Business interpretation
* HR analytics
* Python data analysis

---

## Author

**Aslan Rustamov**

Data Analyst

GitHub: [Aslan934](https://github.com/Aslan934)

Project Repository: [hr-employee-attrition-analysis](https://github.com/Aslan934/hr-employee-attrition-analysis)
