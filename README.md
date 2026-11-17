# 📊 Sales Performance Dashboard (Power BI)

##  Project Overview
This project features an interactive Sales Dashboard built in Power BI. The purpose of this dashboard is to present an overview of sales metrics and trends, enabling stakeholders to analyze year-over-year (YoY) sales performance and understand key sales trends.

*Note: Since a Power BI account is required to view interactive `.pbix` files, this repository contains the dataset, dashboard screenshots, data model, and the DAX code used to build the report.*

##  Dashboard Preview
[images/dashboard_preview.PNG](https://github.com/hajeromerbashir/sales-performance-powerbi/blob/main/images/dashboard_preview.PNG)

##  Key Requirements Met
The dashboard was designed to address the following business requirements:

*   **KPI Overview:** Displays a summary of Total Sales, Total Profit, and Total Quantity for both the Current Year (CY) and Previous Year (PY).
*   **Sales Trends:** Presents monthly KPIs for CY and PY. Uses conditional formatting to highlight the highest and lowest sales months.
*   **Product Subcategory Comparison:** Compares sales performance by product subcategory across CY and PY, including a side-by-side comparison of Sales and Profit.
*   **Weekly Trends:** Displays weekly Sales and Profit data for the current year, highlighting weeks that perform above and below the average.

##  Data Model
The report utilizes a **Star Schema** design for optimal performance and accurate filtering.
[images/data_model.PNG](https://github.com/hajeromerbashir/sales-performance-powerbi/blob/main/images/data_model.PNG)

*   **Fact Table:** `Orders` (contains transactional data like Sales, Profit, Quantity)
*   **Dimension Tables:** `Customers`, `Location` (Postal Code), `Products`
*   **Supporting Tables:** `Parameter` (What-if parameters for dynamic year selection) and `Measure` tables for organized DAX.

##  (DAX)
The project utilizes advanced DAX calculations to achieve dynamic time intelligence and user interactivity. The code has been categorized into specific markdown files for easy review:
**[Calculated Columns]([DAX/01_Calculated_Columns.md](https://github.com/hajeromerbashir/sales-performance-powerbi/blob/main/DAX/%2301%20Calculated%20Columns%20(Orders%20Table)) - Custom columns for time-based grouping.

*  [[Time Intelligence][(DAX/02_Time_Intelligence.md](https://github.com/hajeromerbashir/sales-performance-powerbi/blob/main/DAX/%2302%20%20Time%20Intelligence%20%26%20Parameter%20Measures))]** - Dynamic CY and PY metrics using What-If parameters
  
*   [YoY Growth]([DAX/03_YoY_Growth.md][(https://github.com/hajeromerbashir/sales-performance-powerbi/blob/main/DAX/%2303%20%20Year-Over-Year%20(YoY)%20Growth%20Measures))](https://github.com/hajeromerbashir/sales-performance-powerbi/blob/main/DAX/%2303%20%20Year-Over-Year%20(YoY)%20Growth%20Measures)** - Year-over-Year percentage differences..
*   [Top N Analysis]([DAX/05_Top_N_Analysis.md][(https://github.com/hajeromerbashir/sales-performance-powerbi/blob/main/DAX/%2305%20Top_N_Analysis))] ** - Dynamic filtering for Top 5 Subcategories.
* [conditional formatting]([DAX/#04 Conditional_Formatting.md][(https://github.com/hajeromerbashir/sales-performance-powerbi/blob/main/DAX/%234%20Conditional_Formatting)])
👉 **[View the full DAX documentation here][DAX](https://github.com/hajeromerbashir/sales-performance-powerbi/tree/main/DAX)**

## 🛠️ Tools & Technologies
*   **Data:** Provided in the `dataset` folder (CSV format).
*   **Power Query:** Data transformation and cleaning.
*   **Power BI Desktop:** Data modeling, DAX, and visualization.


## 🚀 How to View
1. Review the **Dashboard Preview** image above.
2. Explore the **DAX folder** to see the logic behind the calculations.
3. The underlying datasets are available in the **dataset folder** if you wish to recreate the model.
