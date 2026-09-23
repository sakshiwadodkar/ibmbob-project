# InsightIQ — AI-Powered Business Decision Intelligence Platform

**IBM SkillsBuild Data Analytics with AI Academic Internship — Capstone Project**  
**Author:** Sakshi Wadodkar  
**Dataset:** Official Tableau Sample Superstore  
**Year:** 2025

---

## 1. Project Overview

InsightIQ is a comprehensive AI-powered business decision intelligence platform built entirely on the official Tableau Sample Superstore dataset. The platform integrates descriptive analytics, predictive machine learning, explainable AI, anomaly detection, and what-if decision simulation into a single, cohesive Jupyter Notebook pipeline.

The central business question addressed is:

> *"Given historical business data, what is happening in the business, what patterns and risks can be identified, what may happen next, and how might different business decisions affect expected outcomes?"*

---

## 2. Problem Statement

Modern retail organisations accumulate vast volumes of transactional data but frequently lack the analytical infrastructure to extract timely, actionable intelligence. Key challenges include:

- Unclear drivers of profitability across products, customers, and regions
- Unmanaged discount strategies eroding margins
- Absence of reliable sales forecasting
- No systematic identification of anomalous business events
- Inability to simulate the potential impact of strategic decisions before execution

InsightIQ addresses all of these challenges through a structured, reproducible analytics pipeline.

---

## 3. Objectives

1. Perform comprehensive exploratory data analysis on the Superstore dataset
2. Calculate and visualise key business KPIs (Sales, Profit, Margin, AOV)
3. Analyse customer, product, and regional performance patterns
4. Investigate the historical relationship between discount levels and profitability
5. Build and evaluate predictive sales models (Linear Regression + Random Forest)
6. Apply feature importance for model explainability
7. Detect anomalous business performance observations using Isolation Forest
8. Analyse product returns using the Returns sheet
9. Build an interactive what-if Decision Simulator for discount scenario analysis
10. Provide traceable, data-supported business recommendations

---

## 4. Key Features

| Feature | Description |
|---------|-------------|
| **Business KPI Dashboard** | Total Sales, Profit, Margin, Orders, Customers, AOV, Discount |
| **EDA Suite** | 15+ visualisations across time, category, region, customer, and product dimensions |
| **Predictive Sales Model** | Random Forest + Linear Regression with chronological train/test split |
| **Model Evaluation** | MAE, RMSE, MAPE with actual vs predicted plots |
| **Explainable ML** | Random Forest feature importance with interpretation |
| **Anomaly Detection** | Isolation Forest at transaction and monthly level |
| **Returns Analysis** | Order-level return rate by category, region, and segment |
| **InsightIQ Decision Simulator** | What-if discount scenario analysis with estimated sales, profit, and margin |
| **Scenario Comparison** | Multi-scenario table and visualisation |
| **Business Risk Analysis** | Structured identification of data-supported risk indicators |

---

## 5. Dataset Description

| Attribute | Value |
|-----------|-------|
| **File** | `sample_-_superstore.xls` |
| **Format** | Microsoft Excel 97-2003 (.xls) |
| **Primary Sheet** | Orders — 10,194 transaction line records, 21 columns |
| **Supporting Sheets** | Returns (296 returned orders), People (4 regional managers) |
| **Time Period** | January 2023 – December 2026 |
| **Geography** | United States and Canada |
| **Key Dimensions** | Category, Sub-Category, Region, Segment, Ship Mode |
| **Key Measures** | Sales, Profit, Quantity, Discount |

---

## 6. Official Dataset Source

**Tableau Public Sample Data:**  
https://public.tableau.com/app/resources/sample-data

> The Tableau Sample Superstore dataset is the intellectual property of Tableau Software. It is used here strictly for educational and academic research purposes under the IBM SkillsBuild internship programme. No ownership is claimed over the dataset.

---

## 7. Technologies Used

