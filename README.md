# 💳 Credit Card Fraud Detection

## 📌 Project Overview
Credit card fraud accounts for less than 0.2% of transactions but causes significant financial losses annually. This project builds a **Machine Learning model** to detect fraudulent transactions with **high recall** while minimizing false alerts, using the well-known Credit Card Fraud dataset.

---

## 📊 Business Problem
Banks and financial institutions face:
- High financial loss from undetected fraud
- High operational costs from false positives
- Need for a balanced solution that maximizes fraud detection while reducing false alerts

---

## 🎯 Objective
- Build a model to **maximize recall** (catch most fraud cases)
- Optimize **precision** to reduce unnecessary manual reviews
- Recommend deployment threshold for production

---

## 🗂 Repository Structure

---

## ⚙️ Steps & Methodology
1. **Exploratory Data Analysis**
   - Checked class imbalance
   - Scaled `Amount` and `Time`
   - Prepared clean dataset

2. **Modeling**
   - Logistic Regression with `class_weight=balanced`
   - Evaluated metrics (Precision, Recall, ROC-AUC)
   - Tuned decision threshold for best fraud detection trade-off

3. **Results**
   - **ROC-AUC:** 0.98
   - **Recall (Fraud):** 85% at threshold 0.35
   - **Precision (Fraud):** 20% at threshold 0.35

4. **Recommendations**
   - Deploy model at threshold ≈ 0.35
   - Auto-block top 1% risky transactions, review next 4% manually
   - Retrain model quarterly

---

## 📈 Results Summary
| Metric                  | Default (0.5) | Tuned (0.35) |
|-------------------------|---------------|--------------|
| Recall (Fraud)          | 92%           | 85%          |
| Precision (Fraud)       | 6%            | 20%          |
| ROC-AUC                 | 0.98          | 0.98         |

---

## 📂 Key Files
- 📓 **[EDA Notebook](notebooks/1_exploratory_analysis.ipynb)**  
- 📓 **[Modeling Notebook](notebooks/2_modeling_and_tuning.ipynb)**  
- 📄 **[Business Case](docs/business_case.md)**  
- 📄 **[Executive Summary](reports/executive_summary.pdf)**  

---

## 🛠 Installation
```bash
git clone <https://github.com/srinath2327/Credit-Card-Fraud-Detection>
cd credit-card-fraud-detection
pip install -r requirements.txt
