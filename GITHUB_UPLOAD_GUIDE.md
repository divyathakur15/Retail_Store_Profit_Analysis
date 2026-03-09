# GitHub Upload Guide

Follow these steps to upload your project to GitHub.

## Prerequisites
- Git installed on your computer
- GitHub account created
- Repository created on GitHub

---

## Step-by-Step Guide

### 1. Open PowerShell/Terminal
Navigate to your project root folder:
```powershell
cd "c:\Users\HP\Desktop\EXCEL\Dummy Store Analysis Project"
```

### 2. Move Documentation to Root
The documentation should be at the project root:
```powershell
# Copy all documentation files to root
Copy-Item -Path "Retail_Store_Profit_Analysis\*" -Destination "." -Force

# You can then delete the empty folder if desired
# Remove-Item "Retail_Store_Profit_Analysis" -Recurse -Force
```

### 3. Initialize Git Repository
```powershell
git init
```

### 4. Add All Files
```powershell
git add .
```

### 5. Create Initial Commit
```powershell
git commit -m "Initial commit: Retail Store Profit Analysis Dashboard with comprehensive documentation"
```

### 6. Create Repository on GitHub
1. Go to https://github.com/new
2. Repository name: `Retail_Store_Profit_Analysis`
3. Description: `Interactive Excel dashboard analyzing global retail sales data with insights on revenue, profit, and market performance`
4. Choose "Public"
5. **DO NOT** initialize with README, .gitignore, or license (we already have these)
6. Click "Create repository"

### 7. Connect to GitHub
Replace `divyathakur15` with your GitHub username:
```powershell
git remote add origin https://github.com/divyathakur15/Retail_Store_Profit_Analysis.git
git branch -M main
git push -u origin main
```

### 8. Verify Upload
Visit your repository URL to ensure all files uploaded correctly.

---

## Troubleshooting

### Error: "remote origin already exists"
```powershell
git remote remove origin
git remote add origin https://github.com/divyathakur15/Retail_Store_Profit_Analysis.git
```

### Error: Authentication Failed
Use GitHub Personal Access Token:
1. Go to GitHub → Settings → Developer settings → Personal access tokens
2. Generate new token with "repo" permissions
3. Use token as password when pushing

### Error: Large File Warning
If Excel file is too large:
```powershell
# Check file size
Get-Item "workbook\retail-store-analysis.xlsx" | Select-Object Name, Length

# If over 100MB, use Git LFS
git lfs install
git lfs track "*.xlsx"
git add .gitattributes
git add workbook/retail-store-analysis.xlsx
git commit -m "Add Excel file with Git LFS"
git push
```

---

## After Upload

### Add Topics
1. Go to your repository on GitHub
2. Click the gear icon next to "About"
3. Add topics: `excel-dashboard`, `data-analysis`, `business-intelligence`, `retail-analytics`, `pivot-tables`

### Enable Features
- ✅ Issues (for bug reports)
- ✅ Discussions (for Q&A)
- ✅ Wiki (optional)

### Create Release (Optional)
1. Go to Releases → Create a new release
2. Tag version: `v1.0.0`
3. Release title: `Initial Release - Complete Dashboard`
4. Description: Copy from CHANGELOG.md
5. Attach Excel file if needed

---

## Repository Settings

### Description
```
Interactive Excel dashboard analyzing global retail sales data (2010-2017) with insights on revenue, profit, and market performance across multiple regions and product categories.
```

### Topics
```
excel-dashboard
data-analysis
business-intelligence
retail-analytics
pivot-tables
data-visualization
sales-analysis
profit-analysis
excel-project
dashboard-design
```

---

## Success! 🎉

Your project is now on GitHub and ready to be shared!

**Repository URL:**
`https://github.com/divyathakur15/Retail_Store_Profit_Analysis`

Share it on:
- LinkedIn
- Twitter
- Your portfolio
- Job applications

---

*Good luck with your project!*
