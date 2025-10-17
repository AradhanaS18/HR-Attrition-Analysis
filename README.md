# 💼 HR Attrition Analysis Dashboard (Power BI)
This project presents an interactive HR Attrition Analysis Dashboard created using Microsoft Power BI.
It provides insights into employee attrition patterns, helping HR departments understand and address employee turnover effectively.

# 🧩 Project Overview
The dashboard analyzes employee data to identify trends and factors contributing to attrition such as:
Overtime
Department
Age group
Job role
Marital status
Gender

# 🛠 Tools & Technologies Used
Power BI – for data visualization and dashboard creation
Power Query (within Power BI) – for data cleaning and transformation
DAX (Data Analysis Expressions) – for calculated measures such as:
Attrition Count
Attrition Rate
Average Monthly Income
Age Group
Female Count
Male Count

# 🧮 Key DAX Measures Used
Total Employees = COUNT(EmployeeData[Attrition])

Attrition Count = 
CALCULATE(COUNT(EmployeeData[Attrition]), EmployeeData[Attrition] = "Yes")

Attrition Rate = 
DIVIDE([Attrition Count], [Total Employees], 0)

Average Monthly Income = 
AVERAGE(EmployeeData[MonthlyIncome])

Age Group = SWITCH(
    TRUE(),
    'HR Employee Attrition'[Age] >= 18 && 'HR Employee Attrition'[Age] <= 25, "18-25",
    'HR Employee Attrition'[Age] >= 26 && 'HR Employee Attrition'[Age] <= 35, "26-35",
    'HR Employee Attrition'[Age] >= 36 && 'HR Employee Attrition'[Age] <= 45, "36-45",
    'HR Employee Attrition'[Age] >= 46 && 'HR Employee Attrition'[Age] <= 55, "46-55",
    'HR Employee Attrition'[Age] > 55, "55+"
)

Female Count = COUNTROWS(FILTER('HR Employee Attrition', 'HR Employee Attrition'[Gender]="Female"))

Male Count = COUNTROWS(FILTER('HR Employee Attrition', 'HR Employee Attrition'[Gender]="Male"))

# 📊 Dashboard Highlights
Attrition by Age Group: Shows which age ranges are more likely to leave the company.
Attrition by Job Role: Highlights roles with higher turnover.
Attrition by Overtime: Demonstrates how overtime affects employee retention.
Average Monthly Income Analysis: Compares salaries of employees who stayed vs. left.

# 💡 Key Insights
The overall attrition rate is 16%.
Employees doing Overtime have a higher attrition rate (41%) than those who don’t (10%).
Single employees tend to leave more often than married ones.
Younger employees (especially ages 26–35) show higher turnover rates.
Sales and HR departments have more attrition compared to others.

# 👩‍💻 Author
Aradhana S
💼 Aspiring Data Analyst | Power BI Enthusiast
🔗 https://www.linkedin.com/in/aradhanasubash/
