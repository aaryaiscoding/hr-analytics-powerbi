# 📊 HR Analytics Dashboard
### Built with Power BI | DAX | Power Query

> An interactive, multi-page Power BI dashboard analyzing employee attrition across **1,470 records** from IBM's HR dataset. Designed to surface workforce risk patterns, compensation trends, and key drivers of employee turnover — enabling data-driven HR decision-making.

---

## 🖼️ Dashboard Preview

| Overview | Attrition Drivers | Compensation |
|----------|------------------|--------------|
| ![Overview]<img width="608" height="329" alt="image" src="https://github.com/user-attachments/assets/f512580d-9a3d-4194-bd1f-bbab4505e9ed" />
| ![Attrition Drivers]<img width="608" height="341" alt="image" src="https://github.com/user-attachments/assets/62746fd7-ae2b-40ff-b723-4eadf4f89cff" />
 | ![Compensation]<img width="609" height="338" alt="image" src="https://github.com/user-attachments/assets/6961a37e-7a48-4b2c-9cde-6d48b4706880" />
 |

---

## 📁 Project Structure

```
hr-analytics-powerbi/
├── HR_Analytics_Dashboard.pbix
├── dataset/
│   └── WA_Fn-UseC_-HR-Employee-Attrition.csv
├── screenshots/
│   ├── overview.png
│   ├── attrition_drivers.png
│   └── compensation.png
└── README.md
```

---

## 🔍 Key Insights

- 👤 **16% overall attrition rate** across 1,470 employees
- ⏰ Employees working **overtime leave at 3x the rate** of those who don't
- 😞 **Low job satisfaction** is the strongest single predictor of attrition
- 💸 Younger employees earning **below $5K/month** account for the majority of departures
- 🏆 **Managers and Research Directors** earn significantly more than all other roles
- 🎓 Employees with **doctoral degrees** earn ~30% more than those with bachelor's degrees

---

## 📐 DAX Measures

```dax
Headcount = COUNTROWS(Employees)

Attrition Count = 
    CALCULATE(COUNTROWS(Employees), Employees[Attrition] = "Yes")

Attrition Rate = 
    DIVIDE(
        CALCULATE(COUNTROWS(Employees), Employees[Attrition] = "Yes"),
        COUNTROWS(Employees),
        0
    )

Avg Monthly Income = AVERAGE(Employees[MonthlyIncome])

Avg Tenure = AVERAGE(Employees[YearsAtCompany])

Avg Age = AVERAGE(Employees[Age])
```

---

## 🛠️ Tools & Skills

| Area | Details |
|------|---------|
| **Visualization** | Power BI Desktop |
| **Data Transformation** | Power Query (M language) |
| **Calculations** | DAX measures |
| **Data Source** | IBM HR Analytics — Kaggle |

---

## 📂 Dataset

[IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

1,470 employee records across 35 features including department, job role, monthly income, overtime, job satisfaction, years at company, and attrition status.

---

## 🚀 How to Open

1. Download `HR_Analytics_Dashboard.pbix`
2. Open with [Power BI Desktop](https://powerbi.microsoft.com/desktop) (free)
3. Use the slicers on each page to filter by Department, Gender, and Job Role

---

*Built as part of a data analytics portfolio — focused on HR workforce risk assessment and compensation analysis.*