| Technology | Version | Purpose |
|-----------|---------|---------|
| Python | 3.x | Core programming language |
| pandas | ≥1.5.0 | Data manipulation and analysis |
| numpy | ≥1.23.0 | Numerical computations |
| matplotlib | ≥3.6.0 | Static visualisations |
| seaborn | ≥0.12.0 | Statistical visualisations |
| scikit-learn | ≥1.2.0 | ML (Random Forest, Isolation Forest) |
| xlrd | ≥1.2.0 | Reading legacy .xls files |
| python-docx | ≥0.8.11 | Project report generation |
| Jupyter Notebook | ≥1.0.0 | Interactive analytical environment |

---

## 8. Methodology

The project follows this analytical progression:

```
Historical Business Data (Superstore .xls)
        ↓
Data Loading & Sheet Inspection
        ↓
Data Quality Assessment
        ↓
Data Cleaning & Preprocessing
        ↓
Exploratory Data Analysis (15+ visualisations)
        ↓
Business KPI Calculation
        ↓
Customer / Product / Regional Analytics
        ↓
Discount & Profitability Analysis
        ↓
Time-Series Sales Analysis
        ↓
Predictive Modelling (Baseline → LR → Random Forest)
        ↓
Model Evaluation (MAE, RMSE, MAPE)
        ↓
Model Explainability (Feature Importance)
        ↓
Anomaly Detection (Isolation Forest)
        ↓
Business Risk Analysis
        ↓
Returns Analysis (Order-level)
        ↓
InsightIQ Decision Simulator (What-if Scenarios)
        ↓
Scenario Comparison
        ↓
Key Findings (Observed / Predicted / Anomaly / Scenario)
        ↓
Data-Supported Recommendations
```

---

## 9. Project Structure

```
InsightIQ/
├── sample_-_superstore.xls              ← Official Tableau dataset (DO NOT MODIFY)
├── SakshiWadodkar_InsightIQ.ipynb       ← Main analytical notebook
├── requirements.txt                     ← Python dependencies
├── SakshiWadodkar_InsightIQ_ProjectReport.docx  ← Full project report
└── README.md                            ← This file
```

Output image files generated during notebook execution (saved to project directory):
```
kpi_dashboard.png
customer_analytics.png
product_analytics.png
top_products.png
regional_analytics.png
discount_profitability.png
sales_trend.png
quarterly_sales.png
model_evaluation.png
feature_importance.png
anomaly_detection.png
returns_analysis.png
scenario_comparison.png
```

---

## 10. Installation Instructions

### Prerequisites

- Python 3.9 or higher
- pip (Python package manager)
- Jupyter Notebook or JupyterLab

### Step 1 — Install Python (if not already installed)

Download Python 3.11 or 3.12 from:  
https://www.python.org/downloads/

Ensure you check **"Add Python to PATH"** during installation.

### Step 2 — Verify installation

```bash
python --version
pip --version
```

---

## 11. Requirements Installation

