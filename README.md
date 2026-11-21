# Excel Sales Performance Dashboard (2022–2025)

An interactive Excel dashboard for exploring sales, profitability, product-category performance, sales channels, and geographic sales patterns using a **synthetic** transaction dataset.

![Sales dashboard overview](images/dashboard_overview.png)

## Project overview

This portfolio project demonstrates how transaction-level business data can be summarized into actionable performance views. It includes year selection and visual comparisons across months, product categories, sales channels, and countries.

## Dataset

- **Source:** Synthetic sales transaction CSV, included in `dataset/`.
- **Period:** 2022–2025.
- **Records:** 18,045 transaction rows, 36 columns.
- **Example fields:** `Order_ID`, `Order_Date`, `Order_Year`, `Product_Category`, `Sales_Channel`, `Country`, `Quantity`, `Sales_Amount`, `Cost_Amount`, `Profit`, and `Order_Status`.

## Dashboard KPIs (all years)

| Metric | Value | Definition |
| --- | ---: | --- |
| Unique orders | 14,541 | Distinct `Order_ID` values |
| Units sold | 38,384 | Sum of `Quantity` |
| Recorded sales | $8,252,141.40 | Sum of `Sales_Amount` |
| Recorded profit | $1,649,387.54 | Sum of `Profit` |
| Average order value | $567.51 | Recorded sales / unique orders |

## Features

- Year dropdown: All Years, 2022, 2023, 2024, 2025 (`DASHBOARD!S4`).
- KPI cards for orders, units, sales, profit, and average order value.
- Monthly sales trend line chart.
- Product-category sales pie chart.
- Sales-channel comparison bar chart.
- Country-level sales comparison column chart.
- Dark-green navigation-style sidebar and consistent dashboard styling.

## Tools and methodology

- **Microsoft Excel** (`.xlsx`) for presentation, formulas, charts, and year selection.
- Source transactions were aggregated by year, month, category, channel, and country into the `Dashboard Data` sheet.
- Dashboard KPIs use formulas referencing those precomputed summaries.
- The workbook contains summarized data; the original transaction-level CSV is supplied separately.

## How to use

1. Download `dashboard/Sales_Performance_Dashboard.xlsx` and open it in Microsoft Excel.
2. Open the **DASHBOARD** sheet.
3. Select a year in the dropdown at cell **S4**, or choose **All Years**.
4. Review the updated KPI cards and charts.
5. Use `Dashboard Data` for supporting aggregates and `READ ME` for metric definitions.

> The sidebar labels are decorative, not working navigation buttons. Adding new CSV rows does not automatically refresh the workbook; the summary tables must be regenerated.

## Important limitations

- This project uses **synthetic data** and is intended for learning and portfolio demonstration, not actual business reporting.
- All order statuses are included in the displayed aggregates. The dashboard label **Net Sales** reflects the source field `Sales_Amount`; it should not be treated as accounting net revenue after independently excluding cancellations and returns.
- Distinct order counts across different years are not necessarily additive if an order ID appears in multiple years.
- Findings are descriptive and do not establish causation.

## Repository contents
```text
Excel-Sales-Performance-Dashboard/
├── README.md
├── dataset/
│   └── Sales_transactions_2022_2025.csv
├── dashboard/
│   └── Sales_Performance_Dashboard.xlsx
├── images/
│   ├── dashboard_overview.png
│   └── dashboard_2025.png
└── docs/
    └── Project_Documentation.md
```
## Portfolio purpose

Created to practice Excel-based data analysis, KPI design, business reporting, and data visualization. Screenshots demonstrate the interface; open the Excel workbook for working year-based interaction.
