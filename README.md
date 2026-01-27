# Personal-Project-Superstore

# Project Summary
This project explores retail sales performance using a cleaned version of the Superstore dataset. 

The goal was to take a real‑world, imperfect dataset and turn it into something structured, reliable, and ready for analysis. I used the Pandas library within Python to clean and prepare the data, SQL to extract key metrics, and Tableau to visualise insights in a clear and meaningful way.

This dataset was chosen as I found it intriguing to investigate the major profitable categories as welll as the differences between the areas in the USA market.

# Project Structure
```md
├── data/
│   ├── superstore_raw.csv                 # Original dataset
│   ├── superstore_cleaned.csv             # Cleaned via Pandas
│   └── superstore_tableau_export.csv      # SQL-filtered data for Tableau
├── notebook/
│   └── data_cleaning.ipynb                # Pandas cleaning code
├── sql/
│   ├── create_table.sql                   # MySQL schema
│   ├── load_data.sql                      # Data ingestion script
│   └── select_for_tableau.sql             # SQL query for specific columns
├── tableau/
│   └── superstore_visualisations.twbx     # Packaged workbook (3 sheets + dashboard)
└── README.md                              # Project documentation
```
# Data Cleaning (Python/Pandas)
The raw dataset contained misaligned rows and inconsistent formatting. 

Using the Pandas library, I loaded the file with, ensured it is cleaned and then exported columns within the clean CSV suitable for SQL import. This ensured the dataset was consistent, structured, and ready for analysis.

1. Imported Pandas and mounted Google 
   Mounted Google Drive to access the dataset and loaded it into a Pandas DataFrame.
   
2. Loaded the dataset
   The raw CSV file was loaded using `latin1` encoding to avoid any decoding issues.
   
3. Check for duplicates
   Duplicate rows were checked and confirmed to be zero.

4. Convert date columns
   The `Order Date` and `Ship Date` columns were converted to datetime formats so that date-based analysis will work correctly.

5. Convert numeric columns
   Columns such as `Sales`, `Quantity`, `Discount`, and `Profit` were converted to numeric types to ensure proper numeric values.

6. Export cleaned dataset
   The cleaned data was saved into a new file under a new name.

# SQL Analysis
  To prepare the dataset for analysis and visualisation, I followed a structured SQL workflow:

1. Created the database table using a custom schema with the correct field types and stored it in a database called `data` in SQL.

2. Loaded the cleaned CSV into MySQL using `LOAD DATA INFILE`.
  
3. Selected using `SELECT` and exported specific columns from the database for Tableau visualisation.

# Tableau Visualisation
  <img width="1665" height="769" alt="image" src="https://github.com/user-attachments/assets/b9b4c761-b65a-47fe-ad0a-6baaf4c87411" />

# Key Insights
**Top 5 Sub-Categories by Sales:** Phones and Chairs consistently  lead in sales, showing steady year-over-year growth. ​Binders and Storage are emerging as strong secondary performers by late 2017.​

**Profit by Region:** ​The West and East region of the United Sates drive the majority of company profit. ​The Central region is the lowest performer, indicating a need for strategic review or targeted marketing.​

**Sales over Time:** Total sales show strong seasonality with significant peaks in Q4 each year which is not a surprise to me as this is the period where there are usually offers due to the festive periods.​Overall, the business achieved a record-high revenue of over $280,000 in the final quarter of 2017.

# 🎯 Business Impact
Identified high‑performing product categories for potential expansion

Highlighted underperforming regions requiring strategic review

Revealed seasonal patterns that can guide inventory and marketing planning
