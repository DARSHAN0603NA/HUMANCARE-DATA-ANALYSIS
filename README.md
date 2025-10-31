# 🏥 Healthcare Data Analysis Dashboard (Power BI)

## 📌 Project Overview
This project focuses on analyzing **hospital admission data** to understand patient trends, length of stay, and readmission patterns.  
Using **Power BI**, we built an interactive dashboard that provides clear insights into hospital operations and patient outcomes.

---

## 🎯 Objectives
- Analyze patient admission and discharge patterns  
- Identify key metrics such as total patients, average stay, and readmissions  
- Visualize cost, age distribution, and department-wise admissions  
- Provide actionable insights to improve healthcare management efficiency  

---

## 🧠 Dataset Description
**Dataset Name:** `Healthcare Data Analysis for Readmission.csv`

**Main Columns:**
- `Patient_ID` – Unique ID for each patient  
- `Admission_Date` – Date of admission  
- `Discharge_Date` – Date of discharge  
- `Age` – Age of the patient  
- `Gender` – Male/Female  
- `Department` – Department admitted (e.g., Cardiology, Orthopedics, etc.)  
- `Diagnosis` – Type of disease or reason for admission  
- `Length_of_Stay` – Days stayed in hospital  
- `Readmission` – Whether the patient was readmitted or not  

---

## ⚙️ Steps Followed in Power BI

### 1️⃣ Data Import & Cleaning
- Loaded dataset into Power BI using **Get Data → CSV**  
- Checked for missing or incorrect values  
- Converted `Admission_Date` and `Discharge_Date` to **Date format**  

### 2️⃣ DAX Measures Created
```DAX
Total Patients = COUNT('Healthcare Data Analysis for Readmission'[Patient_ID])

Average Stay = AVERAGE('Healthcare Data Analysis for Readmission'[Length_of_Stay])

Average Age = AVERAGE('Healthcare Data Analysis for Readmission'[Age])

Total Readmitted = 
CALCULATE(
    COUNTROWS('Healthcare Data Analysis for Readmission'),
    'Healthcare Data Analysis for Readmission'[Readmission] = "Yes"
)

Admissions Over Time = COUNT('Healthcare Data Analysis for Readmission'[Admission_Date])

### 📊 Dashboard Visuals
Visual	Purpose
KPI Cards	Show Total Patients, Average Stay, Average Age
Bar Chart	Show Patients by Department
Column Chart	Show Length of Stay by Diagnosis
Pie Chart	Show Gender distribution
Line Chart	Show Admissions Trend over Time
🎨 Dashboard Formatting (Simple Style)

Background: Light grey or white

Fonts: Segoe UI (Default Power BI font)

Color theme: Blue, Green, Grey (healthcare-friendly)

Alignment: Use “Align” and “Distribute” options in Format tab

### 🧩 Insights

Departments with higher patient loads

Average hospital stay across conditions

Readmission trend and possible causes

Gender and age trends in admissions

### 🛠️ Tools Used

Power BI Desktop

Microsoft Excel (for dataset preparation)

### 👨‍💻 Author

Darshan N A
Branch: [Your Branch Name]
Semester: [Your Semester]
Project: Healthcare Data Analysis using Power BI

### 📁 Repository Structure
📦 Healthcare-Data-Analysis
 ┣ 📄 Healthcare Data Analysis for Readmission.csv
 ┣ 📄 PowerBI_Dashboard.pbix
 ┣ 📄 README.md
 ┗ 📁 Screenshots/

