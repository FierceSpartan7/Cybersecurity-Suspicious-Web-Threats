# 🔐 Cybersecurity – Suspicious Web Threat Interaction

## 🧠 Overview
This project analyzes AWS CloudWatch web traffic logs to detect suspicious web sessions. The dataset contains **282 network traffic records from 7 countries**, including features like `bytes_in`, `bytes_out`, and `duration_seconds`.  
The goal is to identify anomalies (potential web threats) using Python-based data analysis and machine learning.

---

## 🎯 Objective
- Detect unusual web traffic patterns indicating potential attacks.  
- Analyze incoming/outgoing byte flow and session duration.  
- Use machine learning (Isolation Forest) to flag ~5% anomalies.  
- Visualize attacker IP activity and behavioral trends.

---

## 🧩 Dataset Information
**Source:** AWS CloudWatch_Traffic_Web_Attack.csv  
**Records:** 282 sessions  
**Features:**
- **bytes_in / bytes_out** → Amount of data transferred.  
- **duration_seconds** → Connection duration.  
- **rule_names / country_name** → Used for grouping suspicious activities.

---

## 🧰 Tools & Technologies
- **Python**
- **pandas, numpy** → Data preprocessing  
- **scikit-learn** → Anomaly detection (Isolation Forest)  
- **matplotlib** → Visualization  
- **Jupyter Notebook** → Analysis & documentation  

---

## 📊 Project Workflow
1. **Data Cleaning** – Handled missing values and irrelevant columns.  
2. **Feature Scaling** – Normalized numeric columns using `StandardScaler`.  
3. **Anomaly Detection** – Applied `IsolationForest(contamination=0.05)` to flag anomalies.  
4. **Results Generation** – Exported suspicious sessions and created visual insights.  
5. **Visualization** – Generated anomaly scatter plot for visual understanding.  

---

## 📁 Folder Structure
Cybersecurity-Web-Threat-Interaction/
│── data/
│ └── CloudWatch_Traffic_Web_Attack.csv
│── notebooks/
│ └── Cybersecurity_WebThreat_Interaction.ipynb
│── outputs/
│ ├── suspicious_results.csv
│ ├── traffic_stats_summary.csv
│ └── anomaly_scatter_plot.png
│── README.md
│── requirements.txt

---

## 📈 Key Insights
- Around **5% of sessions** were detected as *Suspicious*.  
- Most suspicious activities originated from a few IP clusters.  
- Byte transfer and session duration patterns helped distinguish anomalies.  

---

## 🧩 Results
- `suspicious_results.csv` → Lists all flagged sessions.  
- `traffic_stats_summary.csv` → Statistical breakdown of network traffic.  
- `anomaly_scatter_plot.png` → Visualization of anomaly vs normal sessions.  

---

## 🚀 Future Improvements
- Integrate real-time detection with cloud APIs.  
- Automate alert generation using Python scripting.  
- Add GeoIP mapping for attacker tracking.  

---

## 👨‍💻 Author
**Mohd Atikur Rehman**  
*Aspiring Data Analyst | Cybersecurity Enthusiast*  
📍 Focused on practical data-driven insights for security and analytics.  

---
📊 *“Turning data into defense — one log at a time.”*
