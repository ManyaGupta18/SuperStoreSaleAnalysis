# SuperStore Sale Analysis

## 🧾 Project Overview

Welcome to the **SuperStore Sale Analysis** project!  
This repository showcases an end-to-end workflow—from loading and transforming data using SQL, to creating dashboards in Excel and Tableau that deliver meaningful business insights.

### Key Highlights
- Loaded raw transactional and product data into **SQL** (SQL Server Management Studio).
- Built new tables through **JOIN** operations to create a consolidated dataset for analysis.
- Exported cleaned/aggregated data to **Excel**, and designed intuitive dashboards with pivot tables and charts.
- Developed an interactive **Tableau dashboard** featuring filters, KPIs, and visualizations to support decision-making.

---

## 📁 Repository Structure

```
SuperStoreSaleAnalysis/
├── sql/
│   ├── load_data.sql              # Scripts to load raw data
│   └── join_tables.sql            # SQL joins to create the analytical table
├── excel/
│   ├── SuperStore_Report.xlsx     # Excel file with pivot charts and dashboards
│   └── screenshots/               # Images of Excel dashboards
├── tableau/
│   ├── SuperStoreDashboard.twbx   # Tableau packaged workbook
│   └── visuals/                   # Dashboard snapshots (PNG/JPG)
└── README.md                      # This file
```

---

## 🚀 Tech Stack & Tools

| Tool        | Purpose                             |
|-------------|-------------------------------------|
| **SQL**     | Data ingestion, cleaning, JOINs     |
| **Excel**   | Pivot tables, charts, reporting     |
| **Tableau** | Interactive dashboard & visualization |

---

## 🔍 SQL Workflow

- Imported raw data into staging tables.
- Performed multi-table JOINs (e.g., `Orders` + `Customers` + `Products`) to construct one view/table optimized for analytics.
- Included aggregation (SUM, COUNT, AVG) and filtering logic for performance.
- Sample snippet:

  ```sql
  SELECT
    o.OrderID, o.OrderDate, c.CustomerName, p.ProductCategory,
    SUM(o.Sales) AS TotalSales,
    COUNT(*) AS OrderCount
  FROM Orders o
    JOIN Customers c ON o.CustomerID = c.CustomerID
    JOIN Products p  ON o.ProductID = p.ProductID
  GROUP BY o.OrderID, o.OrderDate, c.CustomerName, p.ProductCategory;
  ```

---

## 📊 Excel Dashboard Highlights

- Created PivotTables summarizing Total Sales by Category, Region, and Customer Segment.
- Designed charts (bar, line, donut) to visualize trends over time.
- Used conditional formatting to spotlight top/bottom performers.
- Embedded slicers for dynamic interactivity.

---

## 📈 Tableau Dashboard Features

- Interactive filters for regions, product categories, and order dates.
- KPI cards showing metrics like Total Sales, Profit, and Order Count.
- Trend lines, heat maps, and bar charts to explore performance dimensions.
- Dashboard designed for clarity and user experience, ideal for executive reporting.

---

## 🖼️ Screenshots

Below are some sample visuals from the dashboards:

### 📌 Excel Dashboard

<img width="920" height="565" alt="image" src="https://github.com/user-attachments/assets/964a387a-5442-4239-aeb4-f672d00079b8" />
<img width="847" height="545" alt="image" src="https://github.com/user-attachments/assets/cf750838-11fa-4e26-9bca-eae20c207f72" />



### 📌 Tableau Dashboard

<img width="929" height="631" alt="image" src="https://github.com/user-attachments/assets/2f14ca07-4138-492a-af95-cd6a49b3b57b" />
<img width="851" height="641" alt="image" src="https://github.com/user-attachments/assets/8cc73067-a3a3-4452-9cec-a32feff4e142" />
<img width="897" height="311" alt="image" src="https://github.com/user-attachments/assets/aec328b2-52f2-4ceb-96ae-04770ae1d469" />




---

## 🛠 How to Explore

1. **SQL folder**: Run the scripts to load and transform sample data tables.
2. **Excel folder**: Open `SuperStore_Report.xlsx` to explore pivot charts.
3. **Tableau folder**: Open the `.twbx` file to interact with visual dashboards.

---

## 🤝 Contact & Contributions

Have feedback or suggestions? I’d love to hear from you!

- **GitHub**: ManyaGupta18  

---

## 📝 Final Notes

This project demonstrates a full-stack data approach—from SQL for data engineering to Excel for classical reporting, and Tableau for interactive visual storytelling. It is ideal for portfolio inclusion or as a showcase of your technical proficiency.

Feel free to adapt and expand it. Let me know if you'd like help tailoring it further or adding badges, screenshots, or demo links!
