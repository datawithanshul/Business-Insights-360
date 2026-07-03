# 📊 Business Insights 360

An end-to-end **Power BI Dashboard** developed using the **AtliQ Hardware** dataset to deliver actionable insights across **Finance, Sales, Marketing, Supply Chain, and Executive** business functions.

The dashboard enables stakeholders to monitor KPIs, evaluate business performance, identify growth opportunities, and make data-driven decisions through interactive visualizations.

---

# 🏢 Company Overview

**AtliQ Hardware** *(an imaginary company)* is a rapidly growing **consumer electronics** company specializing in hardware products such as **PC accessories, printers, and peripheral devices**. Over the years, AtliQ has expanded its operations globally, establishing a strong presence across key markets, including **APAC, North America, Latin America, and the European Union**.

The company distributes its products through two primary sales platforms:

- 🏬 **Brick-and-Mortar Stores** – Partnering with leading physical retail chains such as **Croma** and **Best Buy**.
- 🛒 **E-Commerce Platforms** – Selling products through major online marketplaces such as **Amazon** and **Flipkart**.

AtliQ operates through multiple sales channels:

- 🛍️ **Retailers** – Third-party online and offline sellers that stock and sell AtliQ products.
- 🏪 **Direct Stores** – Company-owned stores where customers can purchase products directly.
- 🚚 **Distributors** – In restricted markets such as **China** and **South Korea**, AtliQ partners with authorized distributors to ensure product availability.

> **Note:** AtliQ's direct customers are **retailers** and **distributors**, while the **end consumers** are the final users of its products.

---

# 🔎 Problem Statement

As a rapidly growing company, **AtliQ Hardware** relied heavily on scattered **Microsoft Excel** files for business reporting and analytics. This fragmented approach made it difficult to generate timely insights, leading to slower decision-making and operational inefficiencies. During its expansion into the **Latin American** market, these limitations contributed to significant business challenges and financial losses.

Meanwhile, competitors leveraging modern **data analytics** and **Business Intelligence (BI)** solutions gained a competitive advantage by making faster, data-driven decisions.

To improve visibility, streamline reporting, and support strategic decision-making, AtliQ Hardware initiated a comprehensive **Business Insights 360** analytics project. The objective was to build an interactive Power BI dashboard that provides stakeholders with a centralized view of business performance across **Finance, Sales, Marketing, Supply Chain, and Executive** functions, enabling informed decisions and sustainable business growth.

---

# 🎯 Project Objective

The objective of this project is to empower business stakeholders with an interactive dashboard that enables data-driven decision-making by tracking key performance indicators (KPIs), analyzing profitability, monitoring sales performance, optimizing supply chain operations, and identifying business growth opportunities.

---

# 🛢️ Data Overview

AtliQ Hardware has provided **two SQL databases** and **three Excel files** for analysis.

## 📄 Excel Files

- **Operating Expenses**
- **Targets** *(available only for FY 2022)*
- **Market Share** *(limited to the Personal Computer division)*

## 🗄️ SQL Databases

### **gdb041**

**Fact Tables**
- `fact_forecast_monthly`
- `fact_sales_monthly`

**Dimension Tables**
- `dim_customer`
- `dim_market`
- `dim_product`

### **gdb056**

Contains the following tables:

- `freight_cost`
- `gross_price`
- `manufacturing_cost`
- `post_invoice_deductions`
- `pre_invoice_deductions`

## 📅 Fiscal Year

AtliQ's fiscal year runs from **September to August**, and the dataset covers actual sales from **September 1, 2017** to **December 31, 2021**.

> **Note:** Since this is a bootcamp project provided by **Codebasics**, the original datasets cannot be shared publicly.

---

# 🧹 Data Cleaning & Transformation

## 📌 Standardized & Trimmed Data

- Removed leading and trailing spaces from text fields.
- Standardized naming conventions to ensure consistency across the dataset.

## 📌 Data Structuring & Optimization

- Created a **`dim_date`** table to enable efficient time-based analysis.
- Merged **`fact_sales_monthly`** and **`fact_forecast_monthly`** into a single table, **`fact_actual_estimates`**, to simplify calculations and reporting.
- Added calculated fields to **`fact_actual_estimates`** by retrieving data from related tables (for example, deriving **pre-invoice deductions** using percentage values from the **`pre_invoice_deductions`** table).
- Disabled data load for intermediate tables that were only used to derive calculations in **`fact_actual_estimates`**, improving report performance and reducing the overall Power BI file size.

**Techniques Used:** Power Query, Merge Queries, Data Modeling, Calculated Columns, Performance Optimization.

---

# 📑 Report Inclusions

This repository includes a PDF version of the Power BI report hosted on the Power BI Service, along with its underlying data model. Below, you'll find a screenshot of the data model and a PDF of the report for a quick preview.

### 📄 [Dashboard](Dashboard/Business_Insights_360.pdf)

### 🧩 [Data Model](Model/Data_Model.png)

