# HR Attrition Dashboard Documentation

![Data Analytics](https://img.shields.io/badge/Data%20Analytics-Insight-blue?logo=tableau&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-Report-yellow?logo=microsoftpowerbi&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**HR attrition** (also called employee attrition) refers to the gradual reduction of a company’s workforce when employees leave the organization and are not immediately replaced.

It’s different from **turnover**, which usually means employees leaving and the company hiring new people to fill those roles. With attrition, the position may remain vacant or even eliminated.

---

## Key Points

- **Causes:** Retirement, resignation, layoffs, career changes, internal transfers, or even death.  
- **Impact:** Leads to a shrinking workforce, which can save costs but may also create skill gaps.

---

## Types of Attrition

1. **Voluntary attrition** – Employee chooses to leave (e.g., better job offer).  
2. **Involuntary attrition** – Employee leaves due to layoffs, termination, etc.  
3. **Internal attrition** – Employees move to other roles/departments within the company.  
4. **Demographic-specific attrition** – A certain group (like new hires, women, or older employees) leaving at higher rates.

---

## Tracking Attrition in HR Analytics

Attrition is often tracked as a percentage:

```text
Attrition Rate = (Number of employees who left during a period / Average number of employees during that period) × 100
```

## 1. Data Preparation & Transformation
- Imported HR dataset into Power BI.  
- Transformed the **Attrition** column from “Yes/No” into binary values (`1` for Yes, `0` for No).  
- Changed column data types for accurate calculations.  
- Ensured a clean, structured data model ready for analysis.  

---

## 2. Key Measures Created

**Attrition Rate (DAX Measure):**
```DAX
Attrition Rate = DIVIDE( SUM(HR_Data[Attrition_count]),  SUM(HR_Data[EmployeeCount]) )
```
- Converted **Attrition Rate** to **Percentage** format for better readability  
- **Average Age**  
- **Average Monthly Income** 
- **Average Years at Company**

## 3. Visualizations Implemented

- **Tree Map** → Attrition by Gender  
- **Donut Chart** →  Attrition by Education  
- **Stacked Column Chart** → Attrition by Salary distribution
- **Stacked Column Chart** → Attrition by Age groups
- **Line Chart** → Years at Company vs Attrition (filtered for < 14 years)  
- **Stacked Column Chart** → Attrition by Job Roles (Top N filter applied)  
- **Matrix Table** → Job Role, Job Satisfaction, and Sum of Attrition  

---
## 4. Insights 
![Insights](https://img.shields.io/badge/Insights-Attrition-blue)
## 1. Overall Attrition
- The organization experienced an **attrition rate of 16%**, with 238 employees leaving out of a total workforce of 1,480.
- This rate is higher than typical industry benchmarks (~10–12%).
- Average profile of employees leaving:
  - **Age:** 37 years
  - **Tenure:** 7 years
  - **Salary:** $6.5K
- Indicates mid-career professionals and moderately compensated staff contribute significantly to turnover.

## 2. Attrition by Education
- Employees with **Life Sciences and Medical degrees** account for the largest proportion of exits.
- **Technical** and **Marketing** graduates show departures in smaller numbers.
- Suggests that **knowledge-intensive/technical roles** are particularly vulnerable to turnover.

## 3. Attrition by Age
- Highest attrition occurs in employees aged **26–35**, likely seeking better opportunities elsewhere.
- Attrition declines in older age groups, indicating **more experienced staff are relatively stable**.

## 4. Attrition by Gender
- **Male employees** account for a larger share of attrition than females.
- This may reflect:
  - Role distribution
  - Market demand for certain skill sets
  - Career mobility preferences

## 5. Attrition by Salary
- Majority of attrition occurs within **lower salary bands**, particularly employees earning ≤ $5K.
- Turnover decreases as salary increases.
- Highlights the importance of **competitive compensation** for retention.

## 6. Attrition by Tenure
- Attrition shows a **bimodal pattern**:
  - Spike within the **first 1–2 years** (onboarding/early engagement challenges)
  - Smaller increase around the **10-year mark** (career stagnation/limited advancement)

## 7. Attrition by Job Role
- High turnover roles: **Research Scientists, HR professionals, Sales Representatives**
- Low turnover roles: **Manufacturing Directors, Senior-level positions**
- Suggests **role-specific retention strategies** are needed.

## 8. Job Role vs Satisfaction Analysis
- Attrition among Research Scientists, HR, and Sales employees appears **independent of job satisfaction scores**.
- Indicates other factors like:
  - Workload
  - Compensation
  - Growth opportunities
- Organizational/structural issues in these functions need attention to improve retention.

## Key Takeaways / Recommendations
- **Target 26–35 Age Group**: Implement career development and fast-track promotions to reduce mid-career attrition.  
- **Review Compensation**: Majority of attrition occurs for salaries <5K; adjust pay packages.  
- **Enhance Early Engagement**: High attrition at 1–2 years points to onboarding, mentorship, and role-fit issues.  
- **Focus on Research Scientist & HR Roles**: These roles show high attrition; apply targeted retention strategies.  
- **Assess Gender Dynamics**: Higher male attrition may reflect job-role concentration or work-life balance concerns.  
- **Support Long-Tenure Employees**: Prevent exits around 10 years with leadership tracks, reskilling, or internal mobility.

---
