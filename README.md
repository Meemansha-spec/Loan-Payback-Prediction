
# Credit Risk Dataset Analysis

## Overview

This project is about **analyzing the loan dataset in order to gain insights about the borrowers and understand the factors that are associated with loan default risk**. This analysis is about **performing exploratory data analysis (EDA) on the loan dataset and preparing the features for modeling**.

The process involves **data cleaning, outlier handling, checking for multicollinearity, and categorical variable selection** in order to ensure that the data is in the correct state before building reliable credit risk models.

---

# Description of the Data Set

This data set contains **information about the customer's demographics, financial information, and loan information** in order to **analyze the risk of loan repayment or default**.

The features in the data set include:

* Demographics of borrowers (age, education, marital status, gender)
* Financial information (income, debt-to-income ratio, credit score)
* Loan information (loan amount, interest rate, loan term, installment)
* Credit behavior (delinquencies, credit limit, account balance)
* Employment status and loan purposes

The target variable is **whether the customer defaulted on the loan or not**.

---

# Project Workflow

## 1. Data Upload and Initial Exploration

The data set is **uploaded into the workspace and initial exploration is done in order to understand the structure of the data and the features in the data set**.

Some of the **initial exploration techniques include inspecting the data set's dimensions, checking for missing values, understanding the data types, and understanding the features in the data set**. Some **visualizations are also done in order to understand the patterns in the data set**. Some of the visualizations include income distributions, loan amount distributions, credit score distributions, and default risk distributions.

---

## 2. Outlier Treatment using Winsorization

Financial data sets are prone to **extreme values in the data sets, and it is important to handle these values in order to obtain reliable results**.

To resolve this problem, **winsorization** was applied to specific numerical features. Winsorization limits extreme values by setting them to specific percentile limits.

Benefits of winsorization:

* It reduces extreme values
* It does not reduce the number of data points
* It stabilizes statistical calculations

---

## 3. Detection of Multicollinearity Using Correlation Matrix

A **correlation matrix** was applied to examine relationships between numerical features.

Highly correlated features are said to **contain redundant information**. These features may impair statistical model performance.

Steps applied:

* Calculated correlations between numerical features
* Identified features that are strongly correlated with each other (correlation = ±1)
* Examined features that may exhibit redundancy

---

## 4. Variance Inflation Factor Analysis

To detect **multicollinearity** between features, **Variance Inflation Factor** was calculated for all numerical features.

**Variance Inflation Factor** measures how strongly each feature is explained by other features.

Results interpretation:

| VIF Value | Interpretation             |
| --------- | -------------------------- |
| < 5       | Low multicollinearity      |
| 5-10      | Moderate multicollinearity |
| > 10      | High multicollinearity     |

Features with very high values of **Variance Inflation Factor** are removed.

---

## 5. Categorical Feature Selection Using Chi-Square Test

**Chi-Square Test of Independence** was applied to categorical features. It examines whether categorical features are statistically significantly associated with the target variable, **loan default**.

This test helps identify categorical features that are important in predicting **loan default**.

Two values are calculated:

* **p-value** - Determines statistical significance
* **Cramér’s V** - Determines strength of association

Features with strong relationships were kept for further analysis.

---

# Key Outcomes

After the preprocessing, the data set was further refined through the following processes:

* Reduction of the effect of extreme outliers
* Deletion of highly correlated numerical features
* Deletion of redundant features using VIF
* Selecting relevant categorical variables using statistical tests

This resulted in a clean and structured data set ready for predictive modeling.

---

# Tools and Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy
* Statsmodels

---

# Future Work

Possible future work for this project includes:

* Feature engineering
* Risk segmentation
* Development of machine learning models for default prediction
* Evaluation of the models using metrics such as AUC, KS statistic, and Confusion matrix
* Development of a credit risk scorecard
