# Overnight ED & Imaging Operations Dashboard 📊🏥

## 🔍 Project Overview

This project explores real-time Emergency Department (ED) and Imaging Department performance during overnight shifts (9 PM – 6 AM), using data I collected manually while working on-site. 

The goal? To uncover operational bottlenecks, identify patterns in patient and imaging flow, and generate actionable insights that could help improve care delivery and resource planning.

## 📈 Why This Matters

Emergency departments often face strain during night hours, with limited staffing and rising patient needs. By analyzing what happens *hour by hour*, we can better understand where delays occur — and how we might address them using data-driven approaches.

This project is a small, ethically guided step toward **smarter, real-time healthcare systems**.

---

## 🗂️ Dataset Description

Data was manually collected in Excel during several overnight shifts at a hospital and organized into 3 sheets:

### Sheet 1: ED Flow & Wait Times
- Total ED patients per hour
- Patients waiting to see a doctor (per hour)
- Wait time to see a doctor (per hour)
- Total time spent in ED (per hour)
- Imaging wait times (CT, XR, US)
- Pending scans (CT, XR, US)

### Sheet 2: Imaging Orders & Completions
- XR and CT scans ordered per hour
- XR and CT scans completed per hour

### Sheet 3: Scan Duration
- Ordered time, scan start time, and scan completion time for XR and CT
- Calculated scanning durations
- Grouped by complexity:
  - `CT++` = multi-region or contrast-based CTs (e.g., CT Spine + Head)
  - `CT` = single-region CT
  - `XR++` = multi-view X-rays
  - `XR` = single-view X-rays

---

## 🧽 Data Cleaning & Prep

Performed in **SQL** (Microsoft SQL Server):

- Removed irrelevant/blank columns
- Standardized null values
- Flagged and excluded inconsistent timestamps
- Calculated derived metrics (e.g., scan time in minutes)

---

## 📊 Power BI Dashboard

Built a 3-page interactive dashboard with slicers and KPIs. Here's a breakdown:

### **Page 1: ED Wait Times & Patient Flow**
- Line chart: ED wait time to see a doctor vs. total wait time
- Line chart: Hourly ED patient volume vs. patients waiting for doctor
- Card: Number of doctors on shift (based on hour selected)
- Slicer: Select hour between 9 PM – 6 AM

### **Page 2: Imaging Wait Times**
- Ribbon chart: Imaging wait time by modality (CT, XR, US)
- Line chart: Pending scans by hour (CT, XR, US)
- Slicer: Select hour of the night

### **Page 3: Imaging Operations & Scan Time**
- Clustered column chart: XR Orders vs Completions
- Clustered column chart: CT Orders vs Completions
- Pie chart: XR operational strength (completed vs. ordered)
- Pie chart: CT operational strength (completed vs. ordered)
- Bar chart: Average scan time for CT++, CT, XR++, XR

---

## 💡 Key Insights

- **Wait time to see a doctor** was ~1–2 hrs, while **total time in ED** was ~5–6 hrs.
- **CT scans** had the longest wait times, with fluctuations throughout the night.
- **XR scans** were consistent and had minimal wait times.
- **Backlogs** were being cleared: CT and XR completed more scans than ordered.
- **Scan durations** increased with complexity (CT++ ~10 min, XR ~4 min).
- **Staffing levels** dropped over the night (from 4 doctors at 9 PM to 2 by 3 AM), influencing trends.

---

## 🛡️ Ethical Considerations

All data was **de-identified** and handled in alignment with:
- **PHIPA (Personal Health Information Protection Act)** regulations
- **Internal hospital policies**
- Departmental guidance on privacy and appropriate use

This project was conducted **purely for learning and research** purposes, with approvals from relevant stakeholders.

---

## 🚀 Future Improvements

- Incorporate transportation staffing data to correlate with delays
- Automate real-time data collection (e.g., with EPIC or imaging system APIs)
- Build predictive models to anticipate peak periods
- Expand to daytime and weekend shifts
- Include lab, bed assignment, and admission timing metrics

---

## 👨‍⚕️ About Me

I'm a healthcare data analyst focused on real-time operational improvements in hospital systems. I’m passionate about using data to streamline care, reduce delays, and support frontline staff with actionable insights.

Connect with me on [LinkedIn](https://www.linkedin.com/in/Oseaga/)  
Check out my portfolio: [datascienceportfol.io/Oseaga](https://www.datascienceportfol.io/Oseaga)

---

## 📬 Feedback & Collaboration

Have ideas, feedback, or similar projects you're working on?  
I’d love to connect — feel free to open an issue or reach out via LinkedIn.

---

## 🔖 Tags

`#HealthcareAnalytics` `#PHIPACompliant` `#PowerBI` `#SQL` `#EDFlow` `#ImagingOps` `#HealthTech` `#DataEthics` `#RealTimeHealthcare` `#OperationalEfficiency`

