# 📊 Retail Store Profit Analysis Dashboard

![Dashboard Preview](../dashboard/retail-store-dashboard.png)

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Dataset Description](#-dataset-description)
- [Dashboard Features](#-dashboard-features)
- [Key Insights & Findings](#-key-insights--findings)
- [Project Structure](#-project-structure)
- [Tools & Technologies](#-tools--technologies)
- [How to Use](#-how-to-use)
- [Visualizations](#-visualizations)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 Project Overview

This project presents a comprehensive analysis of global retail sales data spanning from **2010 to 2017**, covering transactions across **multiple countries, regions, and product categories**. The primary objective is to uncover actionable business insights through data visualization and analysis.

**Key Objectives:**
- Analyze sales performance across different geographic regions and countries
- Identify the most profitable product categories and sales channels
- Understand customer order priorities and their impact on business
- Track yearly trends in revenue, costs, and profitability
- Support data-driven decision-making through interactive dashboards

The project features an **interactive Excel dashboard** with dynamic slicers, pivot tables, and charts that enable stakeholders to explore the data and make informed business decisions.

---

## 📂 Dataset Description

The dataset contains **1,000 retail transaction records** from a global retail company operating across multiple continents. Each record represents a unique sales order with comprehensive details about the transaction.

### 📊 Dataset Statistics
- **Total Records:** 1,000 transactions
- **Time Period:** 2010 - 2017
- **Geographic Coverage:** 6 regions, multiple countries
- **Product Categories:** 12 item types
- **Sales Channels:** Online and Offline

### 📝 Column Descriptions

| Column Name | Description | Data Type |
|-------------|-------------|-----------|
| **Region** | Geographic region (e.g., North America, Europe, Asia) | Text |
| **Country** | Specific country where the order was placed | Text |
| **Item Type** | Product category (Cosmetics, Vegetables, Baby Food, etc.) | Text |
| **Rep Name** | Sales representative handling the order | Text |
| **Sales Channel** | Distribution method (Online/Offline) | Text |
| **Order Priority** | Priority level (H-High, M-Medium, L-Low, C-Critical) | Text |
| **Order Date** | Date when the order was placed | Date |
| **Order ID** | Unique identifier for each transaction | Number |
| **Ship Date** | Date when the order was shipped | Date |
| **Units Sold** | Quantity of products sold in the order | Number |
| **Unit Price** | Selling price per unit | Currency |
| **Unit Cost** | Production/procurement cost per unit | Currency |
| **Total Revenue** | Total income from the sale (Units Sold × Unit Price) | Currency |
| **Total Cost** | Total cost of goods sold (Units Sold × Unit Cost) | Currency |
| **Total Profit** | Profit earned (Total Revenue - Total Cost) | Currency |
| **Year** | Extracted year from Order Date | Number |

### 🌍 Geographic Regions Covered
1. **North America** (Canada, USA, Greenland)
2. **Europe** (Multiple EU countries)
3. **Asia** (Japan, Mongolia, Laos, Maldives, etc.)
4. **Sub-Saharan Africa** (Multiple countries)
5. **Middle East and North Africa** (Libya, Turkey, Israel, etc.)
6. **Central America and the Caribbean** (Jamaica, Honduras, etc.)
7. **Australia and Oceania** (Fiji, Micronesia)

### 🛍️ Product Categories
- Cosmetics
- Vegetables
- Baby Food
- Cereal
- Fruits
- Clothes
- Household items
- Office Supplies
- Snacks
- Beverages
- Meat
- Personal Care

---

## 📊 Dashboard Features

The Excel dashboard provides a comprehensive view of business performance through multiple interactive components:

### 🎯 Key Performance Indicators (KPIs)
- **Total Orders:** Complete count of transactions processed
- **Total Revenue:** Aggregate income generated from all sales
- **Total Cost:** Cumulative cost of goods sold
- **Total Profit:** Net profit across all transactions

### 📈 Interactive Visualizations

1. **Top 10 Countries by Profit** (Horizontal Bar Chart)
   - Identifies the most profitable markets
   - Helps prioritize resource allocation

2. **Profit by Region** (Pie/Donut Chart)
   - Shows profit distribution across geographic regions
   - Enables regional performance comparison

3. **Profit by Item Type** (Bar Chart)
   - Displays profitability of different product categories
   - Guides inventory and product strategy decisions

4. **Profit by Sales Channel** (Pie Chart)
   - Compares Online vs Offline sales performance
   - Informs channel investment strategies

5. **Yearly Profit Trend** (Line Chart)
   - Tracks profit evolution over time (2010-2017)
   - Identifies growth patterns and seasonal trends

6. **Order Priority Distribution** (Visualization)
   - Analyzes the distribution of order priorities
   - Helps optimize logistics and fulfillment

### 🎛️ Interactive Filters
- **Item Type Slicer:** Filter all visualizations by specific product categories
- Dynamic updates across all charts for real-time analysis

---

## 💡 Key Insights & Findings

Based on the comprehensive analysis of 1,000 transactions spanning 2010-2017:

### 🏆 Geographic Performance
- **Sub-Saharan Africa** shows significant presence in the dataset
- **Top performing countries** include Libya, Canada, Japan, and various European nations
- Multiple emerging markets demonstrate strong growth potential

### 📦 Product Performance
- **High-value items** include Household goods (Unit Price: $668.27) and Office Supplies (Unit Price: $651.21)
- **Fast-moving products** include Fruits and Beverages (lower unit prices but potentially higher volume)
- **Profit margins** vary significantly across product categories

### 🌐 Sales Channel Insights
- Both **Online and Offline channels** are actively utilized
- Channel preference varies by region and product type
- Multi-channel strategy is essential for market coverage

### 📅 Temporal Trends
- Business operations span **7+ years** (2010-2017)
- Consistent year-over-year activity indicates business stability
- Seasonal patterns can be identified through date analysis

### ⚡ Order Priority Patterns
- Mix of **Critical (C), High (H), Medium (M), and Low (L)** priority orders
- Priority levels impact shipping schedules and customer satisfaction
- Helps optimize operational efficiency

---

## 📁 Project Structure

```
Retail_Store_Profit_Analysis/
│
├── 📄 README.md                          # Project documentation (you are here)
│
├── 📊 data/
│   └── retail-store-sales-data.csv       # Raw dataset (1,000 transactions)
│
├── 📈 dashboard/
│   └── retail-store-dashboard.png        # Complete dashboard screenshot
│
├── 📉 visualizations/
│   ├── kpi-cards-and-slicers.png         # KPI metrics and filter controls
│   ├── profit-by-item-type.png           # Product category performance
│   ├── profit-by-region.png              # Regional profit distribution
│   ├── profit-by-sales-channel.png       # Online vs Offline comparison
│   ├── top-10-profit-by-country.png      # Top performing countries
│   ├── yearly-profit-trend.png           # Time series analysis
│   └── order-priority-distribution.png   # Priority level breakdown
│
└── 📂 workbook/
    └── retail-store-analysis.xlsx        # Excel file with data, pivots, and dashboard
```

---

## 🛠️ Tools & Technologies

This project was built using the following tools and techniques:

### Microsoft Excel
- **Version:** Excel 2016 or later recommended
- **Features Used:**
  - Pivot Tables for data aggregation and summarization
  - Pivot Charts for dynamic visualizations
  - Slicers for interactive filtering
  - Conditional Formatting for data highlighting
  - Data Validation for data integrity
  - Formulas and Functions (SUM, AVERAGE, IF, etc.)

### Data Processing Techniques
- ✅ Data Cleaning and Preparation
- ✅ Data Transformation and Feature Engineering
- ✅ Statistical Analysis
- ✅ Time Series Analysis
- ✅ Comparative Analysis

### Visualization Techniques
- 📊 Bar Charts (Horizontal & Vertical)
- 🥧 Pie Charts & Donut Charts
- 📈 Line Charts for Trends
- 📋 KPI Cards
- 🎛️ Interactive Slicers

---

## 🖼️ Visualizations

### Complete Dashboard
![Complete Dashboard](../dashboard/retail-store-dashboard.png)

### KPI Cards and Slicers
![KPI Cards](../visualizations/kpi-cards-and-slicers.png)
*Key metrics at a glance with interactive filters*

### Top 10 Countries by Profit
![Profit by Country](../visualizations/top-10-profit-by-country.png)
*Identifying the most profitable markets globally*

### Profit Distribution by Region
![Profit by Region](../visualizations/profit-by-region.png)
*Regional performance comparison*

### Product Category Performance
![Profit by Item Type](../visualizations/profit-by-item-type.png)
*Which products generate the most profit?*

### Sales Channel Analysis
![Sales Channel](../visualizations/profit-by-sales-channel.png)
*Online vs Offline performance*

### Yearly Profit Trend
![Yearly Trend](../visualizations/yearly-profit-trend.png)
*Profit evolution from 2010 to 2017*

### Order Priority Distribution
![Order Priority](../visualizations/order-priority-distribution.png)
*Understanding order urgency patterns*

---

## 📈 Future Enhancements

Potential improvements for this project:

- [ ] Add predictive analytics for future sales forecasting
- [ ] Implement customer segmentation analysis
- [ ] Create automated reports using VBA macros
- [ ] Integrate with Power BI for advanced visualizations
- [ ] Add shipping time analysis (Order Date vs Ship Date)
- [ ] Perform ABC analysis for inventory management
- [ ] Include profit margin % calculations by category
- [ ] Add geographic mapping visualizations
- [ ] Implement what-if scenario analysis
- [ ] Create mobile-friendly dashboard version

---

## 🤝 Contributing

Contributions are welcome! If you'd like to improve this project:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/AmazingFeature`)
3. **Commit your changes** (`git commit -m 'Add some AmazingFeature'`)
4. **Push to the branch** (`git push origin feature/AmazingFeature`)
5. **Open a Pull Request**

### Ways to Contribute
- Report bugs or issues
- Suggest new features or visualizations
- Improve documentation
- Add new analysis perspectives
- Optimize Excel formulas and calculations

---

## 📧 Contact

**Divya Thakur**
- GitHub: [@divyathakur15](https://github.com/divyathakur15)
- LinkedIn: [Connect with me](https://www.linkedin.com/in/divyathakur15)
- Email:  [Emial](divya.thakur1506@gmail.com)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Dataset source: [Specify source if applicable]
- Inspiration from various retail analytics projects
- Microsoft Excel community for tips and best practices
- Open source community for continuous learning

---

## ⭐ Star This Repository

If you found this project helpful, please consider giving it a star! It helps others discover the project and motivates further development.

---

**📊 Happy Analyzing! 📊**

*Last Updated: March 2026*