# 🛒 Walmart Inventory Intelligence System
### From Basic EDA → Production-Grade Machine Learning System

<p align="left">
  <img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Scikit--Learn-1.3-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Status-Production%20Ready-4CAF50?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Domain-Retail%20Analytics-9C27B0?style=for-the-badge"/>
</p>

---

## 📌 Project Overview

This project evolved in **two versions** — starting from a thorough exploratory data analysis of Walmart's inventory data, then upgraded to a full **production-grade ML system** with demand forecasting, stockout risk prediction, revenue forecasting, and inventory optimization.

> **Business Problem:** Walmart's existing forecasting system has ~18% MAPE error, causing significant revenue loss from stockouts and excess capital locked in overstock. This project replaces it with an ML-driven approach.

---

## 🗂️ Repository Structure

```
Walmart-Inventory-Analysis/
│
├── 📓 Walmart-Inventory-Analysis.ipynb       ← Version 1: EDA & Insights
├── 📓 Walmart_MNC_Level_Analysis.ipynb       ← Version 2: Full ML System
├── 📄 Walmart-Inventory-Dataset.csv          ← Dataset
├── 📄 Walmart-Inventory-Analysis-summary.pdf ← Project Summary PDF
├── 📄 requirements.txt                       ← Python Dependencies
├── 📄 .gitignore                             ← Git Configuration
│
├── 📂 models/        ← Auto-created when notebook runs
│   ├── demand_forecast_model.pkl
│   ├── stockout_classifier.pkl
│   ├── revenue_forecast_model.pkl
│   ├── label_encoders.pkl
│   └── model_metadata.json
│
└── 📂 reports/       ← Auto-created when notebook runs
    ├── kpi_dashboard.png
    ├── eda_analysis.png
    ├── model_evaluation.png
    ├── feature_importance.png
    ├── stockout_classifier.png
    ├── revenue_forecast.png
    ├── inventory_optimization.png
    ├── store_performance.png
    └── business_impact.png
```

---

## 📊 Version 1 — EDA & Business Insights 
> `Walmart-Inventory-Analysis.ipynb`

A comprehensive exploratory analysis answering 22 real business questions:

| Analysis Area | Key Finding |
|--------------|-------------|
| Revenue Analysis | Electronics generates 52% of total revenue ($7.94M) |
| Inventory vs Demand | Correlation = 0.003 → Inventory NOT aligned with demand |
| Forecast Accuracy | 18.4% forecast error → Poor planning model |
| Stockout Impact | $752K higher revenue during stockout periods (peak demand) |
| Lost Revenue | $359M lost due to under-forecasting |
| Excess Inventory | $343M tied up due to over-forecasting |
| Customer Retention | 74.9% one-time buyers → Major retention opportunity |
| Store Performance | $374K revenue gap between best and worst store |

**Skills Demonstrated:** Pandas, Matplotlib, Seaborn, Business KPI Analysis, Data Storytelling

---

## 🤖 Version 2 — MNC-Level ML System
> `Walmart_MNC_Level_Analysis.ipynb`

### 🏗️ ML Pipeline Architecture

```
Raw Data
   ↓
Cleaning Pipeline (15+ engineered features)
   ↓
┌──────────────────────────────────────────┐
│  Demand Forecasting    → Random Forest   │
│  Stockout Classifier   → RF Classifier  │
│  Revenue Forecasting   → Grad. Boosting  │
│  Inventory Optimizer   → EOQ Formula     │
└──────────────────────────────────────────┘
   ↓
Business Impact Quantification
   ↓
Model Persistence → Production Deployment
```

### 📈 Models & Performance

| Model | Type | Purpose | Evaluation |
|-------|------|---------|------------|
| Random Forest (Tuned) | Regression | Demand Forecasting | R², RMSE, MAPE, CV Score |
| Gradient Boosting | Regression | Revenue Forecasting | R², RMSE |
| RF Classifier (Tuned) | Classification | Stockout Risk | AUC-ROC, F1, Accuracy |

### ⚙️ MNC-Standard Techniques Used

