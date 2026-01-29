
---

##  1. Project Overview
The goal of this analysis is to:

- Clean and prepare the dataset  
- Analyze relationships between key variables  
- Validate findings using statistical hypothesis testing  
- Engineer meaningful features for future predictive modelling  

---

##  2. Data Loading

Initial data exploration included:  
- `df.head()`  
- `df.shape`  
- `df.info()`  
- `df.describe()`  

---

##  3. Data Cleaning

### a) Missing Values
- Calculated and analyzed missing value percentages  
- Dropped columns with **more than 40% missing values**  
- Filled missing values using:  
  - **Numeric columns → Median**  
  - **Categorical columns → Mode**

### b) Incorrect Values
- Converted negative day values using `.abs()`  
- Added **YEARS_DECISION** feature for easier interpretation  

✔ After cleaning, **100% of missing values were handled**

---

##  4. Outlier Detection & Removal

Outliers were removed using the **Interquartile Range (IQR)** method:

- `Q1` → 25th percentile  
- `Q3` → 75th percentile  
- `lower = Q1 - 1.5 * IQR`  
- `upper = Q3 + 1.5 * IQR`  
- Rows outside the bounds were filtered out  

---

##  5. Feature Engineering

| Feature | Description |
|--------|-------------|
| **CREDIT_ANNUITY_RATIO** | Ratio of approved credit to annuity |
| **APPLICATION_CREDIT_RATIO** | How close application amount is to approved credit |
| **IS_REFUSED** | Binary flag for refused loans |
| **IS_APPROVED** | Binary flag for approved loans |

---

##  6. Exploratory Data Analysis (EDA)

Visualizations included:

- Histograms + KDE plots  
- Boxplots  
- Countplots  
- Scatterplots  
- Correlation heatmap  

---

##  7. Statistical Hypothesis Testing

Performed to validate observed patterns:

### a) **Chi-Square Test**
Used to identify relationships between **categorical variables**

### b) **Two-Sample T-Test**
Compared means between different **customer groups**

---

##  Summary

This project provides a full EDA pipeline including data preparation, visualization, outlier treatment, feature generation, and hypothesis validation — preparing the dataset for further machine learning modeling.

---



