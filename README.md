# Personal-Project-Superstore

# Project Summary
This project explores retail sales performance using a cleaned version of the Superstore dataset. 

The goal was to take a real‑world, imperfect dataset and turn it into something structured, reliable, and ready for analysis. I used the Pandas library within Python to clean and prepare the data, SQL to extract key metrics, and Tableau to visualise insights in a clear and meaningful way.

This dataset was chosen as I found it intriguing to investigate the major profitable categories as welll as the differences between the areas in the USA market.

# Project Structure
```md
├── Data/
│   ├── Superstore_Raw.csv                 # Original dataset
│   ├── Superstore_Cleaned.csv             # Cleaned via Pandas
│   └── Superstore_Subset.csv              # SQL-filtered data for Tableau
├── Notebook/
│   └── Superstore_Data_Cleaning.ipynb     # Pandas cleaning code
├── Sql/
│   ├── Create_Table.sql                   # MySQL schema
│   ├── Load_Data.sql                      # Data ingestion script
│   └── Select_For_Tableau.sql             # SQL query for specific columns
├── Tableau/
│   └── Superstore_Visualisations.twbx     # Packaged workbook (3 sheets + dashboard)
└── README.md                              # Project documentation
```
# Data Cleaning (Python/Pandas)
The raw dataset contained misaligned rows and inconsistent formatting. 

The following steps ensured the dataset was cleaned and prepared for the next stages of analysis:

1. Imported the Pandas library and mounted Google Drive to access the dataset before loading it into a Pandas DataFrame.
   
2. The raw CSV file was loaded using `latin1` encoding to avoid any decoding issues.
   
3. Duplicate rows were checked and confirmed to be zero.

4. The `Order Date` and `Ship Date` columns were converted to datetime formats so that date-based analysis will work correctly.

6. Columns such as `Sales`, `Quantity`, `Discount`, and `Profit` were converted to numeric types to ensure proper numeric values.

7. The cleaned data was saved into a new file under a new name.

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
