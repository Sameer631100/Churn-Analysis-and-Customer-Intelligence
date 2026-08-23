# 📊 Churn Analysis & Customer Intelligence

An end-to-end **Customer Churn Analysis** project for an OTT subscription platform, using **SQL and Python** to identify churn patterns, analyze customer behavior, measure revenue impact, and generate actionable retention strategies.

## 📌 Project Overview

Customer retention is critical in the highly competitive OTT industry. This project analyzes subscriber, subscription, and customer-support data to identify:

* **Who** is likely to churn
* **Why** customers churn
* **When** customers are most likely to leave
* Which customer segments have the highest financial risk
* How churn affects revenue and Customer Lifetime Value (CLTV)

The project combines **SQL data extraction, data cleaning, feature engineering, exploratory data analysis, visualization, and business intelligence** to convert raw customer data into actionable insights.

## 🎯 Objectives

* Analyze customer churn behavior
* Identify high-risk customer segments
* Calculate important churn and revenue KPIs
* Analyze churn across subscription plans and locations
* Investigate the relationship between customer support escalations and churn
* Quantify revenue loss and CLTV impact
* Develop data-driven customer retention strategies

## 🛠️ Tech Stack

| Category           | Technologies                           |
| ------------------ | -------------------------------------- |
| Programming        | Python                                 |
| Database           | SQLite                                 |
| Data Manipulation  | Pandas, NumPy                          |
| Data Analysis      | Pandas, NumPy                          |
| Data Visualization | Matplotlib, Seaborn                    |
| Data Extraction    | SQL                                    |
| Analytics          | EDA, Feature Engineering, KPI Analysis |

## 🔄 Project Workflow

```text
Relational Database
        ↓
SQL Data Extraction
        ↓
Python + Pandas
        ↓
Data Cleaning
        ↓
Feature Engineering
        ↓
Exploratory Data Analysis
        ↓
KPI & Churn Analysis
        ↓
Data Visualization
        ↓
Business Insights
        ↓
Retention Strategy
```

## 🗄️ Database Structure

The project uses a relational database named **`customer_churn`** containing three primary tables.

### 1. `db_customer`

Contains customer demographic information:

* `customerid`
* `name`
* `country`
* `state`
* `gender`
* `dob`
* `interests`
* `pincode`

### 2. `db_subscription`

Contains subscription and financial information:

* `customerid`
* `subscription_start_date`
* `subscription_type`
* `renewal_date`
* `plan_type`
* `contract_type`
* `cancellation_date`
* `cancellation_reason`
* `monthly_charges`
* `cltv`
* `churn_score`

### 3. `db_support`

Contains customer-support information:

* `customerid`
* `complaint_date`
* `escalations`
* `csat_score`
* `comment`

## 🧹 Data Cleaning

The data-cleaning stage includes:

* Checking and converting data types
* Renaming columns where required
* Selecting relevant columns
* Performing quality checks
* Identifying and handling missing/null values

## ⚙️ Feature Engineering

New analytical features are created to support churn analysis, including:

* Customer tenure
* Churn-related metrics
* Customer aging
* Revenue-related measures
* Risk-based segmentation
* Transformed analytical variables

## 📈 Key KPIs

| KPI                | Description                                                 |
| ------------------ | ----------------------------------------------------------- |
| Churn Rate         | Churned customers / Total customers                         |
| Retention Rate     | 1 − Churn Rate                                              |
| Churn by Plan      | Churn rate grouped by plan type                             |
| Churn by Location  | Churn rate grouped by country/state                         |
| ARPU               | Total monthly charges / Active customers                    |
| Average Tenure     | Average customer subscription duration                      |
| Revenue at Risk    | Monthly revenue associated with high-risk customers         |
| Escalation Rate    | Escalations / Complaints × 100                              |
| Average Complaints | Complaints / Distinct customers                             |
| Escalation → Churn | Churn comparison for customers with and without escalations |

## 🔍 Exploratory Data Analysis

EDA focuses on:

* Aggregations
* Group-by analysis
* Pivot tables
* Churn segmentation
* Plan-level analysis
* Geographic analysis
* Contract-type comparisons
* Customer-support analysis

