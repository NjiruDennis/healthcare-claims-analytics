# 🏥 Healthcare Insurance Claims Analytics

![SQL](https://img.shields.io/badge/SQL-PostgreSQL-blue?logo=postgresql)
![Python](https://img.shields.io/badge/Python-3.12-green?logo=python)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange?logo=jupyter)
![Tableau](https://img.shields.io/badge/BI-Tableau-lightblue?logo=tableau)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## 📌 Project Overview
End-to-end analysis of **54,860 healthcare insurance claims** spanning **May 2019 to May 2024**.
This project mirrors real-world healthcare analytics workflows including claims cost analysis,
insurer performance benchmarking, anomaly detection, and admission trend reporting.

> **Tools Used:** PostgreSQL 18, Python 3.12, Pandas, Matplotlib, Seaborn, Tableau, Jupyter Notebook

---

## 🎯 Business Questions Answered
1. Which insurance providers generate the highest claim volumes and total billing?
2. Which medical conditions drive the most cost across the portfolio?
3. Are there anomalous billing amounts that require investigation?
4. How does length of stay vary by condition and what does it cost per day?
5. What are the month-on-month admission and billing trends over 5 years?

---

## 📁 Project Structure
healthcare-claims-analytics/
├── data/
│   └── healthcare_dataset.csv       # Raw dataset (55,500 records)
├── sql/
│   └── healthcare_analysis.sql      # 6 advanced SQL queries
├── python/
│   ├── healthcare_eda.ipynb         # Full EDA Jupyter Notebook
│   ├── billing_distribution.png     # Billing analysis charts
│   ├── condition_analysis.png       # Medical condition charts
│   ├── admission_trends.png         # Monthly trend charts
│   └── los_admission_analysis.png   # Length of stay charts
├── tableau/
│   └── healthcare_dashboard.twbx    # Tableau dashboard (coming soon)
└── README.md

---

## 🗄️ Dataset
| Attribute | Detail |
|---|---|
| Source | [Kaggle - Healthcare Dataset](https://www.kaggle.com/datasets/prasad22/healthcare-dataset) |
| Records | 55,500 (54,860 after cleaning) |
| Columns | 15 |
| Date Range | May 2019 to May 2024 |
| Coverage | 5 insurance providers, 6 medical conditions |

---

## 🔍 Data Quality Findings
| Issue | Count | Resolution |
|---|---|---|
| Duplicate rows | 534 | Removed |
| Negative billing amounts | 108 | Flagged for review, kept in dataset |
| Missing values | 0 | No action needed |
| Inconsistent name casing | All records | Standardised to title case |

---

## 📊 SQL Analysis

Six advanced queries written in PostgreSQL demonstrating:
`CTEs` `Window Functions` `RANK()` `LAG()` `PARTITION BY` `Z-Score Anomaly Detection` `DATE_TRUNC` `NULLIF`

| Query | Description |
|---|---|
| 1 | Dataset overview and summary statistics |
| 2 | Billing analysis by insurance provider with window functions |
| 3 | Medical condition cost ranking with running totals |
| 4 | Anomaly detection using Z-score statistical method |
| 5 | Length of stay analysis with PARTITION BY |
| 6 | Month-on-month admission trends using LAG function |

📂 See full queries: [sql/healthcare_analysis.sql](sql/healthcare_analysis.sql)

---

## 🐍 Python EDA

Full exploratory data analysis in Jupyter Notebook covering data loading,
cleaning, transformation, and visualisation.

📂 See notebook: [python/healthcare_eda.ipynb](python/healthcare_eda.ipynb)

### Billing Distribution
![Billing Distribution](python/billing_distribution.png)

### Medical Condition Analysis
![Condition Analysis](python/condition_analysis.png)

### Monthly Admission Trends
![Admission Trends](python/admission_trends.png)

### Length of Stay & Admission Type
![LOS Analysis](python/los_admission_analysis.png)

---

## 💡 Key Findings

| Finding | Detail |
|---|---|
| Total portfolio value | $1,404,121,601 across 54,860 claims |
| Average claim value | $25,594 per patient |
| Highest cost condition | Diabetes at $236,494,659 total billing |
| Top insurer by volume | Cigna with 11,115 claims |
| Average length of stay | 15.5 days overall |
| Billing anomalies | 108 negative billing records flagged |
| Monthly billing range | $19M to $26M per month |
| Notable trend | Feb 2022 dip: admissions dropped 18%, billing dropped to $19M |

---

## ⚙️ How to Run This Project

### SQL
1. Install PostgreSQL 18
2. Create a database called `healthcare_claims`
3. Run the table creation and import script
4. Execute queries in `sql/healthcare_analysis.sql`

### Python
```bash
pip install pandas matplotlib seaborn psycopg2-binary sqlalchemy jupyter
jupyter notebook python/healthcare_eda.ipynb
```

---

## 👤 Author
**Dennis Njiru Aningu**
Senior Data Analyst | SQL, Python, Tableau, Excel

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://linkedin.com/in/dennisaningu)
[![GitHub](https://img.shields.io/badge/GitHub-NjiruDennis-black?logo=github)](https://github.com/NjiruDennis)

