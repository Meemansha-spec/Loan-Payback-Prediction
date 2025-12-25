# Loan-Payback-Prediction
How can we identify borrowers who are likely to repay their loans versus those who are at risk of default, using available financial and demographic data?

# Loan Payback Prediction – Business & Risk Analysis

## 1. Business Understanding

### 1.1 Business Context
Financial institutions provide loans to customers with diverse financial backgrounds, employment stability, and credit histories. 
While lending generates revenue through interest, loan defaults pose a significant financial risk to the institution.

The core challenge for lenders is to strike a balance between:
- Maximizing profitability by approving loans, and  
- Minimizing credit risk caused by borrower defaults.

This project analyzes historical loan data to understand repayment behavior and identify key risk drivers that influence loan payback outcomes.

---

### 1.2 Business Problem Statement
The objective of this analysis is to answer the following question:

**How can we identify borrowers who are likely to repay their loans versus those who are at risk of default using available financial and demographic data?**

This is a **decision-support problem**, not just a prediction task, where incorrect decisions have direct financial consequences.

---

### 1.3 Target Variable
- **Target Column:** `loan_paid_back`
  - `1` → Loan paid back  
  - `0` → Loan not paid back (default)

This represents a binary classification problem with asymmetric risk.

---

### 1.4 Business Impact of Misclassification

In real-world lending, different types of errors have unequal costs:

| Error Type | Business Impact |
|----------|-----------------|
| False Positive (Risky borrower approved) | Direct financial loss, increased non-performing assets |
| False Negative (Safe borrower rejected) | Lost revenue and potential customer dissatisfaction |

Due to this imbalance, accuracy alone is not an appropriate evaluation metric for this problem.

---

### 1.5 Business Objectives
This analysis aims to support the following objectives:

1. **Risk Identification**  
   Identify borrower attributes associated with higher default risk.

2. **Portfolio Risk Assessment**  
   Understand how default risk varies across income levels, credit scores, employment status, and loan purposes.

3. **Policy Guidance**  
   Provide analytical insights to guide loan approval criteria and risk-based pricing strategies.

4. **Explainability & Trust**  
   Ensure findings are interpretable and statistically validated for stakeholder decision-making.

---

### 1.6 Key Business Questions
The analysis seeks to answer the following questions:

- How does credit score influence loan repayment behavior?
- Does a higher debt-to-income ratio significantly increase default risk?
- Are certain loan purposes associated with higher default rates?
- How do employment status and education level affect repayment outcomes?
- Are interest rates adequately compensating for borrower risk?

---

### 1.7 Key Metrics (KPIs)

**Portfolio-Level Metrics**
- Overall default rate
- Average loan amount
- Average interest rate

**Risk Metrics**
- Default rate by credit score band
- Default rate by income bracket
- Default rate by employment status
- Default rate by loan purpose

**Model Evaluation Metrics**
- ROC-AUC
- Precision and Recall
- False Positive and False Negative rates

Accuracy is intentionally avoided due to class imbalance and unequal misclassification costs.

---

### 1.8 Analytical Assumptions
- Historical repayment behavior is indicative of future default risk.
- Borrower attributes are accurately reported.
- The dataset represents a stable lending environment without major economic disruptions.

---

### 1.9 Constraints & Limitations
- No time-based repayment history is available.
- Behavioral transaction data is not provided.
- Analysis is based on a static snapshot of borrower information.

These constraints influence model selection and interpretation of results.

---

### 1.10 Success Criteria
The analysis is considered successful if:
- High-risk borrower segments are clearly identified.
- Risk drivers are statistically validated.
- Models demonstrate strong discriminatory power (ROC-AUC).
- Insights are interpretable and actionable.
- Findings can be effectively communicated to stakeholders through visual analytics.

---

### 1.11 Research Perspective
This project approaches loan default prediction from a **research and decision-science perspective**, emphasizing:
- Statistical rigor  
- Interpretability  
- Risk-aware evaluation  
- Business-aligned insights  

Rather than focusing solely on predictive performance, the goal is to generate reliable, explainable, and actionable credit risk insights. 