> **NOTE:** The **Information Panel** includes provisions for FAQs and a downloadable live Excel version for future company use. However, sharing the live Excel version requires the company's permission.

> **NOTE:** The **Support Panel** provides options to resolve issues, submit feedback, request new features, and review the contingency plan. Company support is required to integrate these features into the Power BI report.

---

## 🛠️ Tools Used

- **Data Cleaning & Transformation:** Power Query
- **Data Visualization:** Microsoft Power BI
- **Data Analysis:** DAX (Data Analysis Expressions)

---

# 💡 Insights

## 📈 Business Growth & Financial Performance

- Rapid expansion: **Net Sales** grew approximately **280% (FY 2019)**, **140% (FY 2020)**, **200% (FY 2021)**, and **350% (FY 2022)**.
- **Net Profit %** has remained negative since FY 2020 due to high operational and marketing expenses, which is typical for a company in its growth phase.

---

## 🌍 Revenue & Market Trends

- **APAC** remained the largest market (FY 2019–FY 2022), led by **India**, while **Latin America** was the smallest.
- **Amazon** was the top global customer across all years, while **Nova (Austria)** was the smallest customer since FY 2020.
- The **Notebook** segment achieved the highest revenue growth in every fiscal year but recorded the most negative **Net Profit %** in FY 2022, likely due to increased marketing spending.
- **Desktop** recorded the lowest growth in FY 2019 and FY 2020, while **Networking** became the weakest-performing segment in FY 2022.
- **USB Flash Drives** underperformed in FY 2021 and FY 2022, indicating potential product or market challenges.

---

## 💰 Sales & Customer Insights

- A flat post-discounting model across all products and customers within each market is significantly reducing **Gross Margin %**. A performance-based discounting strategy by product and customer is recommended to improve profitability.
- Products such as **AQ 5000 Series Electron 9 5900X**, **AQ MB Elite**, and **AQ Wi Power Dx1** recorded zero sales in FY 2022, likely due to changing demand or product obsolescence.

---

## 🚚 Forecast Accuracy & Supply Chain Efficiency

- **Forecast Accuracy (FCA%)** dropped from approximately **86% (FY 2019)** to **73% (FY 2020)** due to COVID-19 disruptions but recovered to approximately **80% (FY 2021)** and **81% (FY 2022)**.
- Excess inventory was a major challenge during FY 2019–FY 2020, whereas stock shortages became the primary issue in FY 2021–FY 2022.
- The work-from-home trend during FY 2020 caused stock shortages for processors, keyboards, and WiFi extenders.

---

## 🏆 Competitive Position & Market Share

- **AtliQ's PC market share** increased from approximately **1% (FY 2021)** to **6% (FY 2022)**, although **Dale** remained the market leader.
- **India** emerged as the fastest-growing market, contributing approximately **13% market share** in FY 2022.
- Among all subzones, **North America** generated the highest revenue in FY 2022, while AtliQ's market penetration remained around **5%**.

---

## 🎯 Operational & Strategic Insights

- Sales consistently peaked between **September and December**, driven by festive seasons and year-end promotions.
- **Retailers** contributed approximately **72%** of total revenue in FY 2022.
- The **UK** incurred the highest marketing expenses, making it a key area for strategic review, followed by **Germany**, which showed relatively low revenue despite high marketing spending.

---

# 📝 Recommendations

## 💰 Improve Profitability

- Gradually reduce operational and marketing expenses after capturing significant market share to improve **Net Profit %**.
- Reevaluate the pricing and cost structure of the **Notebook** segment to improve profitability.
- Shift from a flat post-discounting model to a **performance-based discounting strategy** for each product and customer within every market.

---

## 🌍 Expand Market Presence

- Expand distribution networks and targeted marketing efforts in high-growth regions such as **APAC**, with a particular focus on **India**.
- Develop targeted strategies to increase market share in **North America**.
- Focus on product differentiation to strengthen competitiveness in the **PC** segment and challenge dominant competitors such as **Dale**.

---

## 📦 Optimize Supply Chain

- Improve demand forecasting by leveraging real-time data to minimize stock imbalances and enhance supply chain efficiency.
- Align inventory planning and promotional activities with the **September–December** sales peak to maximize seasonal demand.

---

## 📈 Product & Marketing Strategy

- Investigate the underperformance of **USB Flash Drives** and consider repositioning, discontinuing, or introducing improved product models.
- Optimize marketing expenditure in the **UK** and **Germany** to improve return on investment (ROI).

---
# 📎 Links

### 🌐 LinkedIn Post
[View LinkedIn Post](PASTE_YOUR_LINKEDIN_POST_LINK_HERE)

### 📊 Live Dashboard
[Open Power BI Dashboard](PASTE_YOUR_POWER_BI_SERVICE_LINK_HERE)

---
# 🧠 Skills Gained

- Gained a deeper understanding of business metrics and their impact on a company's performance.
- Designed insightful, user-centric Power BI dashboards.
- Developed functional knowledge of **Finance, Sales, Marketing, and Supply Chain**, and their influence on overall business outcomes.

---

