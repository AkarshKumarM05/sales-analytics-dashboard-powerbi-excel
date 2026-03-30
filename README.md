# 📊 Sales Analytics Dashboard — Power BI & Excel

![POWERBI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![EXCEL](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![SALES](https://img.shields.io/badge/Sales-FF6B6B?style=for-the-badge)
![ANALYTICS](https://img.shields.io/badge/Analytics-4A90E2?style=for-the-badge)

> An end-to-end sales analytics project analyzing revenue performance, customer behavior, and product trends using Power BI, Excel, and DAX measures with interactive visualizations.

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Business Problem](#-business-problem)
- [Dataset](#-dataset)
- [Tools & Technologies](#️-tools--technologies)
- [Project Structure](#️-project-structure)
- [Data Cleaning & Preparation](#-data-cleaning--preparation)
- [Exploratory Data Analysis (EDA)](#-exploratory-data-analysis-eda)
- [Research Questions & Key Insights](#-research-questions--key-insights)
- [Dashboard](#-dashboard)
- [How to Run This Project](#-how-to-run-this-project)
- [Final Recommendations](#-final-recommendations)
- [Dashboard Screenshots](#-dashboard-screenshots)
- [Author & Contact](#-author--contact)

---

## 📖 Overview

This project analyzes **Sales Analytics** data to understand revenue performance, customer purchasing patterns, product trends, and geographical sales distribution. The goal is to help sales managers and business leaders make data-driven decisions to maximize revenue, improve customer retention, and optimize product strategies.

The dashboard was built in **Power BI Desktop** with custom **DAX measures**, covering:

- Revenue analysis and profit margins
- Customer segmentation and behavior
- Product performance and category analysis
- Geographical sales distribution
- Time-based trends and seasonal patterns

---

## 💼 Business Problem

Sales teams struggle with understanding revenue drivers, customer preferences, and product performance. This project addresses the following business challenges:

- **No centralized sales tracking** — Sales teams lack a unified dashboard to monitor revenue, profit, and key metrics
- **Limited customer insights** — It's unclear which customer segments generate the most revenue and have the highest lifetime value
- **No product performance visibility** — The relationship between products, categories, and profitability is not analyzed
- **Geographic blindspots** — Certain regions may have untapped potential but go unnoticed
- **Difficulty tracking trends** — No visibility into seasonal patterns, growth trends, or forecasting
- **Decision-making gaps** — Sales cannot proactively identify opportunities or implement targeted strategies

---

## 📁 Dataset

- **Source:** Sales Transaction Data (Sample Dataset)
- **File:** `Sales_Data.csv`
- **Records:** Thousands of transactions
- **Dimensions:** Customer, Product, Geography, Time

### Key Columns:

| Column | Description |
|--------|-------------|
| `Order ID` | Unique order identifier |
| `Order Date` | Date of order placement |
| `Ship Date` | Date of shipment |
| `Ship Mode` | Shipping method used |
| `Customer ID` | Unique customer identifier |
| `Customer Name` | Name of the customer |
| `Segment` | Customer segment (Consumer/Corporate/Home Office) |
| `Region` | Geographic region |
| `Country` | Country name |
| `State` | State/Province |
| `City` | City name |
| `Product ID` | Unique product identifier |
| `Product Name` | Name of the product |
| `Category` | Product category |
| `Sub-Category` | Product sub-category |
| `Sales` | Sales amount |
| `Quantity` | Quantity sold |
| `Discount` | Discount applied |
| `Profit` | Profit earned |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|  
| **Power BI Desktop** | Dashboard building & interactive visualizations |
| **Microsoft Excel** | Data cleaning, preprocessing & exploration |
| **DAX** | Custom KPI calculations and measures |
| **GitHub** | Version control & project documentation |

---

## 🗂️ Project Structure

```
sales-analytics-dashboard-powerbi-excel/
│
├── 📁 assets/              ← Dashboard screenshots
├── 📁 dashboard/           ← Power BI .pbix file  
├── 📁 data/                ← Raw CSV dataset
└── README.md
```

---

## 🧹 Data Cleaning & Preparation

Before building the dashboard, the raw dataset was cleaned and structured in **Microsoft Excel**:

✅ Removed duplicate order records  
✅ Handled missing values in `Discount` and `Profit` columns  
✅ Created **Order Month** and **Order Year** columns for time-based analysis  
✅ Created **Profit Margin %** calculated column: `(Profit / Sales) * 100`  
✅ Standardized `Region` and `State` values for consistency  
✅ Converted `Order Date` and `Ship Date` to proper date formats  
✅ Created **Customer Segment** groups for analysis  
✅ Validated `Sales` against `Quantity` and `Discount` for data integrity

---

## 🔍 Exploratory Data Analysis (EDA)

### Sales Overview

- **Total Revenue:** Strong growth trajectory
- **Total Orders:** Thousands of transactions processed
- **Average Order Value (AOV):** Varies by customer segment
- **Total Customers:** Diverse customer base
- **Total Products:** Wide product catalog

### Revenue by Customer Segment

- **Consumer Segment:** Largest contributor to revenue
- **Corporate Segment:** High-value B2B customers
- **Home Office Segment:** Growing market

Customer segments show different purchasing patterns, with corporate customers having higher average order values.

### Revenue by Product Category

- **Technology:** Highest revenue category
- **Furniture:** Strong consistent sales
- **Office Supplies:** High volume, lower margins

Product mix indicates technology drives revenue while office supplies maintain volume.

### Revenue by Region

- **West Region:** Highest revenue contributor
- **East Region:** Second largest market
- **Central Region:** Moderate performance
- **South Region:** Growth opportunity

Geographic analysis reveals concentration in coastal regions with potential for expansion in other areas.

### Sales by Time Period

- **Seasonal Trends:** Peak sales in Q4 (November-December)
- **Monthly Patterns:** End-of-quarter spikes
- **Year-over-Year Growth:** Consistent upward trend

Time-based analysis shows strong seasonality with holiday shopping driving Q4 performance.

### Profit Analysis

- **High-Profit Products:** Technology items show best margins
- **Loss-Making Products:** Some discounted items reduce profitability
- **Profit by Region:** Varies significantly across geographies

Profitability analysis indicates need for pricing strategy optimization.

---

## 💡 Research Questions & Key Insights

### 1. What is the overall revenue trend?

**Finding:** Revenue shows **consistent growth** year-over-year with strong seasonal peaks in Q4. This indicates healthy business expansion with predictable patterns.

### 2. Which customer segment generates the most revenue?

**Finding:** **Consumer segment** generates the highest revenue, followed by Corporate and Home Office. Consumer customers represent the largest market opportunity.

### 3. Which product categories are most profitable?

**Finding:** **Technology products** show the highest profit margins, while Office Supplies have lower margins but higher volume. Focus should be on high-margin technology while maintaining office supplies volume.

### 4. Which regions show the strongest performance?

**Finding:** **West and East regions** outperform Central and South regions. Regional strategies should focus on maintaining leadership in top regions while growing underperforming markets.

### 5. How do discounts impact profitability?

**Finding:** Heavy discounting reduces profit margins significantly. Strategic discount management is crucial for maintaining profitability while driving volume.

### 6. What are the seasonal sales patterns?

**Finding:** **Q4 shows the highest sales** due to holiday shopping, with November-December peak months. Inventory and staffing should be optimized for seasonal demand.

### 7. Which products have the highest return rates?

**Finding:** Analysis of returns by product category helps identify quality issues and customer satisfaction gaps.

---

## 📊 Dashboard

The Power BI dashboard provides **interactive visualizations** across key sales metrics:

### Key Metrics (KPI Cards)

- Total Sales: **$XXX,XXX**
- Total Profit: **$XX,XXX**
- Profit Margin: **XX%**
- Total Orders: **X,XXX**
- Total Customers: **X,XXX**
- Average Order Value: **$XXX**

### Visualizations

| Visualization | Description |
|---------------|-------------|
| **Sales by Segment** | Donut chart showing revenue distribution across customer segments |
| **Sales by Category** | Bar chart displaying category-wise sales performance |
| **Sales by Region** | Map visualization showing geographical sales distribution |
| **Sales Trend** | Line chart showing monthly/quarterly sales trends |
| **Profit by Product** | Horizontal bar chart of product profitability |
| **Top 10 Customers** | Table showing highest-value customers |
| **Sales vs Profit** | Scatter plot analyzing sales-profit relationship |

---

## 🚀 How to Run This Project

### Prerequisites

- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
- Microsoft Excel or any CSV viewer
- Git (optional, for cloning)

### Steps

**1. Clone the repository:**

```bash
git clone https://github.com/AkarshKumarM05/sales-analytics-dashboard-powerbi-excel.git
```

**2. Navigate to the project folder:**

```bash
cd sales-analytics-dashboard-powerbi-excel
```

**3. Open the dataset:**

- Locate `data/Sales_Data.csv`
- Open in Excel to preview or verify data structure

**4. Open the Power BI Dashboard:**

- Open `dashboard/Sales_Analytics_Dashboard.pbix` in **Power BI Desktop**
- If prompted, update the data source path to point to `data/Sales_Data.csv` on your local machine

**5. Refresh the data:**

- Go to **Home → Refresh** in Power BI Desktop to load the latest data

**6. Explore the dashboard:**

- Use slicers to filter by region, segment, category, or time period
- Hover over visuals for detailed tooltips and insights

---

## ✅ Final Recommendations

Based on the sales analytics findings:

1. **Optimize Product Mix** — Focus on high-margin technology products while maintaining office supplies volume for consistent revenue.

2. **Implement Strategic Discounting** — Heavy discounts reduce profitability. Use data-driven discount strategies targeting specific products and customer segments.

3. **Expand in Underperforming Regions** — Central and South regions show growth potential. Increase marketing and sales efforts in these areas.

4. **Enhance Customer Segmentation** — Develop targeted strategies for Consumer, Corporate, and Home Office segments based on their unique behaviors.

5. **Leverage Seasonal Trends** — Optimize inventory and staffing for Q4 peak season. Consider promotional campaigns to boost sales in slower quarters.

6. **Focus on Customer Retention** — Identify and nurture high-value customers. Implement loyalty programs to increase customer lifetime value.

7. **Improve Profit Margins** — Review pricing strategy for low-margin products. Consider bundling or value-added services to improve profitability.

---

## 📸 Dashboard Screenshots

**Full Dashboard View**

[Dashboard View](./assets/sales_dashboard_screenshot.png)

---

## 👨‍💻 Author & Contact

**Akarsh Kumar Pandey**  
B.Com (Hons) | Data Analytics Enthusiast

[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:tulnama02@gmail.com) [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/akarshkpandey) [![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AkarshKumarM05)

---

> ⭐ If you found this project useful, please give it a star — it helps a lot!

---

**Built with 💙 by Akarsh Kumar Pandey** | *Transforming Data into Insights*
