# 📊 Customer Behavior & Lifecycle Analysis — Adventure Works

![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![Domain](https://img.shields.io/badge/Domain-Retail%20Analytics-blue?style=for-the-badge)
![Dataset](https://img.shields.io/badge/Dataset-Adventure%20Works-orange?style=for-the-badge)

---

## 📌 Project Overview

This project is a **Customer Behavior & Lifecycle Analysis** built on the **Adventure Works** retail dataset using **Tableau Desktop**. The primary goal was to analyse how customers behave over time — how frequently they purchase, how recently they were active, and how valuable they are to the business.

Adventure Works is a Microsoft sample retail database widely used for analytics and business intelligence projects.

---

## 🎯 Objective

> To analyse customer purchasing patterns across segmentation, lifecycle, engagement, churn risk, and profitability — and deliver actionable insights through 2 interactive Tableau dashboards.

---

## 🖼️ Dashboard Preview

### Dashboard 1 — Customer Behavior & Lifecycle Analysis
![Dashboard 1](1st_pic.jpeg)

### Dashboard 2 — Sales & Profitability Analysis
![Dashboard 2](2nd_pic.jpeg)

---

## 📐 Dashboard Structure

| Dashboard | KPIs | Charts | Total Sheets |
|-----------|------|--------|--------------|
| Dashboard 1 — Customer Behavior & Lifecycle | 4 | 5 | 9 |
| Dashboard 2 — Sales & Profitability | 5 | 6 | 11 |
| **Total** | **9** | **11** | **20** |

---

## 📊 Dashboard 1 — Customer Behavior & Lifecycle Analysis

### 🔢 KPIs (4)

| KPI | Value | Description |
|-----|-------|-------------|
| Total Customers | 18,484 | Total unique customers in the dataset |
| Active Customers | 11,818 | Customers who made a recent purchase |
| Repeat Customers | 6,865 | Customers with more than one order |
| One-Time Customers | 11,619 | Customers who purchased only once |

### 📈 Charts (5)

| Chart | Type | Description |
|-------|------|-------------|
| Inactive Days by Engagement | Bar Chart | Distribution of customers by number of inactive days grouped by engagement level |
| Customer Share | Pie Chart | Split between New Customers (18,484) and Returning Customers (5,244) |
| Year-Wise Customer | Line Chart | Customer count trend from 2010 to 2014 — peak at 17,429 in 2013 |
| Lifecycle Composition | Treemap | Breakdown into New & Active (8,838), Loyal but Inactive (4,285), Loyal & Active (2,980), New but Inactive (2,781) |
| Engagement vs Recency Heatmap | Heatmap | Cross-tab of Customer Engagement Segment vs Recency (Latest vs Previous) |

---

## 📊 Dashboard 2 — Sales & Profitability Analysis

### 🔢 KPIs (5)

| KPI | Value | Description |
|-----|-------|-------------|
| Revenue Per Customer | 26,120 | Average revenue generated per customer |
| Profit Per Customer | 653.6 | Average profit earned per customer |
| High-Value Customer | 16.12% | Percentage of customers in the top 20% sales tier |
| Repeat Purchase Ratio | 37.14% | Percentage of customers who made repeat purchases |
| Active Customer Ratio | 63.94% | Percentage of currently active customers |

### 📈 Charts (6)

| Chart | Type | Description |
|-------|------|-------------|
| Monthly Sales & Profit Trend | Bar + Line Combo | Month-wise sales (bars) and profit trend (line) across the year |
| Country Wise Profit | Map | Geographic profit distribution — US ($3.90M), Australia ($3.69M), Canada ($1.09M), UK, France, Germany |
| Top 20% vs Bottom 80% Customers | Donut Chart | Top 20% customers contribute 66.40% of total sales ($29.36M) vs Bottom 80% at 33.60% |
| Profit Margin By Region | Horizontal Bar | Region-wise profit margins — Central highest at 45.02%, UK lowest at 41.00% |
| Top 10 Customers By Sales | Bar Chart | Ranked list of top 10 customers — Ms Nichole Nara leads at $13.30K |
| Sales Contribution by Product Model | Bubble Chart | Product model sales — Mountain-200 ($7.93M) and Road-150 ($5.55M) are top contributors |

---

## 🔧 Tableau Techniques Used

| Technique | Details |
|-----------|---------|
| **FIXED LOD Expressions** | 37 references — customer-level sales, order counts, first purchase date |
| **DATEDIFF** | Customer tenure in days, inactive days, recency calculation |
| **COUNTD** | Distinct customer count and distinct order count |
| **IF / ELSEIF** | Lifecycle stage, churn flag, engagement segment logic |
| **CASE WHEN** | Dynamic KPI parameter switching |
| **Parameters** | Dynamic metric switcher — Customers / Orders / Sales / Avg Orders |
| **Percentile LOD** | Top 20% customer threshold using PERCENTILE() |
| **YEAR / DATE functions** | First purchase year and order year extraction |

---

## 🧮 Key Calculated Fields (45 Total)

| Category | Fields |
|----------|--------|
| Customer Segmentation | Customer_type, High-Value Customer, Customer_Engagement_Segment, Customer Group, Customer Sales Share |
| Lifecycle & Churn | Customer_Lifecycle, Customer_status, Customer_Recency, Inactive_days, Customer_Tenure_Years, Repeat_purchase, Active Customer Ratio |
| Profitability | Row Profit, Row Profit Margin, Total Cost, Profit Margin, Profit Per Customer, Average Revenue Per Customer, Revenue Dependency Score, Top 20% Sales, Geographical Profit |
| Dynamic KPI | Dynamic Customer Metric, Orders per Customer, Total Orders, Total Sales, First Purchase Year |

---

## 🗄️ Data Sources (7 Tables)

| Table | Type | Description |
|-------|------|-------------|
| `Main_Sales` (FactInternetSales) | Fact | All sales transactions |
| `Dimcustomer` | Dimension | Customer demographics and details |
| `DimDate` | Dimension | Calendar and fiscal date attributes |
| `DimProduct` | Dimension | Product details and standard cost |
| `DimProdCategory` | Dimension | Product category information |
| `DimProdSubCategory` | Dimension | Product sub-category information |
| `DimSalesTerritory` | Dimension | Sales region and country |

---

## 💡 Key Insights

- 🏆 Top 20% of customers contribute **66.40%** of total revenue ($29.36M)
- 🔄 **37.14%** repeat purchase ratio indicates a strong loyal customer base
- ⚠️ **2,781** customers are New but Inactive — early churn risk group to re-engage
- 📅 Customer count peaked at **17,429 in 2013** then dropped sharply to 834 in 2014
- 🌍 **United States** is the most profitable market at $3.90M followed by Australia at $3.69M
- 🚲 **Mountain-200** is the top selling product model contributing $7.93M in sales
- 📊 **Central region** has the highest profit margin at 45.02%

---

## 🚀 How to Open This Project

1. Download **Tableau Public** (free) from [tableau.com/products/public](https://www.tableau.com/products/public)
2. Clone or download this repository
3. Open `Customer_behavior_Shubham.twbx` in Tableau Desktop or Tableau Public
4. All data is embedded inside the `.twbx` file — no separate database connection needed

---

## 🗂️ Project Files

```
Customer-Behavior-Adventure-Works/
│
├── Customer_behavior_Shubham.twbx   ← Tableau Packaged Workbook
├── 1st_pic_.png                     ← Dashboard 1 Screenshot
├── 2nd_pic.png                      ← Dashboard 2 Screenshot
└── README.md                        ← Project documentation
```

---

## 👤 Author

**Shubham Bagadade**
- 🎓 Data Analyst | 2022 Batch
- 💼 Skills: Tableau · Power BI · SQL · Python · Excel
- 🔗 LinkedIn: *[Add your LinkedIn URL]*
- 📧 Email: *[Add your Email]*
- 🐙 GitHub: *[Add your GitHub profile link]*

---

## 🏷️ Tags

`Tableau` `Data Analytics` `Customer Segmentation` `Adventure Works` `Customer Behavior` `Churn Detection` `LOD Expressions` `KPI Dashboard` `Business Intelligence` `Data Visualization` `Customer Lifecycle` `Profitability Analysis` `Treemap` `Heatmap`

---

⭐ If you found this project useful, please consider giving it a star!
