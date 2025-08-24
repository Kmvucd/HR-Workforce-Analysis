# 👥 HR Workforce & Attrition Analysis Dashboard – Power BI
## 📖 Overview

This project is an HR Workforce Analysis Dashboard built with Power BI to explore employee demographics, attrition trends, and workforce distribution.

The dashboard provides actionable insights into:

Workforce composition by age, gender, education, department, and job role.

Employee attrition rates and trends over time.

Salary slab distributions and their correlation with attrition.

Key workforce KPIs for HR decision-making.

## 🗂️ Dataset

Source: HR Analytics Dataset (e.g., IBM HR dataset / internal HR system).

Size: ~1,400+ employee records.

Fields: Employee ID, Age, Gender, Department, Education, Job Role, Salary Slab, Years of Service, Attrition (Yes/No), etc.

## 🔧 Data Preprocessing & Transformation

Data Cleaning

Removed duplicates and inactive employee records.

Handled missing values in Salary and Education fields.

Converted categorical fields (Gender, Department, JobRole) to consistent labels.

Transformations (Power Query + DAX)

Created calculated fields:

Attrition Rate = (Attrition Count / Total Employees) * 100.

Avg Age = AVERAGE(Age).

Avg Salary = AVERAGE(Salary).

Avg Years at Company = AVERAGE(YearsAtCompany).

Created hierarchies: Department → Job Role; Education Field → Education Level.

Salary bucket transformation into bins: Up to 5k, 5k–10k, 10k–15k, 15k+.

## Modeling

Single fact table (Employees) linked with dimension attributes (Education, JobRole, Department).

Established relationships for drill-downs.

## 📌 Key KPIs

Total Employees → 1,416

Attrition Count → 229

Attrition Rate → 16.2%

Average Age → 37 years

Average Salary → 6.5K

Average Years of Service → 7 years

## 🔍 Dashboard Features

### ✅ Filters

Department (HR, R&D, Sales).

Job Role.

Gender.

### ✅ Visualizations

Attrition trends across Education Fields (Donut chart).

Attrition analysis by Age Group (Bar chart).

Workforce distribution by Education Demographics per Department (Stacked area chart).

Attrition by Salary Slab (Bar chart).

Attrition trends over Years of Service (Line chart).

Attrition by Job Role (Bar chart).

Attrition by Gender (Bar/column).

Detailed attrition counts by Job Role × Service Years (Matrix).

### ✅ Drill-Downs

Department → Job Role → Attrition Rate.

Age Group → Attrition Contribution.

Education Level → Department → Employee Count.

### 📂 Project Structure
HR-Workforce-Analysis/
│── data/                     # Raw HR dataset
│── HR_Attrition.pbix          # Power BI Dashboard file
│── images/                    # Dashboard screenshots
│── README.md                  # Documentation

📸 Dashboard Preview

### 📈 Insights from the Dashboard

Life Sciences (38%) and Medical (25%) fields dominate education backgrounds.

Majority attrition occurs in the 26–35 age group.

Highest attrition is among employees earning <5K salary slab.

Certain job roles like Sales Executive (55 attrition cases) and Lab Technician (60 attrition cases) show the highest churn.

Average attrition rate stands at 16.2%, higher in entry-level positions and early years of service.

## 🚀 Tools & Technologies

Power BI Desktop – Dashboard development.

Power Query – Data preprocessing & transformations.

DAX – KPI calculations & measures.

Excel/CSV – Source dataset.

## ✅ Next Steps

Predict attrition using machine learning models (Python/Power BI AI visuals).

Add benchmarking vs industry attrition rate.

Enable automated refresh from HR data source (SQL/SharePoint).