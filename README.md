# Vendor Performance Analysis

## 📌 Project Overview
This project evaluates vendor performance and inventory efficiency in a retail/wholesale setting. It identifies underperforming brands, quantifies vendor contributions to sales and profit, measures the impact of bulk purchasing, flags slow-moving inventory, and statistically compares profitability models across different vendor groups.

**Core business questions**
- Which vendors/brands are underperforming and need pricing or promotional adjustments?
- Who are the top vendors by sales and profitability?
- How much do bulk purchases reduce unit costs?
- Which vendors contribute to unsold inventory and poor stock turnover?
- Are there statistically significant differences between high- and low-performing vendors?

## 🧾 Business Context
Companies risk profit decline due to inefficient pricing, low inventory turnover, over-reliance on a few vendors, and dead inventory. This repo provides a data-driven approach to mitigate these risks and improve decision-making.

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

## 🔍 Key Findings
- **Underperforming Brands**: ~198 brands show low sales but high margins → candidates for targeted promos / price optimization.
- **Vendor Concentration Risk**: Top 10 vendors ≈ 66% of purchases → diversify to reduce supply chain risk.
- **Bulk Purchasing**: Large orders achieve ≈ 72% lower unit costs → supports bulk-buy strategy.
- **Inventory Exposure**: ≈ $2.71M tied up in unsold inventory → optimize purchase quantities/clearances.
- **Profitability Models Differ**: High-margin vendors vs. top-selling vendors differ significantly (hypothesis test rejects H₀).

> See **Vendor Performance Report.pdf** and the notebooks for full details.

## 📊 Visual Highlights
Below are selected visuals from the report / dashboards. 
<img width="488" height="280" alt="Screenshot 2025-09-23 at 13 04 18" src="https://github.com/user-attachments/assets/4b2ae91b-aa43-408b-a318-aa1871635af4" />
<img width="597" height="716" alt="Screenshot 2025-09-23 at 13 02 21" src="https://github.com/user-attachments/assets/c3505909-1813-4749-a940-230ce3a1ad64" />
<img width="870" height="476" alt="Screenshot 2025-09-23 at 13 01 38" src="https://github.com/user-attachments/assets/aaf3afe5-9eb5-489b-8d01-efacf1cafd45" />
<img width="555" height="548" alt="Screenshot 2025-09-23 at 13 02 42" src="https://github.com/user-attachments/assets/24810533-7ec9-454f-872f-c601aa2ecd31" />



## ⚙️ Tech Stack
- **Python**: pandas, numpy, matplotlib/seaborn for EDA and modeling
- **SQLite**: light DB for ingestion & analysis
- **Jupyter Notebooks**: reproducible analysis
- **Power BI**: interactive dashboards

## 🧮 KPIs (computed in `get_vendor_summary.py`)
- **GrossProfit** = TotalSalesDollars − TotalPurchaseDollars  
- **ProfitMargin** = (GrossProfit / TotalSalesDollars) × 100  
- **StockTurnover** = TotalSalesQuantity / TotalPurchaseQuantity  
- **SalesToPurchaseRatio** = TotalSalesDollars / TotalPurchaseDollars  

## 🧠 Methodology Notes
- EDA to identify outliers, zero/negative margins, and slow movers.
- Data cleaning with safe divisions and NA handling.
- Correlation analysis to understand price vs. sales/profit dynamics.
- Hypothesis testing to validate differences in profitability.

## ✅ Recommendations (business-facing)
- Re-price and promote **low-sales, high-margin** brands to grow volume.
- **Diversify vendors** to reduce supply-chain concentration risk.
- Use **bulk purchase** levers where feasible to maintain a cost advantage.
- **Liquidate or right-size** slow-moving inventory to free working capital.
- Improve marketing/distribution for low-performing vendors to lift sales without margin damage.

## 🗂️ Credits & Files to Review First
- Start with **Vendor Performance Report.pdf** for an executive read.
- Then scan **Vendor Performance Analysis.ipynb** for the analytics part. 
- `get_vendor_summary.py` shows the KPI computations used throughout.

## 👤 About Me
Hi, I’m **Niyog Uprety** — an aspiring **Data Scientist**.  

- 🎓 Undergraduate student in **Data Science**  
- 📊 Passionate about turning raw data into actionable insights and building real-world analytics solutions  
- 🌱 Currently working on projects that combine **finance, data, and machine learning**  
- 💼 Open to internships and collaborations in **data analytics, data engineering, or quant research**  

📬 **Let’s connect:**  
- [LinkedIn](https://www.linkedin.com/in/niyog-uprety-177b9621a/)    
- ✉️ Email: upretyyniyog@gmail.com




