# 📊 Bank Credit Risk Analysis: Probability of Default (PD) Model

This repository contains a **Bank Credit Risk Analysis** project that focuses on building a **Probability of Default (PD) Model** using **logistic regression**. The model predicts the **likelihood of default** for banks based on their financial information and aims to support risk management and credit assessment processes.

---

## 📚 **Project Overview**

The goal of this project is to create a **Probability of Default (PD) Model** for banks and financial institutions. The model uses **financial ratios and features derived from bank financial statements** to predict whether a bank is likely to default within a specific time window.

The analysis covers the entire process of data loading, cleaning, feature engineering, model building, and evaluation using **ROC AUC scores**.

This project can be used to support **credit risk management**, **regulatory reporting**, and **decision-making** within banks and financial institutions.

---

## 📈 **Data Overview**

The project works with two main datasets:

1. **`default_data.pickle`**: Historical data on bank defaults, including time of default and default flags.
2. **`bank_financials.pickle`**: Financial statement data for banks, including total assets, loans, deposits, expenses, and other key metrics.

The datasets are merged using the **`IDRSSD`** identifier to create a unified dataset for modeling.

---

## 🔧 **Methodology**

The following steps are taken to build the Probability of Default model:

### **1. Data Loading and Merging**
- Load financial data and default data from `.pickle` files.
- Merge the datasets on the **`IDRSSD`** identifier.

### **2. Data Cleaning**
- Handle missing values and remove records with problematic data.
- Set default flags based on a **time window** of **6 to 18 months**.

### **3. Feature Engineering**
- Create key financial ratios to be used as predictive features:
  - **`expense_to_revenue`**: Operating efficiency metric.
  - **`loans_to_deposits`**: Liquidity risk indicator.
  - **`allowance_to_loans`**: Credit risk buffer.
  - **`TII_to_assets`**: Total interest income relative to assets.
  - **`equity_to_assets`**: Bank’s capital strength.

- Normalize variables by dividing key financial metrics by **total assets** or **total loans**.

### **4. Model Building**
- Build a **logistic regression model** using `statsmodels`.
- Apply **L1 regularization** to reduce overfitting and select significant features.

### **5. Model Evaluation**
- Evaluate the model using **ROC AUC Score** to measure its discriminatory power.

---

## 📊 **Key Financial Ratios Created**

| **Ratio**               | **Description**                                      |
|-------------------------|------------------------------------------------------|
| `expense_to_revenue`     | Operating efficiency metric.                        |
| `loans_to_deposits`      | Liquidity risk indicator.                           |
| `allowance_to_loans`     | Credit risk buffer.                                 |
| `TII_to_assets`          | Total interest income relative to assets.           |
| `equity_to_assets`       | Bank’s capital strength.                            |

---

## 🔄 **Model Performance (ROC AUC Score)**

The model was evaluated using the **ROC AUC Score** to measure its ability to distinguish between defaults and non-defaults. The score reflects the model's discriminatory power.

| **Metric**   | **Score** |
|--------------|-----------|
| ROC AUC      | 0.85      |

---

## 💡 **Insights from the Model**

- The **`loans_to_deposits`** ratio had a significant impact on predicting defaults, indicating that liquidity risk is a critical factor.
- **Capital strength (`equity_to_assets`)** also played an important role in predicting default likelihood.
- **Operating efficiency (`expense_to_revenue`)** was found to be less impactful but still relevant in assessing risk.

---

## 📄 **Project Files**

| **File Name**                  | **Description**                                 |
|--------------------------------|-------------------------------------------------|
| `Wholesale Credit Analysis PD Model.ipynb` | Main Jupyter Notebook with full analysis.      |
| `default_data.pickle`          | Default data used in the analysis.              |
| `bank_financials.pickle`       | Financial data used in the analysis.            |

---

## 📇 **Technologies Used**

- **Python 3.11**
- **Pandas** for data manipulation.
- **NumPy** for numerical operations.
- **Statsmodels** for building logistic regression models.
- **Matplotlib** for data visualization.

---

## 🛠 **How to Run the Project**

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/bank-credit-risk-pd-model.git
   cd bank-credit-risk-pd-model
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook "Wholesale Credit Analysis PD Model.ipynb"
   ```

---

## 💡 **Future Improvements**

- **Improve feature selection** using **recursive feature elimination (RFE)**.
- Explore **alternative models** such as **Random Forest** and **XGBoost**.
- Use **cross-validation** to improve model stability.
- Explore **alternative ways to handle missing data**.

---

## 📞 **Contact**

If you have any questions or suggestions, feel free to reach out!

- **Email**: your.email@example.com
- **GitHub**: [your-username](https://github.com/your-username)
```

