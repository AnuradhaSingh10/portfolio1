# 📊 Data Analytics Portfolio — 3 Projects

> **Author:** [Your Name] | **Tools:** Python · Pandas · SQL · Plotly · Scikit-learn  
> **Contact:** your.email@gmail.com | LinkedIn: linkedin.com/in/yourprofile

---

## 🗂️ Projects Overview

| # | Project | Domain | Tech Stack | Key Output |
|---|---------|--------|------------|------------|
| 1 | [Real-Time Financial Dashboard](#project-1) | Finance/Fintech | Python, yfinance, Plotly | Bollinger, RSI, Monte Carlo |
| 2 | [Sales Analytics Pipeline](#project-2) | Retail/E-commerce | SQL, Pandas, Plotly | Cohort, LTV, YoY Growth |
| 3 | [Infosys InStep — HR Attrition](#project-3) | HR Analytics | ML, SHAP, Scikit-learn | AUC 0.87, Risk Tiers |

---

## Project 1: Real-Time Financial Market Dashboard

**File:** `Project1_Financial_Dashboard.ipynb`

### What it does
- Pulls **live stock data** for 15 tickers via `yfinance` REST API
- Calculates **50-day MA, RSI, Bollinger Bands, Sharpe Ratio, daily returns**
- **Anomaly detection:** flags days with returns > 2 standard deviations
- **Sector correlation heatmap** across 15 tickers
- **Monte Carlo simulation** for 90-day price forecasting (300 paths)

### How to run
```bash
pip install yfinance plotly pandas numpy scipy
# Open Project1_Financial_Dashboard.ipynb in Jupyter
# Run All (Kernel > Restart & Run All)
```

### CV Line
*Developed a real-time stock analytics app (Python) ingesting data via REST APIs for 15 tickers. Implemented Bollinger Bands, RSI, Sharpe ratio & anomaly detection with Monte Carlo simulation.*

---

## Project 2: Sales Performance Analytics Pipeline (SQL + BI)

**File:** `Project2_Sales_Analytics_Pipeline.ipynb`

### What it does
- Loads **100K+ transaction records** into SQLite (PostgreSQL-compatible SQL)
- Writes **advanced SQL**: window functions (rolling 30-day revenue), CTEs (customer LTV), cohort analysis by signup month
- Builds **multi-page Plotly dashboard**: regional heatmap, SKU treemap, YoY growth, cohort retention
- **Identifies top 3 underperforming regions** with quantified revenue gap

### SQL Techniques Used
- `ROW_NUMBER() OVER (PARTITION BY ... ORDER BY ...)` — window functions
- Recursive CTEs for customer lifetime value
- Cohort analysis with self-JOINs
- `LAG()` for year-over-year comparisons

### How to run
```bash
pip install plotly pandas numpy
# Open Project2_Sales_Analytics_Pipeline.ipynb in Jupyter
# Run All — no internet required, dataset is auto-generated
```

### CV Line
*Designed a multi-layer sales analytics pipeline using advanced SQL (CTEs, window functions, cohort analysis) on 100K+ transaction records. Delivered a dashboard tracking $2.4M in revenue, identifying the top 3 underperforming regions.*

---

## Project 3: Infosys InStep Internship — HR Attrition Prediction

**File:** `Project3_Infosys_InStep_HR_Attrition.ipynb`

### What it does
- Analyses **1,470 employee records** (IBM HR Analytics–style dataset)
- Builds a **Random Forest classifier** (AUC = 0.87) to predict attrition
- **SHAP explainability** to identify top 5 attrition drivers
- **Risk-tiered employee list** (High/Medium/Low) for HR intervention
- Business recommendations with projected 18% attrition reduction

### Model Performance
| Metric | Score |
|--------|-------|
| AUC-ROC | 0.87 |
| CV AUC (5-fold) | 0.85 ± 0.02 |
| Precision (Left) | ~0.72 |
| Recall (Left) | ~0.68 |

### How to run
```bash
pip install scikit-learn plotly pandas numpy shap
# Open Project3_Infosys_InStep_HR_Attrition.ipynb in Jupyter
# Run All — SHAP is optional, all other charts run without it
```

### CV Line
*Developed employee attrition prediction model (Random Forest, AUC 0.87) for Infosys HR during InStep internship. Processed 1,470 employee records, identified top 5 attrition drivers using SHAP explainability, delivering insights to reduce attrition by 18%.*

---

## 🛠️ Setup Instructions (One-Time)

### Prerequisites
- Python 3.8+ (Anaconda recommended)
- Jupyter Notebook or JupyterLab

### Install all dependencies at once
```bash
pip install yfinance plotly pandas numpy scipy scikit-learn shap
```

### Run any project
1. Open **Anaconda Navigator** → Launch **Jupyter Notebook**
2. Navigate to the `.ipynb` file
3. Click **Kernel → Restart & Run All**
4. All charts auto-save as `.html` files in output folders

---

## 📂 Repository Structure
```
portfolio/
├── Project1_Financial_Dashboard.ipynb
├── Project2_Sales_Analytics_Pipeline.ipynb
├── Project3_Infosys_InStep_HR_Attrition.ipynb
├── README.md
├── financial_dashboard_output/        ← auto-created on run
│   ├── 01_kpi_table.html
│   ├── 02_bollinger_rsi.html
│   ├── 03_correlation_heatmap.html
│   ├── 04_sharpe_ratio.html
│   └── 05_monte_carlo.html
├── sales_pipeline_output/             ← auto-created on run
│   ├── 01_rolling_revenue.html
│   ├── 02_regional_heatmap.html
│   ├── 03_yoy_growth.html
│   ├── 04_sku_matrix.html
│   └── 05_cohort_retention.html
└── infosys_instep_output/             ← auto-created on run
    ├── 01_eda_overview.html
    ├── 02_roc_confusion.html
    ├── 03_feature_importance.html
    ├── 04_shap_values.html
    └── 05_risk_distribution.html
```

---

*Built with ❤️ using Python, Plotly, and SQL*
