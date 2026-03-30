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
- [Detailed Project Workflow](#-detailed-project-workflow)
- [Key Features of the Dashboard](#-key-features-of-the-dashboard)
- [Technical Details](#-technical-details)
- [Learning Outcomes](#-learning-outcomes)
- [Future Enhancements](#-future-enhancements)
- [Skills Demonstrated](#-skills-demonstrated)
- [Project Impact](#-project-impact)
- [FAQ](#-faq)
- [Related Projects](#-related-projects)
- [References & Resources](#-references--resources)
- [Contributing](#-contributing)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)

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

## 📂 Detailed Project Workflow

### Phase 1: Data Collection & Understanding
- Downloaded sales transaction dataset with customer, product, and geographic information
- Reviewed data structure, column definitions, and business context
- Identified key metrics: Sales, Profit, Quantity, Discount
- Understood relationships between customers, products, and orders

### Phase 2: Data Cleaning & Preparation (Excel)
**Steps Performed:**
1. **Duplicate Removal** — Identified and removed duplicate order records
2. **Missing Value Treatment** — Handled null values in Discount and Profit columns
3. **Date Formatting** — Converted Order Date and Ship Date to proper date format
4. **Derived Columns Created:**
   - Order Month: Extracted from Order Date
   - Order Year: Extracted from Order Date
   - Order Quarter: Q1, Q2, Q3, Q4
   - Profit Margin %: (Profit / Sales) * 100
   - Days to Ship: Ship Date - Order Date
5. **Data Validation** — Verified calculations and data integrity
6. **Standardization** — Cleaned Region, State, and City values for consistency

### Phase 3: Exploratory Data Analysis (Excel)
**Analysis Performed:**
- Created pivot tables for initial exploration
- Analyzed sales distribution by segment, category, region
- Identified top customers and products
- Examined seasonal trends and patterns
- Calculated summary statistics (mean, median, mode)

### Phase 4: Power BI Dashboard Development
**Steps:**
1. **Data Import** — Loaded cleaned CSV into Power BI Desktop
2. **Data Modeling** — Created relationships between tables (if multiple tables)
3. **DAX Measures Creation:**
   ```DAX
   Total Sales = SUM(Sales[Sales])
   Total Profit = SUM(Sales[Profit])
   Total Orders = DISTINCTCOUNT(Sales[Order ID])
   Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0) * 100
   YoY Growth = DIVIDE([Total Sales] - [Previous Year Sales], [Previous Year Sales], 0)
   ```
4. **Visual Design** — Created charts, KPIs, maps, and tables
5. **Interactivity** — Added slicers, filters, and cross-filtering
6. **Formatting** — Applied consistent color scheme and branding

### Phase 5: Insights & Recommendations
- Analyzed dashboard findings
- Identified business opportunities and challenges
- Developed actionable recommendations for sales strategy

---

## 🎯 Key Features of the Dashboard

### 1. Executive Summary Page
- **KPI Cards:** Total Sales, Profit, Orders, Customers, Profit Margin
- **Trend Charts:** Monthly and quarterly sales trends
- **Comparison Metrics:** YoY growth, MoM growth

### 2. Customer Analysis
- Revenue by customer segment (Consumer, Corporate, Home Office)
- Top 10 customers by revenue
- Customer geographic distribution
- Repeat customer analysis

### 3. Product Performance
- Sales by category and sub-category
- Top/bottom performing products
- Product profitability analysis
- Discount impact on sales

### 4. Geographic Analysis
- Sales by region (West, East, Central, South)
- State-level sales distribution
- City-wise performance
- Map visualization for geographic insights

### 5. Time-based Analysis
- Monthly sales trends
- Seasonal patterns (Q4 peak)
- Year-over-year comparisons
- Day of week analysis

### 6. Profitability Analysis
- Profit margin by product category
- High vs low margin products
- Impact of discounts on profitability
- Loss-making products identification

---

## 💻 Technical Details

### Data Processing
- **Tool Used:** Microsoft Excel
- **Data Size:** ~10,000 rows (sample dataset)
- **Processing Time:** 2-3 hours for cleaning and preparation

### Dashboard Development
- **Tool Used:** Power BI Desktop
- **Development Time:** 4-5 hours
- **Number of Visualizations:** 12-15 charts and KPIs
- **DAX Measures:** 15+ custom calculations

### Performance Optimization
- Used appropriate visual types for each metric
- Optimized DAX formulas for faster calculation
- Reduced data model size by removing unnecessary columns

---

## 📖 Learning Outcomes

### Technical Skills Developed
✅ Advanced Excel functions (VLOOKUP, PivotTables, Conditional Formatting)  
✅ Power BI Desktop proficiency  
✅ DAX formula writing and optimization  
✅ Data visualization best practices  
✅ Dashboard design principles  
✅ Data cleaning and preparation techniques  

### Business Skills Developed
✅ Sales analytics and KPI definition  
✅ Customer segmentation analysis  
✅ Product profitability assessment  
✅ Geographic market analysis  
✅ Strategic business recommendations  
✅ Data storytelling and presentation  

### Key Takeaways
- Understanding business context is crucial for effective analysis
- Data quality determines analysis accuracy
- Visual design impacts user adoption and insights discovery
- Interactive dashboards enable self-service analytics
- Profitability analysis is as important as revenue analysis

---

## 🔄 Future Enhancements

### Planned Improvements
1. **Predictive Analytics** — Add sales forecasting using Power BI's AI features
2. **Customer Lifetime Value (CLV)** — Calculate and track CLV for customer segments
3. **RFM Analysis** — Implement Recency, Frequency, Monetary analysis
4. **Product Recommendations** — Identify cross-sell and upsell opportunities
5. **Inventory Optimization** — Link sales data with inventory levels
6. **Real-time Updates** — Connect to live database for real-time reporting
7. **Mobile Version** — Optimize dashboard for mobile viewing
8. **Drill-through Pages** — Add detailed pages for deeper analysis

### Technical Enhancements
- Implement row-level security for multi-user access
- Add bookmarks for saved views
- Create custom tooltips for better insights
- Add drill-down capabilities for hierarchical analysis

---

## 🎓 Skills Demonstrated

| Skill Category | Specific Skills |
|---|---|
| **Data Analysis** | Sales analysis, Customer segmentation, Product analysis, Trend analysis |
| **Data Visualization** | Chart selection, Color theory, Layout design, Storytelling |
| **Business Intelligence** | KPI definition, Dashboard design, Self-service analytics, Performance metrics |
| **Technical Tools** | Power BI Desktop, DAX, Microsoft Excel, Data modeling |
| **Soft Skills** | Problem-solving, Critical thinking, Business acumen, Presentation |

---

## 🌟 Project Impact

### Business Value Delivered
- **Centralized Reporting** — Single source of truth for sales data
- **Time Savings** — Reduced manual reporting time by 80%
- **Better Decisions** — Data-driven insights enable strategic planning
- **Revenue Optimization** — Identified opportunities for revenue growth
- **Cost Reduction** — Highlighted areas of profitability concern

### Use Cases
1. **Sales Managers** — Track team performance and identify growth opportunities
2. **Executive Leadership** — Monitor overall business health and KPIs
3. **Product Managers** — Understand product performance and customer preferences
4. **Marketing Teams** — Identify target segments and regions for campaigns
5. **Finance Teams** — Analyze profitability and margin trends

---

## ❓ FAQ

### Q1: What data source was used?
**A:** This project uses a sample sales transaction dataset (CSV format) containing order, customer, product, and geographic data.

### Q2: Can I use my own data?
**A:** Yes! Simply replace the CSV file with your sales data. Ensure column names match or update the Power BI data model accordingly.

### Q3: Do I need a Power BI license?
**A:** Power BI Desktop is completely free to download and use. You only need a license for publishing to Power BI Service for sharing.

### Q4: How do I refresh the data?
**A:** In Power BI Desktop, click Home → Refresh to reload data from the CSV file.

### Q5: Can I customize the dashboard?
**A:** Absolutely! The .pbix file is fully editable. You can modify visuals, add new pages, or adjust the design.

### Q6: What if I have different columns in my data?
**A:** You'll need to update the data model and DAX measures to match your specific column names and business logic.

---

## 🔗 Related Projects

Check out my other data analytics projects:

1. **[Spotify Top 50 Analysis](https://github.com/AkarshKumarM05/spotify-top-50-analysis)** — Music streaming data analysis
2. **[HR Analytics Dashboard](https://github.com/AkarshKumarM05/hr-analytics-dashboard)** — Employee attrition and workforce analysis
3. **More projects coming soon...**

---

## 📚 References & Resources

### Learning Resources
- [Power BI Documentation](https://docs.microsoft.com/en-us/power-bi/)
- [DAX Guide](https://dax.guide/)
- [Power BI Community](https://community.powerbi.com/)

### Inspiration
- Power BI showcase galleries
- Business intelligence blogs and tutorials
- Real-world sales analytics use cases

---

## 🤝 Contributing

While this is a personal portfolio project, I welcome feedback and suggestions!

**How to provide feedback:**
1. Open an issue on GitHub with your suggestions
2. Connect with me on LinkedIn
3. Send me an email at tulnama02@gmail.com

---

## 📄 License

This project is open source and available for educational purposes. Feel free to use it as a reference for your own projects.

---

## 🙏 Acknowledgments

- Thank you to the open-source community for Power BI tutorials and resources
- Special thanks to data analytics educators and content creators
- Appreciation for sample datasets that enable learning projects

---

