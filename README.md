# Daikibo Industrials – Data Analysis Project

A data analysis project completed as part of a **Deloitte virtual internship**, analysing telemetry and employee equality data for Daikibo Industrials across their global factories.

---

## 📁 Project Structure

```
├── daikibo-telemetry-data.json     # Raw telemetry data from factory machines
├── Task_5_Equality_Table.xlsx      # Employee compensation equality data
└── README.md
```

---

## 📊 Task 1 – Factory Downtime Analysis (Tableau)

### Objective
Analyse telemetry data collected from Daikibo's manufacturing machines to identify which factories and device types experience the most downtime.

### Steps Performed
- Imported `daikibo-telemetry-data.json` into Tableau with all schema levels selected
- Created a calculated field **"Unhealthy"** to measure downtime:
  ```
  IF [Status] = "unhealthy" THEN 10 ELSE 0 END
  ```
  *(Each unhealthy status = 10 minutes of potential downtime)*
- Built a bar chart: **Down Time per Factory**
- Built a second bar chart: **Down Time per Device Type**
- Created an interactive **Dashboard** where clicking a factory filters the device type chart

### Factories Analysed
- Daikibo Factory Meiyo (Tokyo, Japan)
- Daikibo Factory Seiko (Japan)
- Daikibo Berlin (Germany)
- Daikibo Shenzhen (China)

---

## ⚖️ Task 2 – Gender Pay Equality Classification (Excel)

### Objective
Classify employee compensation equality scores across all factories and job roles into three categories.

### Equality Classification Logic

| Equality Score | Classification |
|---|---|
| -10 to +10 | ✅ Fair |
| -20 to -11 or +11 to +20 | ⚠️ Unfair |
| Below -20 or above +20 | 🚨 Highly Discriminative |

### Output
Added a 4th column **"Equality class"** to `Task_5_Equality_Table.xlsx` using the classification logic above across all factories and job roles.

### Job Roles Covered
C-Level, VP, Director, Sr. Manager, Manager, Jr. Manager, Sr. Engineer, Engineer, Jr. Engineer, Operational Support, Machine Operator

---

## 🛠️ Tools Used

- **Tableau Desktop** – Data visualisation and dashboard creation
- **Microsoft Excel / Python (openpyxl)** – Data classification and spreadsheet editing

---

## 🏢 About

This project was completed as part of the **Deloitte Australia Data Analytics Virtual Internship** on Forage, analysing real-world style manufacturing and HR data for a fictional client, Daikibo Industrials.
