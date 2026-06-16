# Hospital-Emergency-Room-Dashboard
# 🏥 Hospital Emergency Room Dashboard — Excel / Power BI

## Overview

An end-to-end Hospital Emergency Room (ER) Analysis Dashboard built to help hospital stakeholders **monitor patient flow, analyze ER efficiency, and make data-driven decisions**. The project covers complete data modeling, DAX formula creation, KPI design, and interactive dashboard visualization using **9,216 patient records**.

---

## 🗂️ Project Structure

```
Hospital_ER_Dashboard/
│
├── Hospital_Emergency_Room_Data.csv   → Raw patient dataset (9,216 records)
└── Dashboard (Excel)       → KPIs, Charts, Slicers, Calendar Table
```

---

## 📁 Dataset Details

| Column | Description |
|---|---|
| Patient Id | Unique patient identifier |
| Patient Admission Date | Date & time of ER visit |
| Patient First Initial / Last Name | Patient identity |
| Patient Gender | M / F |
| Patient Age | Age in years |
| Patient Race | White, African American, Native American, etc. |
| Department Referral | General Practice, Orthopedics, etc. |
| Patient Admission Flag | TRUE = Admitted, FALSE = Not Admitted |
| Patient Satisfaction Score | Score out of 10 |
| Patient Wait Time | Wait time in minutes |

**Total Records:** 9,216 patients
**Date Range:** 2023 – 2024

---

## 🔧 Tools & Features Used

| Tool/Feature | Purpose |
|---|---|
| **Power Query** | Data cleaning & transformation |
| **Calendar Table** | Time intelligence using `List.Dates()` formula |
| **DAX Formulas** | Age grouping, timeliness classification |
| **Pivot Tables** | Aggregation by department, gender, age group |
| **Charts** | Admission status, age distribution, referrals |
| **Slicers** | Filter by date, gender, department, race |
| **KPI Cards** | Avg wait time, satisfaction score, admission rate |

---

## 🧮 Key DAX Formulas

**Age Group Classification:**
```
= IF([Patient Age]>=70,"70-79",
  IF([Patient Age]>=60,"60-69",
  IF([Patient Age]>=45,"45-59",
  IF([Patient Age]>=30,"30-44",
  IF([Patient Age]>=15,"15-29",
  IF([Patient Age]>=5,"05-14","0-4"))))))
```

**Patient Attend Status (Timeliness):**
```
= IF([Patient Waittime]<30, "Within Time", "Delay")
```

**Calendar Table:**
```
= List.Dates(#date(2023,01,01), 731, #duration(1,0,0,0))
```

---

## 📈 Dashboard KPIs

- **Total Patients** seen in ER
- **Average Wait Time** (minutes)
- **Average Satisfaction Score** (out of 10)
- **Admission Rate** — % of patients admitted
- **Timeliness %** — patients seen within 30 minutes
- **Department Referral Count** — most referred departments
- **Gender Split** — M vs F patient count
- **Age Group Distribution** — 0-4 to 70-79

---

## 📊 Charts Built

| Chart | Insight |
|---|---|
| Admission Status | Admitted vs Not Admitted count |
| Age Distribution | Patient volume by age group |
| Timeliness | % seen within 30 mins vs delayed |
| Gender Analysis | Male vs Female ER visits |
| Department Referrals | Most to least referred departments |

---

## 🚀 How to Use

1. Open the Excel/Power BI file
2. Load `Hospital_Emergency_Room_Data.csv` as data source
3. Enable Power Query transformations
4. Use **Slicers** to filter by Date, Gender, Race, Department
5. KPI cards and charts update dynamically

---

## 💡 Skills Demonstrated

`Excel` · `Power BI` · `Power Query` · `DAX Formulas` · `Calendar Table` · `KPI Design` · `Data Cleaning` · `Charts` · `Slicers` · `Dashboard Design` 

---

## 👤 Author

**Saurav**
CSE Graduate | Aspiring Data Analyst
📍 Gurgaon, India
