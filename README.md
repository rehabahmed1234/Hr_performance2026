# Hr_performance2026
HR analytics project that explores employee performance, job satisfaction, and attrition. It analyzes KPIs like productivity, work quality, and teamwork, links satisfaction to environment, pay, growth, and work-life balance, and identifies turnover drivers (low salary, limited advancement, poor management) to reduce attrition.
# HR Analytics (Power BI)

## Project Overview
This project uses **Power BI** to analyze Human Resources (HR) data in order to understand **employee performance**, **job satisfaction**, and **attrition (employee turnover)**. The goal is to provide data-driven insights that help organizations improve the work environment, increase satisfaction, and reduce employee turnover.

---

## Data Source
The dataset is an **Excel sheet** containing employee-level information related to hiring, leaving, performance, and satisfaction.

### Main Columns
- **EmployeeID**: Unique employee identifier (numeric).
- **FirstName**: Employee first name.
- **LastName**: Employee last name.
- **HireDate**: Date the employee was hired.
- **ExitDate**: Date the employee left the company (blank for active employees).
- **Age**: Employee age.
- **ReasonForLeaving**: Reason for leaving (if applicable).
- **SatisfactionLevel**: Employee satisfaction rating/level.
- **Performance**: Employee performance rating/score.
- **Bonus**: Employee bonus amount (if available in the data).

> Note: Column names may vary slightly depending on the Excel file. They can be adjusted to match the exact dataset fields.

---

## Data Preparation (Power Query / Modeling Steps)
The following steps were performed in Power BI:

1. **Data Cleaning**
   - Checked and fixed data types (dates, numbers, text).
   - Handled missing values (especially `ExitDate` and `ReasonForLeaving`).

2. **Remove Duplicates**
   - Removed duplicated records to ensure each employee/record is represented correctly.

3. **Created New Columns (Derived Fields)**
   - **Experience**: Calculated employee experience/tenure based on `HireDate` (and `ExitDate` for leavers).
   - **Age Groups**: Split `Age` into ranges (e.g., 18–25, 26–35, 36–45, etc.).
   - **Bonus Bands**: Split `Bonus` into categories (Low / Medium / High or custom thresholds).

4. **Created a Separate Date Table**
   - Built a dedicated calendar/date table to support time intelligence and trend analysis.

5. **Relationships**
   - Linked the Date table to the main employee table using the relevant date fields (e.g., `HireDate` and/or `ExitDate`, depending on the analysis).

---

## Dashboard (Report Pages)
The Power BI report includes **4 pages**:

1. **Overview**
   - High-level summary of the HR dataset and key KPIs (e.g., headcount, average satisfaction, average performance, attrition overview).

2. **Employee Satisfaction**
   - Analysis of satisfaction levels and how they vary by segments such as age group, experience, and other available fields.

3. **Attrition Rate**
   - Attrition rate distribution and breakdown by key segments (Age Groups, Experience, Bonus Bands, etc.).

4. **Total Employees**
   - A dedicated page showing **total employees (headcount)** with breakdowns and filters (e.g., by age groups, experience, bonus bands, or other available dimensions).

---

## Expected Insights
This dashboard can help answer questions such as:
- What are the most common reasons employees leave?
- How does satisfaction relate to attrition?
- Which age groups or experience levels show higher turnover?
- Does bonus level correlate with satisfaction and retention?
- How do hiring and leaving trends change over time?

---

## Files
- **HR Project.pbix**: Main Power BI report file (model + visuals).
- **.xlsx**: Excel data source file.

---

## How to Use
1. Download the `.pbix` file.
2. Open it using **Power BI Desktop**.
3. If the Excel source path is not found:
   - Transform Data → Data source settings → Change Source
4. Click **Refresh** to load the latest data.

---

## Notes (Optional Improvements)
If you share:
- the exact column names as written in your Excel sheet,
- the exact definitions for Age Groups and Bonus Bands,
- and whether Experience is calculated in years only or years + months,  
I can tailor this README to match your dataset 100%.
