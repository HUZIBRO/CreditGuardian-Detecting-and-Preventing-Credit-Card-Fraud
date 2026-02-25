# CreditGuardian – Detecting and Preventing Credit Card Fraud

This project provides a comprehensive **exploratory data analysis (EDA)** of credit card transactions, focusing on **spending patterns, customer behavior, and fraudulent transaction risks**. Using **supervised machine learning**, predictive models were built and evaluated to detect fraud, demonstrating proficiency in **data manipulation, visualization, and model evaluation** with Python.  

---

## 🔍 Project Objective  
The goal of **CreditGuardian** is to:  
- Understand customer transaction behavior  
- Identify patterns indicative of fraudulent activity  
- Build predictive models for credit card fraud detection and risk assessment  

---

## 📊 Business Insights: Key Drivers of Fraudulent Transactions

Based on exploratory data analysis, the following risk patterns were identified:

### 1️⃣ Bank-Level Exposure
Transactions associated with **Barclays Bank** show a relatively higher concentration of fraudulent activity, indicating potential exposure differences across issuing institutions.

### 2️⃣ Merchant Category Risk
The **Children Merchant Group** exhibits a disproportionately higher fraud incidence, suggesting that certain merchant segments may present elevated fraud vulnerability.

### 3️⃣ Transaction Channel Risk
**Online transactions** demonstrate a significantly higher fraud rate compared to other transaction types, reinforcing the increased risk associated with card-not-present environments.

### 4️⃣ Entry Mode Risk Indicator
Transactions processed using **CVC entry mode** are more frequently linked to fraudulent cases, indicating elevated risk in manual authentication scenarios.

### 5️⃣ Card Type Distribution
Fraud occurrences are more common among **Visa card transactions** within this dataset, which may reflect usage volume or exposure differences.

### 6️⃣ Transaction Amount Pattern
Fraudulent transactions tend to occur more frequently at **lower transaction amounts**, potentially reflecting fraudsters’ strategy to avoid detection through small-value testing transactions.

---
## 🤖 Modeling Approach  

To predict fraudulent transactions, two supervised machine learning models were implemented. Since the dataset was **highly imbalanced** (fraud cases representing a small minority), special attention was given to ensure the models properly learned from the minority class.

1️⃣ **Logistic Regression**  
A baseline linear model used to establish a benchmark for classification performance and interpretability.  
To address class imbalance, the `class_weight='balanced'` parameter was applied, allowing the model to assign higher importance to fraudulent (minority) transactions.

2️⃣ **Random Forest Classifier**  
An ensemble tree-based model designed to capture non-linear relationships and complex feature interactions within the data.  
Similarly, `class_weight='balanced'` was used to ensure the model focused more effectively on detecting fraudulent cases rather than being biased toward the majority class.
---

## 📊 Evaluation Strategy

Model performance was assessed using multiple classification metrics, including:  
- **Precision**  
- **Recall**  
- **F1-Score**  
- **ROC-AUC Score**  

Given the nature of fraud detection, **Recall was prioritized**, as failing to detect fraudulent transactions (False Negatives) can result in significant financial loss.  

To ensure model robustness and reduce overfitting risk:  
- **K-Fold Cross-Validation** was performed using **ROC-AUC** as the scoring metric.

---

## 🏆 Final Model Selection

Based on comparative evaluation using **Recall** and **ROC-AUC** metrics, the **Random Forest Classifier** was selected as the final model.  

It demonstrated superior ability to detect fraudulent transactions while maintaining balanced precision, making it the most suitable model for this credit fraud detection task.

---

## 💻 Tech Stack  

| Tool/Library     | Purpose                             |  
|------------------|-------------------------------------|  
| **Python**       | Programming language                |  
| **Pandas**       | Data manipulation & aggregation     |  
| **NumPy**        | Numerical computation               |  
| **Matplotlib**   | Static data visualization           |  
| **Seaborn**      | Statistical data visualization      |  
| **scikit-learn** | Machine learning modeling & evaluation |  

---
