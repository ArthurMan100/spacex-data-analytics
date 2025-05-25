# 🚀 SpaceX Launch Data Pipeline

This project extracts, transforms, and loads SpaceX launch data using a structured ETL pipeline. It also includes a Power BI report for visual analysis.

---

## 📁 Project Structure
```
├── Extract_Data/
│ ├── extract_api.ipynb # Extracts launch data via SpaceX API
│ └── extract_web.ipynb # (Optional) Web scraping version
│
├── Transform_Data/
│ ├── transform_api.ipynb # Cleans API data, removes nulls, adds metrics
│ └── transform_web.ipynb # Transforms scraped data similarly
│
├── Load_Data/
│ └── load_to_postgres.ipynb # Loads transformed data into PostgreSQL
│
├── Power_BI/
│ └── spacex_report.pbix # Power BI report for data analysis
│
│── raw_data
│
│── clean_data
│
└── README.md
```
---

## 🔧 Pipeline Overview

### ✅ Extract
- Pulls SpaceX launch data using the SpaceX REST API.
- `extract_web.ipynb` provides a web scraping fallback.

### 🔄 Transform
- Removes null values, standardizes fields.
- Adds custom metrics to determine launch success/failure.
- Two versions depending on data source: API or Web.

### 📥 Load
- Loads the clean, structured data into a PostgreSQL database.
- Easily integrates with BI tools for downstream analytics.

### 📊 Visualize
Explore the insights in `Power_BI/spacex_report.pbix`, including:
- Launch frequency & trends
- Success vs. failure rates
- Breakdown by rocket, location, and more

---

## 🚀 Getting Started

### 1. Clone the repository:
```
git clone https://github.com/ArthurMan100/spacex-data-analytics.git
cd spacex-etl-pipeline
```
### 2. Install dependencies
pip install -r requirements.txt

### 3. Set up environment variables (in a .env file)
```
DB_PORT=5432
DB_PASSWORD=your_password
```
### 4. Run notebooks in order

Extract: extract_api.ipynb or extract_web.ipynb

Transform: transform_api.ipynb or transform_web.ipynb

Load: load_to_postgres.ipynb

### 5. Open Power BI Report

Navigate to the Power_BI folder.

Open spacex_report.pbix with Power BI Desktop.

### 🛠 Setup Requirements
##✅ Prerequisites
Python 3.11.5 or higher

PostgreSQL installed and running

A PostgreSQL database created (e.g., named spacex_db)

A table will be created automatically during the load phase if not present















