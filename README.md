# Superstore_sales_Data
# 📊 Superstore Sales & Profitability Analysis

An end-to-end data analytics project: exploratory data analysis in **Python** (pandas, matplotlib, seaborn) combined with an interactive **Power BI** dashboard, built on the classic Superstore retail dataset (2014–2017).

The goal: figure out where sales and profit actually come from, where the business is quietly losing money, and whether discounting is helping or hurting margin.

---

## 🧾 Project Overview

| | |
|---|---|
| **Dataset** | Superstore retail transactions (9,994 rows, 22 columns) |
| **Time range** | Jan 2014 – Dec 2017 |
| **Tools** | Python (pandas, matplotlib, seaborn), Power BI Desktop (Power Query, DAX) |
| **Deliverables** | Jupyter notebook (EDA), Power BI dashboard (.pbix), full analysis report |

---

## 🗂️ Repo Contents

```
├── Supersstore.ipynb              # Python EDA: cleaning, KPIs, visualizations
├── SuperstoreDashboard.pbix       # Interactive Power BI dashboard
├── updated_superstore.csv         # Cleaned dataset (with parsed dates)
├── Superstore_Analysis_Report.docx # Full write-up: insights, KPIs, recommendations
└── README.md
```

---

## ❓ Business Problem

A retail chain wants a self-service view answering:
- Which categories, sub-categories, and regions drive the most revenue and profit?
- Are any product lines consistently unprofitable — and by how much?
- Is discounting helping win sales, or eroding margin?
- How has performance trended over time?
- Who are the top customers and best-selling products?

---

## 🔑 Key KPIs

| KPI | Result |
|---|---|
| Total Sales | $2,297,200.86 |
| Total Profit | $286,397.02 |
| Profit Margin | 12.47% |
| Total Orders | 5,009 |
| Average Order Value | $458.61 |
| Average Discount | 15.62% |
| Top Category (Sales) | Technology ($836,154) |
| Top Sub-Category (Sales) | Phones ($330,007) |
| Top Sales Year | 2017 ($733,215) |
| Top Region (Sales) | West ($725,458) |

---

## 💡 Key Insights

- **Technology** leads in sales, but revenue leadership ≠ profitability.
- **Tables, Bookcases, and Supplies** are actively losing money (Tables alone: –$17,725).
- **Discount and Profit are negatively correlated** (r ≈ –0.22) — heavy discounting is quietly killing margin, especially above ~30–40%.
- **2017 was the strongest year**, with consistent year-over-year growth since 2014.
- The **West region** outperforms all others; **South** trails behind.

Full breakdown, charts, and recommendations are in `Superstore_Analysis_Report.docx`.

---

## 🛠️ How It Was Built

1. **Data cleaning (Python)** — loaded with `latin1` encoding, converted `Order Date`/`Ship Date` to datetime, handled scientific-notation display issues with `pd.set_option`.
2. **EDA (Python)** — grouped aggregations by Category, Sub-Category, Region, Segment; flagged loss-making sub-categories; built 7 matplotlib/seaborn visualizations including a discount-vs-profit scatter plot.
3. **Dashboard (Power BI)** — imported the cleaned CSV, fixed a Sales-column data-type issue (Text → Decimal Number), built reusable DAX measures for dynamic "Top N" KPI cards (`CALCULATE` + `SELECTEDVALUE` + `TOPN`), and added Category/Sub-Category/Year slicers for interactive filtering.

---

## 🚀 Running It Yourself

**Python notebook**
```bash
pip install pandas matplotlib seaborn
jupyter notebook Supersstore.ipynb
```

**Power BI dashboard**
1. Open `SuperstoreDashboard.pbix` in [Power BI Desktop](https://www.microsoft.com/power-platform/products/power-bi/downloads) (Windows only)
2. Use the slicers on the report page to filter by Category, Sub-Category, or Year

---

## 📌 Recommendations

- Cap or restructure discounts on **Tables** and **Bookcases** — the biggest source of realized losses.
- Set a max discount threshold (e.g. 20%) where the discount–profit relationship is strongest negative.
- Double down on **Technology** and **Phones** — the strongest performers by sales.
- Investigate the **South region's** underperformance relative to West/East.

---

## 📬 Contact

Feel free to open an issue or reach out if you have questions about the approach or want to suggest improvements.
