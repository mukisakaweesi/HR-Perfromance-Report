# 👥 HR Performance Dashboard

## 📚 Table of Contents
1. [Project Overview](#1-project-overview)  
2. [Data Sources](#2-data-sources)  
3. [Tools Used](#3-tools-used)  
4. [Data Cleaning and Preparation](#4-data-cleaning-and-preparation)  
5. [Exploratory Data Analysis (EDA)](#5-exploratory-data-analysis-eda)  
6. [Data Analysis](#6-data-analysis)  
7. [Results & Findings](#7-results--findings)  
8. [Recommendations](#8-recommendations)  
9. [Limitations](#9-limitations)  
10. [References](#10-references)

---

## 1. Project Overview

This project focuses on analyzing key human resource metrics to better understand workforce dynamics and drive data-informed decisions. Using MySQL for data exploration and Power BI for visualization, the project dives into various aspects such as:

Employee distribution by department, state, and city

Demographics breakdown by gender, age, and race

Remote vs. headquarters employment ratios

Termination rates across departments

Historical employment trends from 2000 to 2020

The final output is an interactive Power BI dashboard that gives HR managers, analysts, and executives a 360° view of organizational performance. The goal is to identify strengths, flag areas of concern (like high turnover in specific departments), and recommend actionable strategies for employee retention, diversity, and workforce planning.



---

## 2. Data Sources

The dataset used was a fictional HR dataset, designed to simulate real corporate employee records. It included:
- Employee ID, department, and role  
- Demographics (gender, race, age group)  
- Employment type and location  
- Termination history and net employment change over time  

---

## 3. Tools Used

- **MySQL** for querying and exploring relational datasets  
- **Power BI Desktop** for dashboard development and interactive visuals  
- **Microsoft Excel** for quick inspections and preliminary formatting  

---

## 4. Data Cleaning and Preparation

Performed using SQL and Excel:
- Removed duplicate records and null entries  
- Standardized categorical fields (e.g., job roles, locations, age groups)  
- Created new columns such as age group and years of service  
- Joined multiple tables on `employee_id` to consolidate data  

---

## 5. Exploratory Data Analysis (EDA)

Using **SQL**:
- Aggregated employee counts by gender, race, department, and location  
- Queried age group distribution by gender  
- Calculated termination rates by department  
- Analyzed year-over-year employment changes using date functions  
- Identified which departments had the highest turnover  
Example SQL snippets used:
```sql
SELECT department, COUNT(*) AS employee_count
FROM employees
GROUP BY department;

SELECT gender, age_group, COUNT(*) 
FROM employees
GROUP BY gender, age_group;
```

## 6. Data Analysis

Using **SQL** and **Power BI**:

- Created aggregated tables for gender, age, department, and location  
- Built custom **DAX measures** in Power BI to calculate:  
  - Termination rates  
  - Average length of service  
  - Distribution by department and region  
- Mapped employee locations by city/state using Power BI’s map visuals  
- Tracked historical net employment change (2000–2020)

---

## 7. Results & Findings

- **Geographic concentration**: 75% of employees work at headquarters, primarily in Ohio and Pennsylvania  
- **Age distribution**: The 25–30 age group had the largest share of employees  
- **Gender & diversity**: Gender ratio was relatively balanced overall, but some departments (like Engineering and Auditing) had male dominance  
- **Departmental turnover**: Marketing and Auditing had the highest termination rates  
- **Positive trend**: Employment showed a steady recovery and growth after dips in the early 2010s  

---

## 8. Recommendations

- Conduct audits in departments with high termination rates (Marketing, Auditing) to assess workplace satisfaction  
- Support inclusion and diversity by hiring more underrepresented genders and races in tech and leadership roles  
- Focus on younger employees (25–30 age group) with development programs and mentorship  
- Expand remote work policies, as remote employment has steadily grown and shows productivity benefits  

---

## 9. Limitations

- The dataset is synthetic and may not reflect complex real-world employee behaviors  
- No salary, performance ratings, or feedback loops were included to link with turnover  
- External influences like economic downturns or company policy changes were not factored into the analysis  
- Predictive modeling was out of scope — the focus was descriptive and exploratory  

---

## 10. References

- [Power BI Documentation](https://learn.microsoft.com/en-us/power-bi/)  
- [MySQL Documentation](https://dev.mysql.com/doc/)  
- [OpenStreetMap](https://www.openstreetmap.org/copyright)  
- [TomTom Map API](https://developer.tomtom.com/)  
- [HR Analytics Best Practices – IBM](https://www.ibm.com/topics/hr-analytics)  