| Technique | Why It Matters |
|-----------|---------------|
| `TimeSeriesSplit` Cross-Validation | Prevents data leakage in time series — standard in industry |
| `RandomizedSearchCV` Hyperparameter Tuning | Finds optimal model parameters systematically |
| ROC-AUC Curve | Proper evaluation for imbalanced classification |
| Time-Based Train/Test Split | Future data never leaks into training set |
| EOQ + Safety Stock Formula | Real supply chain optimization used by Walmart, Amazon |
| Feature Importance Analysis | Explains which features drive demand |
| Model Persistence (joblib) | Serialized models ready for API deployment |
| Business Impact in $ | Connects ML metrics to real revenue numbers |

### 💰 Business Impact Quantification

| Opportunity | Approach | Projected Value |
|-------------|----------|----------------|
| Stockout Recovery | 30% recovery via better forecasting | Run notebook to see |
| Overstock Savings | 20% reduction in holding costs | Run notebook to see |
| Customer Retention | 5% improvement from repeat buyer program | Run notebook to see |
| 30-Day Revenue Forecast | Forward-looking revenue planning | Run notebook to see |

### 📁 Production Deliverables

After running the notebook, these files are auto-saved:

**Models (ready for API deployment):**
- `models/demand_forecast_model.pkl`
- `models/stockout_classifier.pkl`
- `models/revenue_forecast_model.pkl`
- `models/label_encoders.pkl`
- `models/model_metadata.json` ← version tracking

**Business Reports (share with stakeholders):**
- `reports/kpi_dashboard.png`
- `reports/revenue_forecast.png`
- `reports/business_impact.png`
- + 6 more charts

---

## 🚀 How to Run

### Prerequisites
- Python 3.10+
- Jupyter Notebook

### Setup

```bash
# 1. Clone the repository
git clone https://github.com/akash01-arch/Walmart-Inventory-Analysis.git
cd Walmart-Inventory-Analysis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run Version 1 — EDA
jupyter notebook Walmart-Inventory-Analysis.ipynb

# 4. Run Version 2 — ML System
jupyter notebook Walmart_MNC_Level_Analysis.ipynb
```

> ⚠️ Run all cells **top to bottom** in order.
> `models/` and `reports/` folders are auto-created by the notebook.

---

## 📊 Key Visualizations

| Chart | Description |
|-------|-------------|
| Executive KPI Dashboard | 8 business metrics in a card layout |
| Seasonality Heatmap | Revenue patterns by Month × Day of Week |
| Model Comparison | R² Score leaderboard across 4 models |
| ROC-AUC Curve | Stockout classifier quality |
| 30-Day Revenue Forecast | With ±12% confidence band |
| Store Performance Matrix | Revenue vs Stockout rate bubble chart |
| Inventory Action Matrix | Reorder Now / Monitor / Sufficient breakdown |
| Business Impact Chart | Dollar value of ML improvements |

---

## 🗺️ Project Roadmap

- [x] EDA & 22 Business Questions Answered
- [x] Data Cleaning Pipeline
- [x] Feature Engineering (15+ features)
- [x] Demand Forecasting Model (Tuned)
- [x] Stockout Risk Classifier (Tuned)
- [x] 30-Day Revenue Forecast
- [x] EOQ + Safety Stock Optimization
- [x] Model Persistence & Deployment Readiness
- [x] Business Impact Quantification
- [ ] SHAP Values for Deep Explainability
- [ ] XGBoost / LightGBM Integration
- [ ] FastAPI Deployment Endpoint
- [ ] MLflow Experiment Tracking
- [ ] Interactive Plotly Dash Dashboard

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Data Processing | `pandas` `numpy` |
| Visualization | `matplotlib` `seaborn` |
| Machine Learning | `scikit-learn` |
| Model Persistence | `joblib` |
| Environment | `jupyter notebook` |

---

## 📂 Dataset

**Source:** Walmart Inventory Dataset  
**Records:** ~5,000 transactions  
**Features:** Store location, product category, inventory levels, demand, pricing, promotions, customer data

---

## 👤 Author

**Akash** — Intermediate Data Science Candidate

[![GitHub](https://img.shields.io/badge/GitHub-akash01--arch-181717?style=flat&logo=github)](https://github.com/akash01-arch)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

*This project demonstrates the complete data science lifecycle — from raw data exploration to production-ready ML models with quantified business impact.*
