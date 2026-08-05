# RUSH Sportswear — Sales Analysis

<img src="https://github.com/hli2325/rush-sales-analysis/blob/main/RUSH%20logo.png?raw=true" width="200" alt="RUSH Logo">

Exploratory Data Analysis (EDA) for RUSH Sportswear (2020–2021).

---

## Project Overview

This repository analyzes raw sales data across 2020 and 2021 to answer 4 business questions, and identify sales growth trends.

---

## EDA Process
1. **Problem Definition:** Establish objectives and questions.
2. **Dataset Design & Creation:** Load datasets (`TABLE_PRODUCTS`, `TABLE_RETAILER`, `TABLE_SALES`).
3. **Data Inspection:** Check missing values, data types, typos, and outliers.
4. **Data Cleaning:**
   - Remove corrupt `***` text in `UNITS_SOLD` and convert to `int64`.
   - Remove `$99,999.0` price outlier and missing values in `UNIT_PRICE`.
   - Convert text `INVOICE_DATE` to `datetime64`.
   - Fix `SALES_METHOD` typo `Ootlet` to `Outlet`.
   - Create calculated `TOTAL_SALES` column (`UNITS_SOLD` * `UNIT_PRICE`).
   - Remove duplicate `RETAILER_ID` records in retailer table.
   - Merge cleaned datasets into master DataFrame `df_master`.

---

## Key Findings

|Question|Top Performer|Data|
|-|-|-|
|**1. Top Product (2021)** | Men's Street Footwear |\$22,649,400|
|**2. Top State - Women's (2021)** | Maine |\$2,176,301|
|**3. Top State - Men's (2021)** | Delaware |\$2,334,300|
|**4.1 Top Retailer (2020)** | Amazon | 316,880 units|
|**4.2 Top Retailer (2021)** | Foot Locker | 1,096,890 units|

---

## Market Insights

- **Financial Growth:** Total revenue grew **+296%** YOY from \$24.17M (2020) to \$95.89M (2021).
- **Sales Channels:** **Online** (\$44.93M) and **Outlet** (\$39.53M) channels lead revenue, outperforming **In-store** sales (\$35.60M).
- **Retail Partners:** Foot Locker became the top distributor in 2021 (1.09M units), surpassing 2020 leader Amazon (316.8K units).

---

## Repo Structure

```
├── RUSH_Sales_Analysis.ipynb    # Colab notebook
├── README.md                    # Repo documentation
├── .gitignore                   # Git ignore rules
├── RUSH logo.png                # Brand logo image
├── TABLE_PRODUCTS_885.csv       # Product table
├── TABLE_RETAILER_885.csv       # Retailer table
├── TABLE_SALES_885.csv          # Sales table
└── RUSH Data Dictionary.pdf     # Data dictionary
```

---

## How to Run

1. Open `RUSH_Sales_Analysis.ipynb` in Google Colab or Jupyter Notebook.
2. Run all cells sequentially.
