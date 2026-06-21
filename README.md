# E-Commerce Order Analytics: Revenue Trends, Patterns & Outlier Detection

## Overview
This project analyses an e-commerce order dataset (1,200 transactions spanning January 2023 – June 2025) to identify revenue trends, product performance patterns, and anomalous orders. Using Python's data analytics stack, the analysis covers descriptive statistics, time-series trend analysis, categorical cross-tabulation, IQR-based outlier detection, and correlation analysis between order attributes.

## Key Findings
- **Revenue trend:** Total revenue declined year-over-year — $553k (2023) → $480k (2024) → $232k (2025, partial year through June).
- **Top performers:** Chair and Printer generated the highest total revenue (~$195k each), while Laptop had the highest average order value at $1,111.
- **Outliers:** Identified 8 outlier orders (all priced between $3,334–$3,456) using the IQR method. These were driven by bulk quantity (5 units) combined with high unit price, not data entry errors.
- **Referral channels:** Instagram was the strongest referral source by both order volume and revenue.
- **Data integrity:** Zero duplicate rows, zero negative values, and `TotalPrice` matched `Quantity × UnitPrice` across all 1,200 rows.

## Tools & Methods
- **Language:** Python
- **Libraries:** Pandas, Matplotlib, Seaborn, OpenPyXL
- **Techniques:** Groupby aggregation, cross-tabulation, time-series resampling, IQR outlier detection, correlation analysis

## Visualisations
| Chart | Description |
|-------|-------------|
| `chart_1_monthly_revenue_trend.png` | Monthly revenue trend (Jan 2023 – Jun 2025) |
| `chart_2_revenue_by_product.png` | Total revenue by product category |
| `chart_3_order_status_distribution.png` | Order status distribution (Pending, Shipped, Delivered, Cancelled, Returned) |
| `chart_4_outlier_boxplot.png` | Boxplot showing outlier orders in `TotalPrice` |
| `chart_5_correlation_heatmap.png` | Correlation heatmap between Quantity, UnitPrice, ItemsInCart, and TotalPrice |

## Project Structure
```
├── Data_Analytics_project_2.ipynb     # Full analysis notebook
├── Dataset_for_Data_Analytics.xlsx    # Source dataset
├── chart_1_monthly_revenue_trend.png
├── chart_2_revenue_by_product.png
├── chart_3_order_status_distribution.png
├── chart_4_outlier_boxplot.png
├── chart_5_correlation_heatmap.png
└── README.md
```

## How to Run
```bash
pip install pandas matplotlib seaborn openpyxl jupyter
jupyter notebook Data_Analytics_project_2.ipynb
```

## Analysis Steps
1. Data loading and exploration (shape, dtypes, summary statistics)
2. Pattern discovery via groupby aggregation and cross-tabulation
3. Time-series trend analysis (monthly and yearly revenue)
4. Outlier detection using the IQR method (1.5× interquartile range)
5. Visualisation of trends, distributions, and correlations

## Author
**Karthik Kannapiran**
MSc Data Science & Analytics, Maynooth University
[LinkedIn](https://www.linkedin.com/in/karthik-kannapiran-576540211) | kannapirankarthik2@gmail.com
