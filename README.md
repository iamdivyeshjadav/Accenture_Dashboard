<div align="center">

# -- ! Accenture India HR Analytics Dashboard ! --
### *Interactive Power BI Dashboard for Workforce, Attrition, Compensation & Performance Analytics*

[![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Measures%20%26%20KPIs-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/dax/)
[![Data Model](https://img.shields.io/badge/Data%20Model-Star%20Schema-4CAF50?style=for-the-badge&logo=databricks&logoColor=white)](https://powerbi.microsoft.com/)
[![HR Analytics](https://img.shields.io/badge/Domain-HR%20Analytics-A100FF?style=for-the-badge&logo=accenture&logoColor=white)](https://powerbi.microsoft.com/)

<br/>

> *"Behind every headcount is a person — a good dashboard helps you see them."*

</div>

---

## 📋 Table of Contents

- [📌 Overview](#-overview)
- [🎯 Problem Statement](#-problem-statement)
- [✨ Key Features](#-key-features)
- [🏗️ Project Structure](#️-project-structure)
- [🔄 Project Workflow](#-project-workflow)
- [👥 Part A — Workforce Overview](#-part-a--workforce-overview)
- [🚪 Part B — Attrition & Retention](#-part-b--attrition--retention)
- [💰 Part C — Compensation Analytics](#-part-c--compensation-analytics)
- [🏅 Part D — Performance & Promotion](#-part-d--performance--promotion)
- [🧭 Part E — Executive Summary](#-part-e--executive-summary)
- [🛠️ Tech Stack](#️-tech-stack)
- [📈 Results & Insights](#-results--insights)
- [🏆 Advantages](#-advantages)
- [📄 License](#-license)
- [👤 Author](#-author)
- [🙏 Acknowledgements](#-acknowledgements)

---

## 📌 Overview

The **Accenture India HR Analytics Dashboard** is an interactive, five-page **Power BI** report that gives HR leaders a complete view of the workforce. It covers headcount and hiring, attrition and retention, salary and pay equity, performance ratings, promotions and training, and ends with a one-page executive summary. The report is designed at **2560 × 1440** with a purple and white theme, KPI cards, slicers, maps, drill-down tables and a page navigator.

This project is designed to:
- Track **headcount**, **active employees**, **tenure** and **hiring trends**
- Understand **who leaves and why** through attrition and retention analysis
- Compare **salary** by department, job level, location, gender and experience
- Measure **performance**, **promotions** and **training completion**
- Practice **star-schema data modeling**, **DAX measures** and **dashboard design** in Power BI

---

## 🎯 Problem Statement

> **Objective:** Build an interactive HR dashboard that helps leadership monitor workforce health and make decisions on hiring, pay, retention and development.

HR data is usually scattered across systems for employees, payroll, exits, reviews and training. This dashboard brings it into one data model, so any metric can be filtered by department, business unit, job level, city, gender and year.

| 📂 Table | 📄 Type | 🔍 Description |
|----------|---------|----------------|
| DimEmployee | Dimension | Employee attributes such as gender |
| DimDepartment | Dimension | Department name and business unit |
| DimJobLevel | Dimension | Job level of each employee |
| DimLocation | Dimension | City-level location data used in maps and slicers |
| DimDate | Dimension | Date table with year, quarter, month and fiscal quarter |
| FactWorkforce | Fact | Salary band, experience years and workforce records |
| FactAttrition | Fact | Exit records with attrition reasons |
| FactPerformance | Fact | Performance reviews and ratings |
| FactTraining | Fact | Training enrollments, course category and status |
| FactRecruitment | Fact | Candidates by recruitment stage |
| MeasureTable | Measures | Holds all DAX measures and KPIs |

The goal is to demonstrate **end-to-end BI skills** — from a star-schema model to measures to a polished, navigable report.

---

## ✨ Key Features

| Feature | Description |
|--------|-------------|
| 📑 **5 Report Pages** | Workforce, Attrition, Compensation, Performance and Executive Summary |
| 🎛️ **Rich Slicers** | Filter by Department, Business Unit, Job Level, City, Gender, Year and Quarter |
| 🔢 **KPI Cards** | Total Employees, Active Employees, Attrition Rate, Retention Rate, Avg Salary, Avg Rating, Promotion Rate and more |
| 🗺️ **Maps** | Employee, salary, attrition and high-performer distribution by city |
| 🔽 **Drill-down Tables** | Summary tables by Business Unit and Department |
| 🍩 **Distribution Donuts** | Workforce by gender, salary by gender, training status |
| 📈 **Trend Charts** | Hiring trend by fiscal quarter and month |
| 🔵 **Scatter Charts** | Attrition vs average salary, and salary vs experience |
| 🔻 **Recruitment Funnel** | Candidates by recruitment stage |
| 💡 **Key Insights Panels** | Written takeaways placed beside the charts on each page |

---

## 🏗️ Project Structure

```
📦 accenture-hr-dashboard/
│
├── 📄 Accenture_Dashboard.pbix   ← Power BI report (data model + 5 pages)
│
└── 📄 README.md                  ← Project documentation
```

---

## 🔄 Project Workflow

```
Raw HR Data (Employees · Payroll · Exits · Reviews · Training · Hiring)
      │
      ▼
┌─────────────────────────────┐
│   Load & Clean Data         │  ← Dimension and fact tables
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   Build Star Schema         │  ← Dim tables + Fact tables + MeasureTable (DAX)
└────────────┬────────────────┘
             │
   ┌─────────┼─────────┬──────────┐
   ▼         ▼         ▼          ▼
┌────────┐┌─────────┐┌──────────┐┌─────────────┐
│Workforce││Attrition││Compensa- ││Performance  │
│Overview ││& Retent.││tion      ││& Promotion  │
└───┬────┘└────┬────┘└────┬─────┘└──────┬──────┘
    └──────────┴──────────┴─────────────┘
                      │
                      ▼
        ┌─────────────────────────┐
        │   Executive Summary     │
        └────────────┬────────────┘
                     │
                     ▼
   Slicers + KPI Cards + Charts Update
                     │
                     ▼
        Insights for HR Leadership ✅
```

---

## 👥 Part A — Workforce Overview

### 📝 1. What does this page show?

The **Workforce Overview** page answers: *how big is the workforce, where is it, and how is it changing?*

---

### 🗺️ 2. Visuals — Overview

| Visual | Type | Fields Used |
|--------|------|-------------|
| 🔢 Total / Active Employees | KPI Cards | `Total Employees`, `Active Employees` |
| 📉 Attrition Rate | KPI Card | `Attrition Rate` |
| ⏳ Average Tenure | KPI Card | `Average Tenure` |
| ⚖️ Gender Ratio | KPI Card | `Gender Ratio` |
| 📈 Hiring Trend | Line Chart | `FY Quarter`, `Month Name`, `New Hires` |
| 🍩 Workforce Composition | Donut | `Gender`, `Total Employees` |
| 🗺️ Employee Distribution by Location | Map | `City`, `Total Employees` |
| 📊 Employee Distribution by Department | Clustered Column | `DepartmentName`, `Total Employees` |
| 🧾 Workforce Summary | Table | `Business Unit`, `DepartmentName`, `Total Employees`, `% of Total`, `Attrition Rate`, `Avg Salary LPA`, `Avg Experience` |

**Slicers:** Department, Business Unit, Job Level, City, Gender, Year, Quarter

---

## 🚪 Part B — Attrition & Retention

### 🔍 3. What does this page show?

The **Attrition & Retention** page answers: *how many people leave, from where, and why?*

| Visual | Type | Fields Used |
|--------|------|-------------|
| 🔢 Attrition Count / Rate | KPI Cards | `Attrition Count`, `Attrition Rate` |
| 🛡️ Retention Rate | KPI Card | `Retention Rate` |
| ⏳ Avg Exit Tenure | KPI Card | `Avg Exit Tenure` |
| 📈 Attrition Trend | Line Chart | `AttritionReason`, `Attrition Count` |
| 📊 Attrition by Job Level | Clustered Column | `JobLevel`, `Attrition Count` |
| 🍩 Attrition by Gender | Donut | `Gender`, `Attrition Count` |
| 🗺️ Attrition by Location | Map | `City`, `Attrition Count` |
| 📊 Attrition by Department | Clustered Bar | `DepartmentName`, `Attrition Count` |
| 🟦 High-Risk Employee Segment | Treemap | `DepartmentName`, `Attrition Count` |
| 🧾 Department Summary | Table | `Attrition Count`, `Attrition Rate`, `Avg Exit Tenure` |

**Slicers:** Department, Job Level, City, Gender, Year

---

## 💰 Part C — Compensation Analytics

### 💵 4. What does this page show?

The **Compensation Analytics** page answers: *how is pay distributed, and is it fair across gender, level and location?*

| Visual | Type | Fields Used |
|--------|------|-------------|
| 🔢 Salary KPIs | KPI Cards | `Avg Salary LPA`, `Median Salary LPA`, `Highest Salary LPA`, `Total Payroll Cr`, `Employees Covered` |
| 🍩 Salary by Gender | Donut | `Gender`, `Avg Salary LPA` |
| 📊 Salary Distribution | Clustered Column | `Salary Band`, `Employees Covered` |
| 📊 Average Salary by Department | Clustered Bar | `DepartmentName`, `Avg Salary LPA` |
| 📊 Average Salary by Job Level | Clustered Column | `JobLevel`, `Avg Salary LPA` |
| 🗺️ Salary by Location | Map | `City`, `Employees Covered` |
| 🔵 Salary vs Experience | Scatter | `Exp Years`, `Avg Salary LPA`, `PerformanceRating` |
| 🧾 Salary Summary | Matrix | Department and Job Level with employees, payroll, average, median, min and highest salary |

**Slicers:** Department, Job Level, City, Gender

---

## 🏅 Part D — Performance & Promotion

### 🔍 5. What does this page show?

The **Performance & Promotion** page answers: *how well are employees performing, who gets promoted, and is training effective?*

| Visual | Type | Fields Used |
|--------|------|-------------|
| 🔢 Performance KPIs | KPI Cards | `Avg Rating`, `High Performers`, `Promotion Rate`, `Training Completion %` |
| 📊 Performance Rating Distribution | Clustered Column | `PerformanceRating`, `Performance Reviews` |
| 📊 Promotions by Department | Clustered Bar | `DepartmentName`, `Promotions` |
| 🍩 Training Completion Analysis | Donut | `Status`, `Training Total` |
| 📈 Training Trend | Line Chart | `CourseCategory`, `Training Completion %` |
| 🗺️ Performance by Location | Map | `City`, `High Performers` |
| 🧾 Performance Summary | Matrix | Employees, rating, promotions, promotion rate, training %, high performers, high performer % |

**Slicers:** Department, Business Unit, City, Gender

---

## 🧭 Part E — Executive Summary

### 🔍 6. What does this page show?

The **Executive Summary** page is a one-screen view for leadership, titled *"Strategic overview of workforce health and HR performance"*.

| Visual | Type | Fields Used |
|--------|------|-------------|
| 🔢 Headline KPIs | KPI Cards | `Total Employees`, `Attrition Rate`, `Avg Salary LPA`, `Promotion Rate`, `High Performers`, `Data As On` |
| 🟦 Workforce Cost by Department (₹ Cr) | Treemap | `DepartmentName`, `Total Payroll Cr` |
| 🔵 Attrition % vs Average Salary | Scatter | `Attrition Rate`, `Avg Salary LPA`, `Total Employees` |
| 🗺️ Performance by Location | Map | `City`, `Total Employees` |
| 🔻 Recruitment Funnel | Funnel | `Stage`, `CandidateID` |
| 🧾 Workforce Summary | Table | Attrition, salary, rating, promotion, training and health score by department |

---

## 🛠️ Tech Stack

| Tool | Version | Purpose |
|------|---------|---------|
| 📊 **Power BI Desktop** | Latest | Report authoring and data modeling |
| 🧮 **DAX** | Built-in | Measures such as Attrition Rate, Retention Rate, Avg Salary LPA, Promotion Rate, High Performer % and Health Score |
| 🗃️ **Data Model** | Star schema | 5 dimension tables, 5 fact tables and 1 measure table |
| 🗺️ **Map Visuals** | Built-in | City-level distribution of employees, salary, attrition and performance |
| 🧭 **Page Navigator & Buttons** | Built-in | Moving between the five pages |
| 🖼️ **Custom Icons** | PNG | Purple and white icons for sections and KPI cards |

---

## 📈 Results & Insights

The dashboard's own insight panels report the following:

- 👥 **Workforce:** 50,000 total headcount, with 48,006 active (96.0%)
- 📍 **Location:** Bengaluru has the largest employee base (4,245)
- ⏳ **Tenure:** Average tenure is 10.3 years, with 12.8 years of average experience
- 🚪 **Attrition:** Rate is 16.0% with 8,000 exits; top exit reason is Better Salary (20.5% of exits)
- 🏢 **Department:** SAP has the highest attrition count (575) at a rate of 16.5%
- 💰 **Salary:** Average ₹31.4 LPA with a median of ₹31.3 LPA; gender pay gap is 0.44%
- 🏅 **Performance:** Average rating is 3.6 out of 5 across 150,000 reviews; 45.3% (22,659) are high performers
- 📚 **Training:** Completion rate is 92.0% across 250,000 enrollments

---

## 🏆 Advantages

| Advantage | Detail |
|-----------|--------|
| 🎓 **Complete HR View** | Workforce, attrition, pay, performance and training in one report |
| 🎛️ **Flexible Filtering** | Slicers for department, business unit, level, city, gender and year |
| 🔄 **Reusable Model** | Star schema with a dedicated MeasureTable for all DAX measures |
| 🔽 **Drill Down** | Business Unit to Department summary tables and date drill-downs |
| 🗺️ **Location Insight** | Maps on four pages show where each metric is concentrated |
| 💡 **Built-in Insights** | Key takeaways written directly on each page |
| 🧪 **Extensible** | Easy to add pages such as Recruitment or Diversity |
| 🖥️ **Clean Layout** | Consistent 2560 × 1440 design with a page navigator |

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for full details.

```
MIT License — Free to use, modify, and distribute with attribution.
```
## Workforce Overview
<img src="assest/page 1.png">

---

## Attrition & Retention

<img src="assest/page 2.png">

---
## Compensation Analytics

<img src="assest/page 3.png">

---
## Performance & Promotion

<img src="assest/page 4.png">

---
## Executive Summary

<img src="assest/page 5.png">

## 👤 Author

<div align="center">

### Divyesh Jadav

[![GitHub](https://img.shields.io/badge/GitHub-yourhandle-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/yourhandle)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/your-profile/)

> *"Every dashboard starts with a question — and ends with a better decision."*

**🎓 Role:** Data Analyst | Power BI Enthusiast \
**📍 Location:** India\
**🛠️ Skills:** Power BI · DAX · Data Modeling · Dashboard Design · Data Visualization

</div>

---

## 🙏 Acknowledgements

Special thanks to the following resources and communities that made this project possible:

- 📚 [Power BI Documentation](https://learn.microsoft.com/en-us/power-bi/) — Official Power BI reference
- 🧮 [DAX Guide](https://dax.guide/) — Complete DAX function reference
- 🎨 [Power BI Report Design Guidance](https://learn.microsoft.com/en-us/power-bi/guidance/) — Layout and design best practices
- 🖥️ [Microsoft Learn — Power BI](https://learn.microsoft.com/en-us/training/powerplatform/power-bi) — Beginner to advanced courses
- 💬 [Power BI Community](https://community.fabric.microsoft.com/) — Problem-solving support
- 📖 [Kaggle Learn](https://www.kaggle.com/learn) — Data and analytics courses

---

<div align="center">

---

*Made with ❤️ and ☕ — Last updated: 6 November, 2026*

</div>
