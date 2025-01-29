# 📊 HR Employee Attendance Dashboard

## 📌 Project Overview
This project leverages **Power BI** to analyze employee attendance trends, providing valuable insights for HR teams to optimize workforce planning, manage absenteeism, and enhance employee engagement.

## 🔍 Why I Did This Project
Tracking and understanding employee attendance is crucial for making data-driven HR decisions. This project demonstrates how data analytics can:
- Identify **work-from-home trends** 📅
- Track **employee presence patterns** 🏢
- Detect **sick leave patterns** for proactive management 🤒
- Optimize **capacity planning** to reduce office space costs 💼

## 🔑 Key Insights
- **Work-from-Home Analysis**: Insights on preferred WFH days, especially Fridays and Mondays.
- **Attendance Trends**: Data-driven planning for team activities based on peak presence days.
- **Sick Leave Trends**: Seasonal illness patterns detected, allowing for preemptive health measures.
- **Office Space Optimization**: Analysis for reducing rental costs through efficient space utilization.

## 📊 Sample Dashboard Preview
![Dashboard Screenshot](https://github.com/SanthoshBotcha/HR-Employee-Analytics-Dashboard/blob/main/HR%20Analytics%20Dashboard.PNG)

## 🛠 Tech Stack & Tools Used
- **Power BI** - Dashboard creation and data visualization
- **Power Query** - Data cleaning and transformation
- **DAX (Data Analysis Expressions)** - Calculating attendance metrics
- **Excel** - Raw data source
- **Power Automate (Future Enhancement)** - Automation of report refresh and alerts

## 🔄 Procedure Followed

1. **Data Collection & Cleaning**
   - Collected employee attendance records from April to June.
   - Unpivoted data for proper Power BI analysis.
   - Removed inconsistencies and formatted date columns.

2. **Data Transformation (Power Query)**
   - Cleaned and transformed data using **Power Query**.
   - Structured data into tabular format for analysis.
   - Merged monthly records into a unified dataset.

3. **Creating DAX Measures**
   - Calculated key metrics:
     ```DAX
     Total Working Days = 
         COUNTROWS(FILTER(FinalData, FinalData[Attendance] <> "WO" && FinalData[Attendance] <> "HO"))

     Work from Home % = 
         DIVIDE(SUM(FinalData[WorkFromHomeCount]), SUM(FinalData[TotalWorkingDays]), 0)

     Sick Leave % =
         DIVIDE(SUM(FinalData[SickLeaveCount]), SUM(FinalData[TotalWorkingDays]), 0)
     ```

4. **Building the Power BI Dashboard**
   - Developed KPIs for presence percentage, work-from-home trends, and sick leave analysis.
   - Implemented interactive filters for exploring data by month, employee, and department.
   - Visualized long-term trends using line and bar charts.

5. **Automating Report Updates (Planned Enhancements)**
   - Integration with **SharePoint** for automatic data refresh.
   - Setting up **email alerts** if attendance drops below a certain threshold.

## 🏆 Final Summary
The **HR Employee Attendance Dashboard** empowers HR teams to:
- Improve **employee engagement** 📌
- Reduce **office space costs** 🏢
- Plan **effective HR policies** 🤝
- Ensure **health & safety** 🏥

