# Vendor Performance Analysis

## 📌 Project Overview
This project evaluates vendor performance and inventory efficiency in a retail/wholesale setting. It identifies underperforming brands, quantifies vendor contributions to sales and profit, measures the impact of bulk purchasing, flags slow-moving inventory, and statistically compares profitability models across vendor groups.

**Core business questions**
- Which vendors/brands are underperforming and need pricing or promotional adjustments?
- Who are the top vendors by sales and profitability?
- How much do bulk purchases reduce unit costs?
- Which vendors contribute to unsold inventory and poor stock turnover?
- Are there statistically significant differences between high- and low-performing vendors?

## 🧾 Business Context
Companies risk margin erosion due to inefficient pricing, low inventory turnover, over-reliance on a few vendors, and obsolete stock. This repo provides a data-driven approach to mitigate these risks and improve decision-making.

## 📂 Repository Structure
```
📁 Project Root
│── vendor_sales_summary.csv         # Final curated dataset (analysis-ready)
│── ingestion_db.py                  # Ingests all CSVs from ./data into SQLite (inventory.db)
│── get_vendor_summary.py            # Builds vendor summary from base tables and computes KPIs
│── Exploratory Data Analysis.ipynb  # Data cleaning & EDA
│── Vendor Performance Analysis.ipynb# In-depth statistical/business analysis
│── Vendor Performance Report.pdf    # Business-facing report with findings & recommendations
│── vendor_performance.pbix          # Power BI dashboard (interactive)
│── images/                          # Screenshots for README (generated)
└── data/                            # (Optional) Raw CSVs used by ingestion script
```

## 🔍 Key Findings (high level)
- **Underperforming Brands**: ~198 brands show low sales but high margins → candidates for targeted promos / price optimization.
- **Vendor Concentration Risk**: Top 10 vendors ≈ 66% of purchases → diversify to reduce supply chain risk.
- **Bulk Purchasing**: Large orders achieve ≈ 72% lower unit costs → supports bulk-buy strategy.
- **Inventory Exposure**: ≈ $2.71M tied up in unsold inventory → optimize purchase quantities/clearances.
- **Profitability Models Differ**: High-margin vendors vs. top-selling vendors differ significantly (hypothesis test rejects H₀).

> See **Vendor Performance Report.pdf** and the notebooks for full details.

## 📊 Visual Highlights
Below are selected visuals from the report / dashboards. (If these are placeholders, replace with your actual screenshots in `/images`.)

<img width="1530" height="1980" alt="vendor_report_page_1" src="https://github.com/user-attachments/assets/26f2b949-a8d2-407a-9576-15ed85b9ec1b" />
<img width="1530" height="1980" alt="vendor_report_page_2" src="https://github.com/user-attachments/assets/f6aade12-a6a9-4cab-a566-47b609c5cf27" />
<img width="1530" height="1980" alt="vendor_report_page_3" src="https://github.com/user-attachments/assets/f23283e8-982d-4a10-81ff-b9cb1a79cad8" />


## ⚙️ Tech Stack
- **Python**: pandas, numpy, matplotlib/seaborn for EDA and modeling
- **SQLite**: lightweight DB for ingestion & analysis
- **Jupyter Notebooks**: reproducible analysis
- **Power BI**: interactive stakeholder-ready dashboards

## 🧮 Key KPIs (computed in `get_vendor_summary.py`)
- **GrossProfit** = TotalSalesDollars − TotalPurchaseDollars  
- **ProfitMargin** = (GrossProfit / TotalSalesDollars) × 100  
- **StockTurnover** = TotalSalesQuantity / TotalPurchaseQuantity  
- **SalesToPurchaseRatio** = TotalSalesDollars / TotalPurchaseDollars  

## 🧠 Methodology Notes
- Robust EDA to identify outliers, zero/negative margins, and slow movers.
- Data cleaning with safe divisions and NA handling.
- Correlation analysis to understand price vs. sales/profit dynamics.
- Hypothesis testing to validate profitability differences.

## ✅ Recommendations (business-facing)
- Re-price and promote **low-sales, high-margin** brands to grow volume.
- **Diversify vendors** to reduce supply-chain concentration risk.
- Use **bulk purchase** levers where feasible to maintain a cost advantage.
- **Liquidate or right-size** slow-moving inventory to free working capital.
- Improve marketing/distribution for low-performing vendors to lift sales without margin damage.

## 🗂️ Credits & Files to Review First
- Start with **Vendor Performance Report.pdf** for an executive read.
- Then scan **Vendor Performance Analysis.ipynb** for the analytical backbone.
- `get_vendor_summary.py` shows the KPI computations used throughout.

---

> **Tip**: If your audience can’t open `.pbix`, add PNGs of the Power BI pages to `/images` and reference them above.
> Consider adding a short Loom/GIF walkthrough of the dashboard.

