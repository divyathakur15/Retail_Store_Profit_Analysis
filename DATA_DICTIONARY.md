# 📖 Data Dictionary

## Overview
This document provides detailed information about each field in the retail store sales dataset.

---

## Dataset Information
- **File Name:** `retail-store-sales-data.csv`
- **Total Records:** 1,000 transactions
- **Date Range:** 2010 - 2017
- **File Size:** ~200KB
- **Format:** CSV (Comma-Separated Values)

---

## Field Descriptions

### 🌍 Geographic Fields

#### Region
- **Data Type:** Text/String
- **Description:** The geographic region where the sale occurred
- **Values:** 
  - North America
  - Europe
  - Asia
  - Sub-Saharan Africa
  - Middle East and North Africa
  - Central America and the Caribbean
  - Australia and Oceania
- **Null Values:** No
- **Example:** "Middle East and North Africa"

#### Country
- **Data Type:** Text/String
- **Description:** The specific country where the order was placed
- **Values:** Multiple countries across all regions
- **Null Values:** No
- **Example:** "Libya", "Canada", "Japan"

---

### 🛍️ Product Fields

#### Item Type
- **Data Type:** Text/String (Categorical)
- **Description:** The category of product sold
- **Values:**
  - Cosmetics
  - Vegetables
  - Baby Food
  - Cereal
  - Fruits
  - Clothes
  - Household
  - Office Supplies
  - Snacks
  - Beverages
  - Meat
  - Personal Care
- **Null Values:** No
- **Use Case:** Product performance analysis, inventory planning

---

### 👤 Sales Fields

#### Rep Name
- **Data Type:** Text/String
- **Description:** Name of the sales representative who handled the order
- **Format:** First Name + Last Name
- **Null Values:** No
- **Example:** "Lauren Marshall", "Evan Vaughan"
- **Use Case:** Sales rep performance tracking

#### Sales Channel
- **Data Type:** Text/String (Binary Categorical)
- **Description:** The channel through which the sale was made
- **Values:**
  - Online
  - Offline
- **Null Values:** No
- **Use Case:** Channel performance comparison, omnichannel strategy

---

### 📦 Order Fields

#### Order Priority
- **Data Type:** Text/String (Categorical)
- **Description:** Priority level assigned to the order
- **Values:**
  - **H** - High Priority
  - **M** - Medium Priority
  - **L** - Low Priority
  - **C** - Critical Priority
- **Null Values:** No
- **Use Case:** Logistics optimization, customer service prioritization

#### Order Date
- **Data Type:** Date
- **Format:** DD-MMM-YY (e.g., 18-Oct-14)
- **Range:** 2010 to 2017
- **Null Values:** No
- **Use Case:** Trend analysis, seasonality studies

#### Order ID
- **Data Type:** Integer/Number
- **Description:** Unique identifier for each transaction
- **Format:** 9-digit number
- **Null Values:** No
- **Uniqueness:** 100% unique (Primary Key)
- **Example:** 686800706

#### Ship Date
- **Data Type:** Date
- **Format:** DD-MMM-YY (e.g., 31-Oct-14)
- **Range:** 2010 to 2017
- **Null Values:** No
- **Use Case:** Shipping time analysis, logistics performance
- **Relationship:** Always >= Order Date

---

### 💰 Sales Metrics

#### Units Sold
- **Data Type:** Integer/Number
- **Description:** Quantity of products sold in the transaction
- **Range:** Varies by product type
- **Null Values:** No
- **Unit:** Count
- **Example:** 8446 units
- **Use Case:** Volume analysis, demand forecasting

#### Unit Price
- **Data Type:** Decimal/Currency
- **Description:** Selling price per unit of product
- **Currency:** USD ($)
- **Decimal Places:** 2
- **Range:** Varies by product category
  - Low: ~$9.33 (Fruits)
  - High: ~$668.27 (Household)
- **Null Values:** No
- **Example:** $437.20

