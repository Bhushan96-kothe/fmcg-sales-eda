# FMCG Sales — Exploratory Data Analysis

End-to-end Python EDA project on a synthetic FMCG sales dataset: 9,000+ orders across dairy, beverages, snacks, personal care, and home care categories, spanning 2024–2025 across 5 Indian regions.

## Dataset

`fmcg_sales_data.csv` — 16 columns including Date, Region/State/City, Channel, Category/Brand/SKU, Units_Sold, MRP, Discount_Pct, Selling_Price, Revenue, Distributor, Sales_Rep.

The data intentionally includes realistic quality issues — duplicate rows, missing values, negative unit-sold entries, and inconsistent text formatting — to demonstrate data cleaning, not just charting.

## What this project covers

- **Data cleaning:** datetime parsing, deduplication, text standardization, missing-value imputation, outlier handling (negative values + IQR-based detection)
- **Aggregation:** category/region/channel-level revenue summaries using `groupby` and `pivot_table`
- **Time series:** monthly revenue trend, category-level seasonality
- **Statistical analysis:** correlation between discount percentage and units sold
- **Visualization:** bar charts, heatmaps, multi-line trend charts, scatter plots (matplotlib)

## Key insights

- Ice cream/beverages sales peak **April–June** (summer seasonality); snacks and home care spike **October–November** (festive season)
- Discount percentage shows **weak/near-zero correlation** with units sold — discounting alone doesn't reliably drive volume
- General Trade is the highest-revenue channel across all regions; HoReCa the lowest
- A small set of outlier orders (identified via IQR) disproportionately skew total revenue and warrant further investigation

## Tools

Python, pandas, matplotlib, NumPy

## Structure

fmcg-sales-eda/
├── fmcg_sales_data.csv # raw dataset
├── fmcg_sales_cleaned.csv # cleaned output
├── eda_notebook.ipynb # full analysis notebook
└── README.md
