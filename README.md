# emergency-room-performance-dashboard
End-to-end ER performance analysis project using Excel (data cleaning &amp; derived columns) and Tableau (dashboarding). Highlights patient demand patterns, wait time vs severity, arrival modes, and cost contribution trends. Built purely for educational and portfolio demonstration purposes.
### Dataset Source
Dataset used for this project is publicly available for educational purposes:
**Healthcare Dataset – Kaggle**  
https://www.kaggle.com/datasets/prasad22/healthcare-dataset
    **This dataset is synthetic and does not contain real patient-  identifiable information.*

---

### Data Preparation (Excel & Power Query)
After reviewing the raw dataset, additional derived fields were created to enable analysis:
| Column Name | Method | Purpose |
| **Triage Level** | IF / Nested IF formula based on *Patient Condition Severity* | Categorized patients into severity levels (1 = Critical → 5 = Non-Urgent) |
| **Arrival Mode** | Standardized using Power Query (ambulance, referral, walk-in) | Grouped arrival categories for comparison |
| **Treatment Time (mins)** | Calculated using `End Time – Start Time` | Measured care duration per patient |
| **Cost** | Assigned cost ranges by severity | Enabled cost-based utilization analysis |
**Unnecessary columns removed:**  
Patient Last Name, Race, Insurance ID, Address fields, and other non-analytical attributes.

---

### Tableau Dashboard KPIs

| KPI | Description |
| **Total Patient Volume** | Total ER visits during the analyzed period |
| **Average Patient Satisfaction Score** | Overall satisfaction indicator |
| **Peak Admission Hour** | Identified busiest time (11 AM) |
| **Average Wait Time** | Compared to 30-minute service target |
| **Average Patient Age** | Demographic indicator |

---

### Analysis Performed
1. **Patient Volume Trends**  
   Compared quarterly admission patterns to understand seasonal demand shifts.
2. **Weekday vs Weekend Admissions**  
   Visualized arrival mode differences between weekday and weekend cases.
3. **Wait Time by Triage Severity**  
   Identified that higher-severity patients wait longer and require more care time.
4. **Age Group Admission Insights**  
   Found consistent distribution of cases across age groups.
5. **Cost Impact by Severity**  
   Waterfall chart shows highest cost impact for severity levels 1–2.

---

### Key Insights / Conclusion
- The ER sees **peak patient volume around 11 AM**, especially on **weekdays and walk-in patients**, indicating a need to adjust staffing during late morning hours.
- **Higher-severity cases** drive **longer wait times and higher treatment costs**, suggesting opportunities for **triage protocol optimization and fast-track lanes**.

---

### Possible Improvements
| Area | Suggested Change |
| Staffing | Increase nurse/doctor coverage between 10 AM – 1 PM |
| Triage Workflow | Implement fast-track for low-severity cases |
| Patient Flow | Improve routing to reduce bottlenecks in peak hours |

---

### Files in This Repository

| File | Description |
|-----|-------------|
| `Hospital_ER_Data_Clean.xlsx` | Cleaned dataset used in Tableau |
| `Emergency Room Dashboard.twbx` | Tableau dashboard workbook |
| `README.md` | Project documentation |

---

### Purpose
This project is purely for **educational and analytical purposes**.  
No real patient data was used, and no personal or confidential information is included.

---

### Developed By
**Tejaswi.v**  
Master’s Student | Healthcare informatics 
