# 🏢 Project 8: Industry-Ready End-to-End ML System for Business Intelligence
### RISE Internship — Machine Learning & AI | Tamizhan Skills

---

## 🚀 Live Dashboard

**[▶ Open Live Dashboard](https://rise-capstone-business-intelligence.vercel.app)**

> Interactive customer intelligence dashboard with real-time churn prediction, CLV forecasting, risk segmentation, and live customer prediction tool.

---

## 📌 Problem Statement

Many organizations experiment with machine learning models but fail to integrate them into end-to-end business workflows. Isolated models without insights, evaluation, and reporting do not create business value. Industry requires complete ML systems that support decision-making.

---

## 🎯 Objective

To design and implement an end-to-end machine learning solution that transforms raw business data into predictions, insights, and actionable intelligence.

This project solves **two ML problems** on the same customer dataset:

| Problem | Type | Target |
|---------|------|--------|
| A — Churn Prediction | Classification | Will this customer leave? (Yes/No) |
| B — CLV Forecasting | Regression | How much is this customer worth? ($) |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python 3.10 | Core language |
| NumPy | Numerical computation |
| Pandas | Data manipulation |
| Matplotlib | Visualisation |
| Seaborn | Statistical plots |
| Scikit-learn | ML models & evaluation |
| Jupyter Notebook | Development environment |
| HTML / CSS / JS | Live dashboard |
| Chart.js | Dashboard charts |
| Vercel | Dashboard deployment |

---

## 📁 Project Structure

```
RISE-ML-Project8-Business-Intelligence/
├── Business_Intelligence_RISE_Project8.ipynb   ← Main notebook
├── dashboard/
│   └── index.html                              ← Live deployed dashboard
├── outputs/
│   ├── 01_eda_dashboard.png
│   ├── 02_correlation_heatmap.png
│   ├── 03_classification_evaluation.png
│   ├── 04_regression_evaluation.png
│   ├── 05_clv_prediction.png
│   ├── 06_feature_importance.png
│   ├── 07_business_outcomes_dashboard.png
│   ├── customer_predictions.csv
│   ├── high_risk_customers.csv
│   └── model_summary.csv
└── README.md
```

---

## 🔄 End-to-End Pipeline

```
Raw Data → EDA → Cleaning → Feature Engineering
    → Classification Models (Churn)
    → Regression Models (CLV)
    → Model Evaluation & Comparison
    → Business Insight Generation
    → Visualisation Dashboard
    → Deployed Live Application
```

---

## 📊 Dataset

Synthetic retail customer dataset — **2,000 customers**, **21 features**

| Feature | Description |
|---------|-------------|
| Age, Gender, Region | Demographics |
| TenureMonths | How long they've been a customer |
| NumPurchases, TotalSpent, AvgOrderValue | Purchase behaviour |
| DaysSincePurchase | Recency indicator |
| NumComplaints, NumReturns | Dissatisfaction signals |
| LoyaltyScore, EmailOpenRate | Engagement metrics |
| SupportTickets, DiscountUsed | Service usage |
| **CLV** | Regression target — lifetime value ($) |
| **Churn** | Classification target — 0 or 1 |

---

## 🤖 Models Trained

### Problem A — Churn Classification

| Model | F1-Score | ROC-AUC | Accuracy |
|-------|----------|---------|----------|
| Logistic Regression | 0.4091 | 0.8932 | 0.94 |
| Decision Tree | 0.4231 | 0.7617 | 0.93 |
| Random Forest | 0.3721 | 0.9258 | 0.94 |
| **Gradient Boosting** ⭐ | **0.4783** | **0.9281** | **0.94** |

### Problem B — CLV Regression

| Model | MAE | RMSE | R² |
|-------|-----|------|----|
| **Linear Regression** ⭐ | **$147.85** | **$187.30** | **0.8782** |
| Gradient Boosting | $160.44 | $203.67 | 0.8559 |
| Random Forest | $164.22 | $205.30 | 0.8536 |

---

## 📈 Key Results

- **110 high-risk customers** identified for immediate retention action
- **$82,678** in predicted CLV at risk from high-churn customers
- Churn rate: **6.9%** of customer base
- CLV model explains **87.8%** of revenue variance (R² = 0.8782)
- Best churn model ROC-AUC: **0.9281** — strong ranking ability

---

## 💡 Features

New features created beyond raw data:

| Feature | Formula | Business Meaning |
|---------|---------|-----------------|
| SpendPerMonth | TotalSpent / TenureMonths | Monthly revenue rate |
| ComplaintRate | NumComplaints / NumPurchases | Dissatisfaction intensity |
| ReturnRate | NumReturns / NumPurchases | Product-fit signal |
| EngagementScore | EmailOpenRate×50 + LoyaltyScore×0.5 | Overall engagement |
| IsHighValue | CLV > 75th percentile | Top customer flag |
| IsRecentBuyer | DaysSincePurchase < 30 | Recency flag |
| IsLongTenure | TenureMonths > 24 | Loyalty flag |

---

## 🖥️ Live Dashboard Features

**[https://rise-capstone-business-intelligence.vercel.app](https://rise-capstone-business-intelligence.vercel.app)**

- **4 KPI cards** — total customers, churn rate, avg CLV, revenue at risk
- **Interactive filters** — by Region, Risk level, and Tenure
- **7 live charts** — risk distribution, CLV by segment, churn by region, loyalty scatter, complaints analysis, tenure analysis, revenue at risk
- **Priority retention table** — top high-risk customers ranked by CLV with churn probability bars
- **Live prediction tool** — enter any customer's data, get instant churn probability + CLV + risk segment + retention recommendation

---

## ▶️ How to Run

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/RISE-ML-Project8-Business-Intelligence.git
cd RISE-ML-Project8-Business-Intelligence

# 2. Install dependencies
pip install numpy pandas matplotlib seaborn scikit-learn jupyter

# 3. Launch notebook
jupyter notebook Business_Intelligence_RISE_Project8.ipynb

# 4. Run all cells (Kernel → Restart & Run All)
```

---

## 📤 Output Files

| File | Description |
|------|-------------|
| `customer_predictions.csv` | All 2000 customers with churn probability, CLV, risk segment |
| `high_risk_customers.csv` | 110 high-risk customers ranked by CLV — retention priority list |
| `model_summary.csv` | All models, metrics, and comparison |
| `01_eda_dashboard.png` | 9-panel EDA overview dashboard |
| `02_correlation_heatmap.png` | Feature correlation matrix |
| `03_classification_evaluation.png` | Churn model comparison + ROC curves |
| `04_regression_evaluation.png` | CLV model metric comparison |
| `05_clv_prediction.png` | Actual vs predicted CLV scatter |
| `06_feature_importance.png` | Top features for both problems |
| `07_business_outcomes_dashboard.png` | Full business intelligence dashboard |

---

## 🎓 Learning Outcomes

- End-to-end experience with real-world ML pipelines
- Solving classification AND regression on the same dataset
- Feature engineering with business domain knowledge
- Model evaluation and comparison across problem types
- Translating ML outputs into business decisions
- Deploying a production-grade dashboard

---

*Built as part of the RISE Internship — Machine Learning & AI track by Tamizhan Skills*
