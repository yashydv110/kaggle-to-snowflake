# Kaggle to Snowflake ETL Project  

This project demonstrates how to extract a dataset from **Kaggle**, process it locally, and then load it into **Snowflake** for analysis.  
It is a simple **ETL (Extract, Transform, Load) pipeline** built in **Python** and **Jupyter Notebook**.  

---

## Project Structure  
- `ETL_Kaggle.ipynb` → Main Jupyter Notebook containing all steps  
- `.gitignore` → To ignore sensitive files (like API keys, credentials)  

---

## Steps Performed  

### 1. Kaggle Dataset Download  
- Authenticated with **Kaggle API**  
- Downloaded dataset: **Wine Reviews**  
- Extracted files to local folder  

### 2. Snowflake Connection  
- Connected to **Snowflake** using Python connector  
- Created **Database, Schema, Warehouse, and Table**  

### 3. Data Load  
- Loaded the Kaggle dataset into **Snowflake table** (`WINE_REVIEWS`)  
- Verified data using SQL queries  

---

## Output  
Kaggle dataset successfully loaded into **Snowflake**  
Table created: `KAGGLE_ETL.WINE_SCHEMA.WINE_REVIEWS`  
Data is available for querying and analysis  

---

## Future Enhancements  
- Automate pipeline using **Airflow** or **Prefect**  
- Add **data cleaning & transformation** steps  
- Build **Power BI / Tableau dashboards** on top of Snowflake  

---

## How to Run  

1. Clone the repository  
   ```bash
   git clone https://github.com/yashydv110/kaggle-to-snowflake.git
   cd kaggle-to-snowflake
