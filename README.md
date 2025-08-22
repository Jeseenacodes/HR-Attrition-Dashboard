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
Attrition Rate =
DIVIDE(
    SUM(HR_Data[Attrition_count]),
    SUM(HR_Data[EmployeeCount])
)
```

---



