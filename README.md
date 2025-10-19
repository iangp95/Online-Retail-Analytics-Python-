# 🛍️ Online Retail — Exploratory Data Analysis

*Project:* Online Retail EDA (Coursera Portfolio Project)  
*Source notebook:* `online_retail.ipynb` (Coursera). See original assignment for dataset details. :contentReference[oaicite:1]{index=1}

---

## Overview

This project explores transactional data from an online retail store (2010–2011). The goal is to uncover sales trends, customer behaviour, and product performance to drive actionable recommendations for merchandising, marketing, and operations.

**Dataset**: `Online Retail.xlsx` (UCI / Coursera environment)  
**Tools**: Python, pandas, matplotlib, seaborn

---

## Key Metrics (summary)

- **Total Revenue:** `£{total_revenue:,.2f}`
- **Unique Customers:** `{total_customers:,}`
- **Total Orders (invoices):** `{total_orders:,}`
- **Total Items Sold:** `{total_items_sold:,}`

> *Note: numbers above are auto-filled by the notebook. See the "How to regenerate" section for instructions.*

---

## Performance Highlights

| Category   | Top Performer                                 | Value |
|------------|-----------------------------------------------|-------|
| **Month**  | `{top_month}`                                  | `£{top_month_value:,.0f}` |
| **Weekday**| `{top_weekday}`                                 | `£{top_weekday_value:,.0f}` |
| **Country**| `{top_country}`                                 | `£{top_country_value:,.0f}` |
| **Product**| `{top_product_name}`                            | `£{top_product_value:,.0f}` |

---

## Key Insights

- The dataset shows **strong seasonality**, with a clear revenue peak during **{top_month}**.
- **{top_weekday}** has the highest revenue among weekdays — useful timing for promotions.
- The top market is **{top_country}**, which contributes a disproportionate share of revenue.
- The single top revenue product is **{top_product_name}**, indicating a high-impact SKU.

---

## Business Recommendations

1. **Ramp inventory** ahead of {top_month} (seasonality window) to avoid stockouts.  
2. **Target marketing** and promotions to exploit weekday peaks (e.g., {top_weekday} campaigns).  
3. **Market prioritization**: invest in logistics and localization for {top_country}.  
4. **SKU strategy**: bundle or cross-sell {top_product_name} with slower-moving items.  
5. **Customer retention**: use RFM segments (generated in the notebook) to target high-value customers with loyalty offers.

---

## Visualizations & Files

- `daily_revenue.png` — Daily revenue time series  
- `monthly_revenue.png` — Monthly revenue bar chart  
- `top_products_by_revenue.png` — Top products (by revenue) barh  
- `hour_weekday_heatmap.png` — Hour-of-day vs weekday revenue heatmap  
- `top_products_by_revenue.csv` — raw CSV export of top products by revenue  
- `rfm_customers.csv` — RFM table for customer segmentation

*(If you run the notebook, these files are saved to the working directory.)*

---

## How to regenerate this README from the notebook

1. Run the notebook cells to compute `total_revenue`, `total_customers`, `total_orders`, `total_items_sold`, `rev_by_month`, `rev_by_weekday`, `country_sales`, and `top_by_revenue`.  
2. Run the "Save README" cell (example provided in the notebook) — it will auto-generate a fresh `README.md` with up-to-date numbers and top performers.

---

## Next steps / Advanced analyses

- Cohort retention analysis to track repeat purchase rates.  
- Time-series forecasting to predict next-quarter demand.  
- Margin & profitability analysis (requires cost data).  
- Predictive modeling for customer lifetime value or churn.

---

## Notes & Data cleaning decisions

- Rows with non-positive `Quantity` or `UnitPrice` were removed (likely returns or errors).  
- Invoice rows beginning with `'C'` were removed as cancelled orders.  
- Outliers were identified using IQR and reported, but can be included/excluded depending on analysis needs.

---

## Acknowledgements

Project adapted from Coursera's *Online Retail EDA* assignment. Dataset: `Online Retail.xlsx` (UCI / Coursera). :contentReference[oaicite:2]{index=2}