Navigate to the project folder and install all dependencies:

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xlrd python-docx jupyter
```

---

## 12. Dataset Placement

The dataset file must be present in the **same folder** as the notebook:

```
InsightIQ/
├── sample_-_superstore.xls    ← REQUIRED
├── SakshiWadodkar_InsightIQ.ipynb
```

Do **not** rename or move the dataset file. The notebook loads it as:

```python
pd.read_excel('sample_-_superstore.xls', sheet_name='Orders', engine='xlrd')
```

---

## 13. How to Run

### Option A — Jupyter Notebook (recommended)

```bash
cd InsightIQ
jupyter notebook SakshiWadodkar_InsightIQ.ipynb
```

Then in the browser:  
**Kernel → Restart & Run All**

### Option B — JupyterLab

```bash
jupyter lab SakshiWadodkar_InsightIQ.ipynb
```

### Option C — VS Code

Open the `.ipynb` file in VS Code with the Jupyter extension installed.  
Select your Python interpreter and run all cells.

### Option D — Command line (nbconvert)

```bash
jupyter nbconvert --to notebook --execute SakshiWadodkar_InsightIQ.ipynb --output SakshiWadodkar_InsightIQ_executed.ipynb
```

---

## 14. Expected Outputs

After successful execution, the following outputs will be produced:

| Output | Description |
|--------|-------------|
| **KPI Dashboard** | 8-card visual summary of business performance metrics |
| **Customer Analytics** | Sales distribution, top customers, segment performance |
| **Product Analytics** | Sub-category sales and profit (with loss sub-categories highlighted) |
| **Regional Analytics** | Sales, profit, and margin by region |
| **Discount Analysis** | Scatter plot, band analysis, box plot |
| **Sales Trend** | Monthly sales and profit time-series |
| **Model Evaluation** | Actual vs predicted plot, residuals |
| **Feature Importance** | Horizontal bar chart of RF feature contributions |
| **Anomaly Detection** | Flagged transactions and monthly anomalies |
| **Returns Analysis** | Return rate by category, region, segment |
| **Decision Simulator** | Scenario comparison table and chart |

All charts are also saved as `.png` files in the project directory.

---

## 15. Predictive Modeling

The notebook builds and evaluates three approaches:

1. **Baseline** — Lag-1 naive forecast (previous month's sales as prediction)
2. **Linear Regression** — Time and lag features
3. **Random Forest Regressor** — Ensemble model with temporal and lag features

**Key design decisions:**
- Chronological train/test split (no random shuffle of time-series data)
- Last 25% of monthly observations used as the test set
- Lag features (Lag-1, Lag-2, Lag-3) prevent data leakage
- Best model selected by lowest RMSE on the held-out test set

**Evaluation metrics:** MAE, RMSE, MAPE (guarded against zero denominators)

> Predictions are model-based estimates from historical patterns. They are not guarantees of future business performance.

---

## 16. Explainable ML

Feature importance is extracted from the Random Forest model's mean decrease in impurity (MDI). The chart shows the relative contribution of each feature to the model's predictions.

**Features used:** Month Index, Month Number, Year, Quarter, Sales Lag-1, Sales Lag-2, Sales Lag-3

> Feature importance reflects model behaviour on historical data. It does not prove causal relationships between features and sales outcomes.

---

## 17. Anomaly Detection

Isolation Forest is applied at two levels:

1. **Transaction level** — Features: Sales, Profit, Quantity, Discount; contamination = 3%
2. **Monthly level** — Features: Monthly Sales, Monthly Profit; contamination = 10%

Anomalies are visualised and a sample is displayed. An anomaly is defined as an observation deviating substantially from the learned pattern — it is not automatically an error or fraud.

---

## 18. Decision Simulator

The InsightIQ Decision Simulator uses Random Forest models trained on order-line level data to estimate per-transaction Sales, Profit, and Margin under different discount scenarios.

**Scenarios evaluated:**
- No Discount (0%)
- Low Discount (10%)
- Moderate Discount (20%)
- High Discount (30%)
- Heavy Discount (50%)

**Output:** Estimated Sales, Profit, Margin, and delta vs baseline for each scenario.

> All simulator outputs are model-based scenario projections from historical data patterns. They are not causal estimates or guaranteed business outcomes.

---

## 19. Limitations

1. All findings are observational — no causal claims are made
2. The time-series model uses a limited number of monthly observations
3. The Decision Simulator operates at order-line level; real discount changes affect complex customer behaviour
4. Isolation Forest contamination parameter is an assumption requiring sensitivity analysis
5. Returns data provides Order ID only — no return reason, SKU, or cost data available
6. Dataset covers US and Canada only

---

## 20. Future Scope

1. ARIMA / Prophet / LSTM for advanced time-series forecasting
2. SHAP values for per-prediction explainability
3. Customer Lifetime Value (CLV) modelling
4. RFM-based customer churn prediction
5. Streamlit or Power BI interactive dashboard deployment
6. Price elasticity modelling with quasi-experimental methods
7. State-level geospatial choropleth visualisations
8. Automated retraining pipeline with new data

---

## 21. Author

**Sakshi Wadodkar**  
IBM SkillsBuild Data Analytics with AI Academic Internship  
Capstone Project — 2025

---

*Dataset source: Tableau Public Sample Data — https://public.tableau.com/app/resources/sample-data*  
*No ownership of the Tableau Sample Superstore dataset is claimed.*
