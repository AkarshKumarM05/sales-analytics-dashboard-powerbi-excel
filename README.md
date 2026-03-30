# 📊 Sales Analytics Dashboard — Power BI & Excel

![POWERBI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![EXCEL](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![SALES](https://img.shields.io/badge/Sales-FF6B6B?style=for-the-badge)
![ANALYTICS](https://img.shields.io/badge/Analytics-4A90E2?style=for-the-badge)

> An end-to-end sales analytics project analyzing revenue performance, customer behavior, and product trends using Power BI, Excel, and DAX measures with interactive visualizations.

---

## 📑 Table of Contents

- [Overview](#overview)
- [Business Problem](#business-problem)
- [Dataset](#dataset)
- [Data Model](#data-model)
- [DAX Measures](#dax-measures)
- [Key Visualizations](#key-visualizations)
- [Insights & Recommendations](#insights--recommendations)
- [Technical Specifications](#technical-specifications)
- [How to Use](#how-to-use)
- [Future Enhancements](#future-enhancements)
- [Connect](#connect)

---

## 🎯 Overview

This **Sales Analytics Dashboard** provides comprehensive insights into sales performance across multiple dimensions including time periods, product categories, customer segments, and geographical regions. Built with Power BI and Excel, it enables stakeholders to make data-driven decisions through interactive visualizations and KPI tracking.

### Project Highlights:
- **📈 Revenue Analysis**: Track total sales, profit margins, and growth trends
- **🛍️ Product Performance**: Identify top-selling products and categories
- **👥 Customer Insights**: Analyze customer behavior and segmentation
- **🌍 Geographic Analysis**: Compare sales performance across regions
- **📊 Time Intelligence**: Year-over-year and month-over-month comparisons

---

## 💼 Business Problem

### Challenge
The sales team needed a centralized analytics solution to:
1. Monitor real-time sales performance against targets
2. Identify underperforming products and regions
3. Understand customer purchasing patterns
4. Optimize inventory and resource allocation
5. Forecast future sales trends

### Objectives
- Create an interactive dashboard for sales monitoring
- Implement DAX measures for advanced analytics
- Enable drill-down capabilities for detailed analysis
- Provide actionable insights for strategic planning
- Track KPIs including revenue, profit, units sold, and customer metrics

---

## 📊 Dataset

### Data Source
The dataset includes transactional sales data with the following characteristics:

**Key Features:**
- **Order Details**: Order ID, Order Date, Ship Date, Ship Mode
- **Customer Information**: Customer ID, Customer Name, Segment, Region
- **Product Details**: Product ID, Product Name, Category, Sub-Category
- **Financial Metrics**: Sales Amount, Quantity, Discount, Profit
- **Geographic Data**: Country, State, City, Postal Code

**Dataset Size:**
- Time Period: Multiple years of historical data
- Records: Thousands of transactions
- Dimensions: Customer, Product, Geography, Time

### Data Quality
- Data cleaning performed in Excel
- Handled missing values and duplicates
- Standardized date formats
- Created calculated columns for analysis

---

## 🔗 Data Model

Implemented a **star schema** with:

### Fact Table:
- **Sales_Fact**: Contains all transactional measures

### Dimension Tables:
- **Date_Dim**: Calendar table with fiscal periods
- **Product_Dim**: Product hierarchy (Category → Sub-Category → Product)
- **Customer_Dim**: Customer segmentation details
- **Geography_Dim**: Location hierarchy (Region → State → City)

### Relationships:
- One-to-many relationships from dimensions to fact table
- Bi-directional cross-filtering where necessary

---

## 🧮 DAX Measures

### Core Measures

```dax
// Total Sales
Total Sales = SUM(Sales_Fact[Sales])

// Total Profit
Total Profit = SUM(Sales_Fact[Profit])

// Profit Margin
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0) * 100

// Total Quantity
Total Quantity = SUM(Sales_Fact[Quantity])

// Total Orders
Total Orders = DISTINCTCOUNT(Sales_Fact[Order ID])

// Average Order Value
Average Order Value = DIVIDE([Total Sales], [Total Orders], 0)
```

### Time Intelligence Measures

```dax
// Year-to-Date Sales
YTD Sales = TOTALYTD([Total Sales], Date_Dim[Date])

// Previous Year Sales
PY Sales = CALCULATE([Total Sales], SAMEPERIODLASTYEAR(Date_Dim[Date]))

// Sales Growth %
Sales Growth % = 
VAR CurrentSales = [Total Sales]
VAR PreviousSales = [PY Sales]
RETURN
    IF(
        NOT(ISBLANK(PreviousSales)),
        DIVIDE(CurrentSales - PreviousSales, PreviousSales, 0) * 100,
        BLANK()
    )

// Month-over-Month Growth
MoM Growth % = 
VAR CurrentMonth = [Total Sales]
VAR PreviousMonth = CALCULATE([Total Sales], DATEADD(Date_Dim[Date], -1, MONTH))
RETURN
    DIVIDE(CurrentMonth - PreviousMonth, PreviousMonth, 0) * 100
```

### Customer Metrics

```dax
// Total Customers
Total Customers = DISTINCTCOUNT(Sales_Fact[Customer ID])

// New Customers
New Customers = 
CALCULATE(
    [Total Customers],
    FILTER(
        ALL(Date_Dim),
        Date_Dim[Date] = 
            CALCULATE(
                MIN(Sales_Fact[Order Date]),
                ALLEXCEPT(Sales_Fact, Sales_Fact[Customer ID])
            )
    )
)

// Repeat Customers
Repeat Customers = [Total Customers] - [New Customers]

// Customer Lifetime Value
Customer LTV = 
AVERAGEX(
    VALUES(Sales_Fact[Customer ID]),
    [Total Sales]
)
```

### Product Performance

```dax
// Top Selling Product
Top Product = 
TOPN(
    1,
    VALUES(Product_Dim[Product Name]),
    [Total Sales],
    DESC
)

// Product Rank
Product Rank = 
RANKX(
    ALL(Product_Dim[Product Name]),
    [Total Sales],
    ,
    DESC,
    DENSE
)

// Category Contribution %
Category % = 
DIVIDE(
    [Total Sales],
    CALCULATE([Total Sales], ALL(Product_Dim[Category])),
    0
) * 100
```

---

## 📈 Key Visualizations

### 1. Executive Summary Page
- **KPI Cards**: Total Sales, Profit, Orders, Customers
- **Trend Lines**: Sales and profit trends over time
- **Gauge Charts**: Performance vs. targets
- **Slicers**: Date range, region, product category filters

### 2. Sales Performance Analysis
- **Area Chart**: Monthly sales trends with forecasting
- **Waterfall Chart**: Sales breakdown by components
- **Combo Chart**: Sales vs. profit comparison
- **Matrix**: Hierarchical sales data

### 3. Product Analysis
- **Bar Chart**: Top 10 products by revenue
- **Treemap**: Product category distribution
- **Scatter Plot**: Profit vs. quantity analysis
- **Table**: Detailed product performance metrics

### 4. Customer Analytics
- **Donut Chart**: Customer segment distribution
- **Column Chart**: Sales by customer segment
- **Funnel Chart**: Customer acquisition journey
- **Heat Map**: Customer activity patterns

### 5. Geographic Analysis
- **Map Visual**: Sales distribution by location
- **Filled Map**: Regional performance
- **Conditional Formatting**: State-wise comparisons

---

## 💡 Insights & Recommendations

### Key Findings

#### Sales Performance
- **Total Revenue**: Strong performance with consistent growth
- **Seasonal Trends**: Peak sales during Q4 (holiday season)
- **Growth Rate**: Positive year-over-year trend

#### Product Insights
- **Top Categories**: Technology and Office Supplies lead revenue
- **High Margin Products**: Specific sub-categories show strong profitability
- **Underperformers**: Some products require pricing or marketing review

#### Customer Behavior
- **Customer Segments**: Corporate customers generate highest revenue
- **Repeat Rate**: Strong customer retention indicators
- **Average Order Value**: Varies significantly by segment

#### Geographic Trends
- **Top Regions**: West and East regions outperform
- **Growth Opportunities**: Central region shows potential
- **Urban vs. Rural**: Urban areas dominate sales

### Strategic Recommendations

1. **Optimize Inventory**
   - Increase stock for top-performing products
   - Phase out slow-moving inventory
   - Adjust for seasonal demand patterns

2. **Customer Engagement**
   - Implement loyalty programs for repeat customers
   - Target high-value customer segments
   - Personalized marketing campaigns

3. **Product Strategy**
   - Expand high-margin product lines
   - Bundle products for increased average order value
   - Review pricing strategy for underperformers

4. **Regional Focus**
   - Increase marketing in underperforming regions
   - Replicate successful strategies from top regions
   - Consider regional preferences in product mix

5. **Sales Operations**
   - Optimize shipping modes for cost efficiency
   - Reduce delivery times in competitive markets
   - Implement dynamic pricing strategies

---

## 🛠️ Technical Specifications

### Tools & Technologies
- **Power BI Desktop**: Version 2.0+
- **Microsoft Excel**: 2016 or later
- **DAX**: Data Analysis Expressions
- **Power Query**: For data transformation

### Features Implemented
- ✅ Interactive drill-down/drill-through
- ✅ Dynamic slicers and filters
- ✅ Time intelligence calculations
- ✅ Custom tooltips
- ✅ Bookmarks for navigation
- ✅ Mobile-optimized layout
- ✅ Row-level security (RLS) ready
- ✅ Automated data refresh

### Performance Optimization
- Efficient DAX formulas using variables
- Aggregated tables for faster queries
- Removed unnecessary columns
- Optimized relationships and cardinality

---

## 🚀 How to Use

### Prerequisites
1. Install Power BI Desktop (latest version)
2. Microsoft Excel 2016 or later

### Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/AkarshKumarM05/sales-analytics-dashboard-powerbi-excel.git
   cd sales-analytics-dashboard-powerbi-excel
   ```

2. **Open the Dashboard**
   - Navigate to the `/dashboard` folder
   - Open `Sales_Analytics_Dashboard.pbix` in Power BI Desktop

3. **Load Data**
   - Dataset is pre-loaded in the .pbix file
   - To refresh with new data, go to Home → Transform Data
   - Update the data source path if needed

4. **Explore Visualizations**
   - Use slicers to filter data
   - Click on visuals for cross-filtering
   - Hover for detailed tooltips
   - Use bookmarks for page navigation

5. **Publish (Optional)**
   - Sign in to Power BI Service
   - Click Publish → Select workspace
   - Configure scheduled refresh

---

## 🔮 Future Enhancements

### Planned Features
- [ ] Predictive analytics using machine learning
- [ ] Advanced forecasting models
- [ ] Customer churn prediction
- [ ] Real-time data integration
- [ ] Integration with CRM systems
- [ ] Automated email reports
- [ ] Mobile app integration
- [ ] Natural language Q&A
- [ ] R/Python custom visuals
- [ ] Sentiment analysis on customer feedback

### Potential Improvements
- Enhanced data security with RLS implementation
- Additional KPIs based on stakeholder feedback
- Integration with external data sources (weather, events)
- Advanced statistical analysis
- Competitive benchmarking

---

## 👨‍💻 Author & Contact

**Akarsh Kumar Pandey**  
B.Com (Hons) | Data Analytics Enthusiast

[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:tulnama02@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/akarshkpandey)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AkarshKumarM05)
---

> ⭐ If you found this project useful, please give it a star — it helps a lot!
