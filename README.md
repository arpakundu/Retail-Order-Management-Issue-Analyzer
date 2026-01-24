# Retail-Order-Management-Issue-Analyzer
This project implements a beginner-friendly, end-to-end analytics pipeline using Python and SQLite SQL to analyze order management data from a retail dataset. It simulates real-world API payload validations using Postman-style logic to identify issues in order lifecycles, enabling structured reporting on SLA breaches, cancelled-but-paid orders, and high-value delayed deliveries.
The project demonstrates core skills in SQL querying, Python data processing, API payload validation, and report generation — ideal for fresher roles involving data analytics, quality assurance, and process monitoring.

## 🎯 Business Problem
Retail order data often arrives as raw CSV files and requires validation and monitoring for operational efficiency. Companies need a reliable way to:
* Analyze order statuses and payment anomalies
* Detect delayed deliveries breaching SLA (Service Level Agreement)
* Flag issues early through API-like payload validations
* Generate actionable reports for downstream operational teams

## 📊 Dataset
**Name:** Brazilian E-Commerce Public Dataset by Olist
**Source:** https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce
**Type:** Structured CSV files
**Records:** 100,000+ orders with payments and order item details

**Key Tables:**
* `orders` (order details, timestamps, statuses)
* `payments` (payment transactions per order)
* `order_items` (products, price, freight info)

## ⚙️ Project Workflow
1. **Data Ingestion & Cleaning**
   Load raw CSV files using Pandas and clean any inconsistencies.
2. **SQLite Database Setup**
   Create and populate the `retail_oms.db` SQLite database file, which acts as the core data store for all SQL queries and analysis steps.
3. **SQL-Based Order Analytics**
   Perform structured queries to analyze order status distribution, detect cancelled-but-paid orders, and identify high-value delayed orders.
4. **Python-Powered Issue Flagging**
   Calculate delivery delays, classify orders as OK, DELAYED, or CANCELLED using Python logic.
5. **API Payload Simulation & Validation**
   Convert order data to JSON-like API payloads and run Postman-style validation rules (mandatory fields, valid statuses, lifecycle consistency).
6. **Reporting & Output**
   Generate CSV reports for issue types and API validation outcomes for easy review and handoff.

## 🧠 Data Quality Checks
* Verification of mandatory fields (e.g., `order_id`)
* Consistency checks on `order_status` values
* Validation of delivery dates against status
* Aggregation checks for payment anomalies
These steps ensure the dataset is reliable for analysis and simulation of API validations.

## 📈 Analytics Performed
* Distribution of orders by status
* Identification of cancelled orders with recorded payments
* Prioritization of high-value orders delayed beyond 5 days
* Flagging of orders by issue type (Cancelled, Delayed, OK)
* Simulation of API order payload validations with PASS/FAIL results
All analytics are performed using SQLite SQL and Python pandas workflows, ensuring compatibility with lightweight environments like Google Colab.

## 📂 Outputs
* **`retail_oms.db`** — The SQLite database file storing all ingested retail order data and intermediate query tables, enabling persistent and performant SQL analytics.
* `order_issue_report.csv` — Classified orders with flagged issues (Cancelled, Delayed, OK).
* `api_validation_report.csv` — Results of API payload validation tests with PASS/FAIL status.
* Executable SQL queries embedded within Python scripts for modular, reproducible analysis.
* Reproducible Google Colab notebook demonstrating the full pipeline.

## 🛠️ Tech Stack
* Python (Pandas, SQLite3)
* SQLite (SQL queries for analytics)
* Jupyter/Google Colab notebook for development & execution

## 🧠 Key Learnings
* Loading and cleaning structured retail order data
* Using SQLite for efficient SQL-based analysis in Python
* Combining SQL and Python to flag business-critical issues
* Simulating API data payloads and applying validation logic
* Generating professional reports and artifacts for stakeholder review

## 📁 Repository Structure
```
Order-Management-API-Validation/
│
├── data/
│   ├── orders.csv
│   ├── payments.csv
│   └── order_items.csv
│
├── notebooks/
│   └── order_management_analysis.ipynb
│
├── reports/
│   ├── order_issue_report.csv
│   └── api_validation_report.csv
│
├── retail_oms.db
├── README.md
└── requirements.txt
```

## 👩‍💻 Author
Arpa Kundu

## 📜 License
MIT License
If you want me to help generate any other part of this project — like resume bullets, interview explanations, or additional code snippets — just let me know!

