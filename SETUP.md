# 🚀 Setup Guide

This guide will help you set up and use the Retail Store Profit Analysis dashboard.

---

## 📋 Prerequisites

### System Requirements
- **Operating System:** Windows 7/8/10/11, macOS 10.12+, or Linux with Excel compatibility
- **Software:** Microsoft Excel 2016 or later (Excel 2019/365 recommended)
- **RAM:** Minimum 4GB (8GB recommended for large datasets)
- **Storage:** At least 50MB free space

### Optional Tools
- **Git:** For cloning the repository
- **Python 3.8+:** If you want to perform additional analysis
- **Power BI Desktop:** For creating Power BI versions (future enhancement)

---

## 📥 Installation

### Method 1: Download ZIP (Easiest)

1. Go to the GitHub repository: [Retail_Store_Profit_Analysis](https://github.com/divyathakur15/Retail_Store_Profit_Analysis)
2. Click the green **Code** button
3. Select **Download ZIP**
4. Extract the ZIP file to your desired location
5. Navigate to the extracted folder

### Method 2: Clone with Git (Recommended)

```bash
# Clone the repository
git clone https://github.com/divyathakur15/Retail_Store_Profit_Analysis.git

# Navigate into the project directory
cd Retail_Store_Profit_Analysis
```

---

## 🔧 Setup Steps

### Step 1: Open the Excel Workbook

1. Navigate to the `workbook/` folder
2. Double-click on `retail-store-analysis.xlsx`
3. **Important:** If you see a "Protected View" warning, click **Enable Editing**

### Step 2: Enable Macros (if applicable)

If the workbook contains macros:
1. Click **Enable Content** in the yellow security warning bar
2. If you don't see this option, go to File → Options → Trust Center → Trust Center Settings
3. Select "Enable all macros" (use cautiously)

### Step 3: Verify Data Connections

1. Go to the **Data** tab
2. Click **Queries & Connections**
3. Ensure all queries are loading properly
4. If you see errors, right-click and select **Refresh**

---

## 📊 Using the Dashboard

### Initial Exploration

1. **Main Dashboard Sheet**
   - This is typically the first visible sheet
   - Contains all visualizations and KPIs

2. **Data Sheet**
   - View the raw data used for analysis
   - Located in a separate tab

3. **Pivot Tables**
   - May be hidden or in separate sheets
   - Right-click on tabs to see hidden sheets

### Interactive Features

#### Using Slicers
1. Click on any item in the slicer (e.g., "Cosmetics")
2. All charts update automatically
3. To select multiple items, hold **Ctrl** while clicking
4. Click the filter icon to clear selections

#### Exploring Charts
1. Hover over any chart element to see details
2. Click on a segment to highlight related data
3. Right-click on charts for more options

#### Filtering Data
1. Click the dropdown arrows in pivot table headers
2. Select/deselect items to filter
3. Use search box for quick filtering

---

## 🔄 Refreshing Data

### If You Update the CSV File

1. Open Excel workbook
2. Go to **Data** tab
3. Click **Refresh All**
4. Wait for all queries and pivot tables to update

### If You Want to Add New Data

1. Open `data/retail-store-sales-data.csv`
2. Add new rows following the same format
3. Save the CSV file
4. In Excel, click **Refresh All**

---

## 🛠️ Troubleshooting

### Problem: Charts Not Displaying

**Solution:**
- Ensure you're using Excel 2016 or later
- Check if the sheet is in "Page Layout" view instead of "Normal" view
- Go to View → Normal

### Problem: Slicers Not Working

**Solution:**
- Right-click on the slicer → Report Connections
- Ensure it's connected to the correct pivot tables
- Click **Refresh** on the slicer

### Problem: #REF! or #VALUE! Errors

**Solution:**
- Check if the data range has changed
- Update pivot table data source:
  - Right-click pivot table → PivotTable Options → Change Data Source
  - Select the correct range

### Problem: File Opens Slowly

**Solution:**
- Close other Excel files
- Disable automatic calculation:
  - Formulas → Calculation Options → Manual
  - Remember to press F9 to calculate when needed
- Remove unused pivot caches:
  - File → Options → Advanced → PivotTable Options

### Problem: Compatibility Issues

**Solution:**
- Save as Excel Binary Workbook (.xlsb) for better performance
- Or use Excel 97-2003 format (.xls) for older versions
- Note: Some features may be lost in older formats

---

## 📱 Advanced Setup

### Setting Up Python Analysis (Optional)

If you want to perform additional analysis using Python:

```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install required packages
pip install pandas numpy matplotlib seaborn openpyxl

# Run analysis script (if available)
python analysis.py
```

### Creating a Power BI Dashboard (Future)

1. Open Power BI Desktop
2. Get Data → Text/CSV
3. Select `retail-store-sales-data.csv`
4. Transform and model data as needed
5. Create visualizations

---

## 🎓 Learning Resources

### Excel Skills Needed
- Pivot Tables and Pivot Charts
- Slicers and Timelines
- Basic formulas (SUM, AVERAGE, IF)
- Chart creation and formatting
- Data validation

### Recommended Tutorials
- [Microsoft Excel Official Training](https://support.microsoft.com/excel)
- [Pivot Table Tutorial](https://support.microsoft.com/en-us/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576)
- [Dashboard Design Best Practices](https://www.youtube.com/results?search_query=excel+dashboard+tutorial)

---

## 📞 Support

### Getting Help

- **Issues:** Open an issue on [GitHub Issues](https://github.com/divyathakur15/Retail_Store_Profit_Analysis/issues)
- **Discussions:** Use [GitHub Discussions](https://github.com/divyathakur15/Retail_Store_Profit_Analysis/discussions)
- **Email:** Contact the maintainer directly

### Before Asking for Help

1. Check this setup guide thoroughly
2. Review the troubleshooting section
3. Search existing issues on GitHub
4. Provide detailed information about your problem:
   - Excel version
   - Operating system
   - Error messages (screenshots help!)
   - Steps to reproduce

---

## ✅ Verification Checklist

After setup, verify everything is working:

- [ ] Excel workbook opens without errors
- [ ] All sheets are visible and accessible
- [ ] Charts display correctly
- [ ] Slicers are functional
- [ ] KPI cards show correct numbers
- [ ] Pivot tables can be refreshed
- [ ] Data source is correctly linked
- [ ] No #REF! or #VALUE! errors
- [ ] Dashboard is interactive

---

## 🎉 You're Ready!

If all steps completed successfully, you're ready to explore the dashboard!

Start by:
1. Reviewing the KPI cards
2. Trying out different slicer selections
3. Hovering over charts to see details
4. Exploring the raw data sheet

Happy analyzing! 📊

---

*Last Updated: March 2026*