Visualizations are created using **Matplotlib** and **Seaborn**.

## 💡 Key Findings

| Metric                  |             Result |
| ----------------------- | -----------------: |
| Overall Churn Rate      |          **28.6%** |
| Retention Rate          |          **71.4%** |
| Average Tenure          |     **1,451 days** |
| ARPU                    |        **Rs 18.8** |
| Total Revenue           |            **395** |
| Revenue Loss from Churn |             **74** |
| CLTV Lost               |          **2,047** |
| Revenue Loss            |            **18%** |
| Monthly Contract Churn  |          **55.6%** |
| Annual Contract Churn   |           **8.3%** |
| Highest-Affected State  |      **Karnataka** |
| Highest Churn Period    | **September 2024** |

## 💰 Business Impact

The analysis identified:

* **28.6% overall churn**
* **55.6% churn among monthly-contract subscribers**
* **8.3% churn among annual-contract subscribers**
* Approximately **73.94/month in MRR leakage**
* Approximately **2,047 in CLTV erosion**
* Six customers identified as an at-risk cohort

These findings support a targeted **contract-migration and retention strategy**.

## 🎯 Customer Risk Segmentation

Customers can be segmented according to:

* Subscription tenure
* Plan type
* Contract type
* Churn score
* Support escalations
* Customer complaints
* Customer Lifetime Value

High- and medium-risk customers can then be prioritized for retention campaigns.

## 📞 Support & Churn Intelligence

Customer-support data is integrated with subscription information to investigate potential relationships between:

* Complaints
* Support escalations
* CSAT scores
* Cancellation reasons
* Churn behavior

## 🚀 Recommended Business Actions

1. **Investigate Karnataka**

   * Analyze pricing changes, complaints, technical issues, and other regional factors.

2. **Analyze Basic Plan Changes**

   * Determine whether recent pricing or product changes affected Basic-plan customers.

3. **Investigate September 2024**

   * Identify events or product changes associated with the churn spike.

4. **Monitor Competitor Activity**

   * Investigate competitor offers and customer switching behavior.

5. **Prioritize High-Risk Customers**

   * Identify customers with High and Medium churn scores.
   * Consider LTV when prioritizing retention campaigns.

6. **Proactive Customer Outreach**

   * Use email, SMS, or calls to address customer concerns before cancellation.

## 📂 Repository Structure

```text
customer-churn-analysis/
│
├── data/
│   └── customer_churn.db
│
├── notebooks/
│   └── churn_analysis.ipynb
│
├── sql/
│   └── churn_queries.sql
│
├── visualizations/
│   └── charts/
│
├── reports/
│   └── insights.pdf
│
├── requirements.txt
├── README.md
└── .gitignore
```

## ▶️ How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/customer-churn-analysis.git
cd customer-churn-analysis
```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn
```

### 3. Run the Analysis

Open the Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
notebooks/churn_analysis.ipynb
```

## 📊 Skills Demonstrated

* SQL
* Python
* Data Manipulation
* Data Cleaning
* Feature Engineering
* Exploratory Data Analysis (EDA)
* Statistical Analysis
* Data Visualization
* KPI Development
* Customer Segmentation
* Churn Analysis
* Revenue Analysis
* Business Intelligence
* Actionable Insight Generation

## 📌 Project Highlights

> **End-to-end data analytics project transforming relational customer data into actionable churn and retention insights.**

### Key Results

**28.6%** — Overall Churn Rate
**55.6%** — Monthly Contract Churn
**8.3%** — Annual Contract Churn
**18%** — Revenue Loss
**2,047** — CLTV Lost
**1,451 days** — Average Customer Tenure

## 🔮 Future Enhancements

* Build an interactive **Power BI/Tableau dashboard**
* Develop a machine-learning-based churn prediction model
* Implement automated customer risk scoring
* Add cohort and retention analysis
* Build customer lifetime value forecasting
* Automate SQL-to-Python data pipelines
* Develop real-time churn monitoring
* Create automated executive reporting

## 👨‍💻 Author

**Sameer Sardana**

Data Analytics | Business Intelligence | Python | SQL | Data Visualization

---

⭐ If you found this project useful, consider giving the repository a star.
