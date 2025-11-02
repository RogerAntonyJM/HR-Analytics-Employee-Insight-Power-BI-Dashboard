
# 🧭 HR Analytics & Employee Insights Dashboard

![Dashboard Preview](HR%20Analytics%20&%20Employee%20Insight%20Dashboard.png)

---

## 📘 Project Description
This project presents an **interactive Power BI dashboard** built using four HR-related datasets to analyze key workforce metrics such as employee demographics, recruitment performance, engagement levels, training investment, and attrition trends.  
The goal is to help the HR department make **data-driven decisions** related to employee retention, satisfaction, and productivity.

---

## 🎯 Project Overview
In today’s data-driven business environment, HR analytics plays a crucial role in understanding workforce behavior and improving organizational performance.  
This dashboard integrates multiple HR datasets into one visual report to provide actionable insights into:

- Employee demographics and departmental distribution  
- Recruitment funnel (Applications → Shortlist → Hires)  
- Training & development effectiveness  
- Work-life balance and engagement trends  
- Attrition and workforce stability  

---

## 🎯 Project Objectives

1. **Understand workforce composition** by analyzing employee distribution across departments and gender.  
2. **Track recruitment efficiency** through the conversion funnel from applicants to hires.  
3. **Measure training investment** and its impact on employee engagement.  
4. **Evaluate work-life balance** and overall engagement scores from survey data.  
5. **Identify potential areas of improvement** in retention and satisfaction rates.  

---

## 🧩 Datasets Used

1. **Employee Data**
   - Employee ID, Department, Gender, Age, Salary, Tenure  
   - Used for demographic insights and departmental analysis  

2. **Employee Engagement Survey Data**
   - Engagement Score, Work-Life Balance, Satisfaction  
   - Used for calculating average engagement and well-being metrics  

3. **Recruitment Data**
   - Applicant ID, Application Date, Status (Applied, Shortlisted, Hired)  
   - Used for funnel analysis and hiring trend  

4. **Training & Development Data**
   - Employee ID, Training Hours, Training Cost, Completion Rate  
   - Used to track training investment and its effect on engagement  

---

## 🧮 Key Measures (DAX)

```DAX
Total Employees = COUNTROWS(employee_data)

Attrition Rate (%) =
DIVIDE([Employees Left], [Total Employees], 0) * 100

Average Engagement = AVERAGE(employee_engagement_survey_data[Engagement Score])

Work Life Balance Score = AVERAGE(employee_engagement_survey_data[WorkLifeBalanceScore])

Total Applicants = COUNTROWS(recruitment_data)

Shortlisted Applicants =
CALCULATE(COUNTROWS(recruitment_data),
    recruitment_data[Status] IN {"Shortlisted", "Interviewing"}
)

Hired Applicants =
CALCULATE(COUNTROWS(recruitment_data),
    recruitment_data[Status] = "Hired"
)

Total Training Cost = SUM(training_and_development_data[Training Cost])
```

---

## 📊 Key Insights from the Dashboard

1. **Workforce Overview**  
   - Total employees: 3,000 across 6 departments.  
   - Production department dominates with over 2,000 employees.  

2. **Recruitment Funnel**  
   - 3,000 total applicants, 610 hired — ~20% hire rate.  
   - 1,796 shortlisted; efficiency can improve with better screening criteria.  

3. **Work-Life Balance & Engagement**  
   - Average Work-Life Balance Score: **3.0 / 5**  
   - Indicates moderate satisfaction, suggesting need for wellness initiatives.  

4. **Training Investment**  
   - Training cost increased from **$0.68M (2022)** to **$1.0M (2023)**.  
   - Higher training correlated with improved engagement.  

5. **Attrition Rate**  
   - Overall attrition rate: **10.7%**, which is within a manageable range.  

---

## 🛠️ Tools & Technologies Used

- **Microsoft Power BI** – Data modeling, DAX calculations, visualization  
- **Microsoft Excel / CSV Files** – Data cleaning & preprocessing  
- **Power Query Editor** – Data transformation and merging  
- **GitHub** – Version control and portfolio hosting  

---

## 💡 Conclusion

This HR Analytics dashboard provides a **comprehensive view of workforce health and efficiency**.  
Through visual storytelling, HR leaders can:

- Identify departments with high attrition or low engagement.  
- Optimize training programs for better employee performance.  
- Streamline recruitment strategies for higher conversion.  
- Monitor employee well-being and satisfaction levels.  

Ultimately, this project demonstrates how **Power BI can turn raw HR data into actionable insights** to support strategic decision-making.

---

## 🚀 How to Use

1. Download the Power BI `.pbix` file from this repository.  
2. Open it in **Power BI Desktop**.  
3. Explore interactive visuals:
   - Filter by department, gender, or year.
   - View engagement trends, training investment, and recruitment metrics.

---

## 📁 Folder Structure
```
HR-Analytics-Project/
│
├── employee_data.csv
├── employee_engagement_survey_data.csv
├── recruitment_data.csv
├── training_and_development_data.csv
├── HR Analytics & Employee Insight Dashboard.png
├── HR_Analytics_Dashboard.pbix
└── README.md
```

---

## 🏁 Future Improvements

- Add predictive analysis for attrition using Power BI AI visuals.  
- Integrate live data from HR software (e.g., Workday, SAP).  
- Build an HR KPI scorecard with real-time refresh.  
