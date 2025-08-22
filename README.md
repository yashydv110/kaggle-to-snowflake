# Kaggle to Snowflake ETL Project

This project demonstrates how to extract a dataset from **Kaggle**, process it locally, and then load it into **Snowflake** for analysis.  
It is a simple ETL (Extract, Transform, Load) pipeline built in Python and Jupyter Notebook.

---

## Project Structure

- `Kaggle_to_Snowflake_ETL.ipynb` → Main Jupyter Notebook containing all steps  
- `.gitignore` → To ignore sensitive files (like keys, creds)  
- `requirements.txt` → Python dependencies  

---

## Steps Performed

1. **Kaggle Dataset Download**  
   - Authenticated with Kaggle API  
   - Downloaded dataset: [Wine Reviews](https://www.kaggle.com/datasets/zynicide/wine-reviews)  
   - Extracted files to local folder  

2. **Snowflake Connection**  
   - Connected to Snowflake using Python connector  
   - Created database, schema, warehouse, and table  

3. **Data Load**  
   - Loaded the Kaggle dataset into Snowflake table (`WINE_REVIEWS`)  
   - Verified data using SQL queries  

---

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/yashydv110/kaggle-to-snowflake.git
cd kaggle-to-snowflake


### 2. Create Virtual Environment (Optional but Recommended)
python3 -m venv venv
source venv/bin/activate

### 3. Install Dependencies
pip install -r requirements.txt

### 4. Configure Kaggle API

Place your kaggle.json file in:

~/.kaggle/kaggle.json


Make sure correct permissions are set:

chmod 600 ~/.kaggle/kaggle.json

### 5. Configure Snowflake

Update your Snowflake credentials in the notebook:

user = "<YOUR_USERNAME>"
password = "<YOUR_PASSWORD>"
account = "<YOUR_ACCOUNT>.snowflakecomputing.com"
warehouse = "COMPUTE_WH"
database = "KAGGLE_ETL"
schema = "WINE_SCHEMA"

### 6. Run the Notebook

Open the Jupyter Notebook and execute all cells:

jupyter notebook ETL_Kaggle.ipynb

## Output

Kaggle dataset successfully loaded into Snowflake

Table created: KAGGLE_ETL.WINE_SCHEMA.WINE_REVIEWS

Queries can now be run in Snowflake to analyze the data

## Future Enhancements

Automate pipeline using Airflow or Prefect

Add data cleaning & transformation

Build Power BI / Tableau dashboard using Snowflake data

##Author
##Yash Yadav