#### Unit Cost
- **Data Type:** Decimal/Currency
- **Description:** Cost per unit (production/procurement cost)
- **Currency:** USD ($)
- **Decimal Places:** 2
- **Null Values:** No
- **Relationship:** Always < Unit Price
- **Example:** $263.33

---

### 📊 Calculated Financial Metrics

#### Total Revenue
- **Data Type:** Decimal/Currency
- **Description:** Total income from the sale
- **Formula:** `Units Sold × Unit Price`
- **Currency:** USD ($)
- **Decimal Places:** 2
- **Null Values:** No
- **Example:** $3,692,591.20
- **Use Case:** Revenue tracking, sales performance

#### Total Cost
- **Data Type:** Decimal/Currency
- **Description:** Total cost of goods sold
- **Formula:** `Units Sold × Unit Cost`
- **Currency:** USD ($)
- **Decimal Places:** 2
- **Null Values:** No
- **Example:** $2,224,085.18
- **Use Case:** Cost management, margin analysis

#### Total Profit
- **Data Type:** Decimal/Currency
- **Description:** Net profit from the transaction
- **Formula:** `Total Revenue - Total Cost`
- **Currency:** USD ($)
- **Decimal Places:** 2
- **Null Values:** No
- **Can Be Negative:** Technically possible, but not in this dataset
- **Example:** $1,468,506.02
- **Use Case:** Profitability analysis, business performance

---

### 📅 Derived Fields

#### Year
- **Data Type:** Integer
- **Description:** Year extracted from Order Date
- **Range:** 2010 - 2017
- **Null Values:** No
- **Use Case:** Yearly trend analysis, time series

#### Column1 & Column2
- **Data Type:** Decimal/Currency
- **Description:** These appear to be duplicate columns
- **Note:** Column1 = Total Profit, Column2 = Total Revenue
- **Recommendation:** These can be ignored as they duplicate existing data

---

## Data Quality Notes

### ✅ Strengths
- No missing values in critical fields
- Consistent date formatting
- Proper data types maintained
- Unique Order IDs for each transaction

### ⚠️ Observations
- Some column names have spaces (not ideal for programming)
- Column1 and Column2 are duplicates
- Country names may need standardization for some analyses
- Rep Name field includes full names (may want to split for analysis)

### 🔧 Recommended Transformations
1. Remove duplicate columns (Column1, Column2)
2. Calculate profit margin percentage: `(Total Profit / Total Revenue) × 100`
3. Calculate shipping duration: `Ship Date - Order Date`
4. Extract month and quarter from dates for seasonal analysis
5. Create price tiers based on Unit Price ranges

---

## Sample Record

```
Region: Middle East and North Africa
Country: Libya
Item Type: Cosmetics
Rep Name: Lauren Marshall
Sales Channel: Offline
Order Priority: M
Order Date: 18-Oct-14
Order ID: 686800706
Ship Date: 31-Oct-14
Units Sold: 8,446
Unit Price: $437.20
Unit Cost: $263.33
Total Revenue: $3,692,591.20
Total Cost: $2,224,085.18
Total Profit: $1,468,506.02
Year: 2014
```

---

## Usage Guidelines

### For Analysis
- Use `Order ID` as the primary key for joining with other datasets
- Group by `Region`, `Country`, or `Item Type` for comparative analysis
- Filter by `Year` for temporal analysis
- Segment by `Sales Channel` for channel comparison

### For Visualization
- **Geographic:** Use Region and Country fields
- **Product:** Use Item Type for categorization
- **Time:** Use Order Date or Year for trends
- **Performance:** Use Total Profit, Total Revenue for metrics

### For Business Intelligence
- **KPIs:** Calculate from Total Revenue, Total Cost, Total Profit
- **Trends:** Use Year and Order Date
- **Segmentation:** Use Region, Country, Item Type, Sales Channel
- **Operations:** Use Order Priority and shipping date difference

---

## Contact
For questions about the data structure or field definitions, please open an issue on GitHub.

---

*Last Updated: March 2026*
