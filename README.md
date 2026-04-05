# 🔍 Benford Law for Audit Analysis (R)

## 📊 Overview

This project applies **Benford’s Law** to detect anomalies in financial data using R.

Benford’s Law predicts that in real-world datasets, the number 1 appears as the first digit about 30% of the time, while higher digits occur less frequently.

When data deviates from this pattern, it may indicate inconsistencies or manipulation.

---

## ⚙️ Methodology

- Generate simulated accounting data  
- Introduce artificial anomalies  
- Extract first digits  
- Compare observed vs expected distribution  
- Apply Chi-Square test  
- Identify suspicious records  

---

## 📈 Example Output

The chart above compares:

- 🔵 Observed distribution  
- 🔴 Expected Benford distribution  

Significant deviations suggest potential anomalies.

---

## 🚨 Key Insight

A very low p-value indicates that the dataset does not follow Benford’s Law.

This does not prove fraud, but strongly suggests the need for further investigation.

---

## 🛠️ Technologies

- R  
- Statistical Analysis  
- Data Simulation  

---

## 📌 Future Improvements

- Apply to real financial datasets  
- Build dashboard using Shiny  
- Integrate machine learning models  

---

## 👨‍💻 Author

Project focused on **audit analytics, data science, and fraud detection**.
