# BIG-DATA-ANALYSIS
COMPANY : CODTECH IT SOLUTIONS PVT.LTD
NAME : SURYA DAS MAHANTA
INTERN ID : CTIS8871
DOMAIN : DATA ANALYTICS
DURATION : 4 WEEKS 
MENTOR : NEELA SANTHOSH KUMAR

## Task 1: Amazon Product Data Analysis
### Objective
The goal of this task was to perform comprehensive Data Cleaning and Exploratory Data Analysis (EDA) on an Amazon product dataset using **PySpark** on a **Databricks Serverless** environment.

### Tech Stack
* **Language:** Python (PySpark)
* **Platform:** Databricks (2026 Free Edition)
* **Storage:** Unity Catalog (Volumes)
* **Compute:** Serverless SQL/Spark Engine

### Key Technical Challenges & Solutions
1. **Currency & Special Character Handling:** Used `regexp_replace` to strip symbols (₹, $) and commas from price columns to enable mathematical processing.
2. **Malformed Data Filtering:** Implemented `try_cast` to handle rows containing text (e.g., "60Hz Refresh Rate") in numeric fields, preventing system crashes.
3. **Delimiter Cleaning:** Cleaned inconsistent delimiters like `|` in the rating columns.
4. **Zero-Division Handling:** Resolved a `DIVIDE_BY_ZERO` error during Standard Deviation calculations for categories with single entries using `try_divide`.

### Insights Derived
* **Category Performance:** Developed a **Z-Score Rating Performance** metric to identify which product categories consistently outperform the average.
* **Pricing Strategy:** Identified the average price points for the top 5 most popular categories.

### How to Run
1. Upload the provided `.ipynb` file to your Databricks Workspace.
2. Connect to a **Serverless** or **All-Purpose** cluster.
3. Update the `file_path` variable to point to your data source in Unity Catalog.
