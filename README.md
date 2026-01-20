# UIDAI Data Hackathon 2026: Tempo-Spatial Analysis of Aadhaar Activity

[cite_start]**Team Members:** Dheerajpreet Singh, Rishit Gakhar, Swastik Panda (IIT Roorkee) [cite: 5]

## 📌 Project Overview
[cite_start]This project addresses the uneven distribution of Aadhaar service usage across India[cite: 10]. [cite_start]While some mature states face infrastructure stress due to high update volumes, remote districts remain underserved[cite: 10]. [cite_start]Our approach moves beyond simple volume reporting to build data-driven indicators for fair access and system reliability[cite: 13, 15].

## 🛠️ Methodology & Technical Stack
### Data Preprocessing
[cite_start]We implemented a robust pipeline to handle significant data anomalies found in the initial datasets[cite: 300, 311]:
* [cite_start]**Canonicalization:** Standardized misspelled state/district names and resolved historical boundary changes (e.g., Telangana-Andhra Pradesh split)[cite: 212, 239, 277].
* [cite_start]**Anomaly Mitigation:** Identified "first-of-the-month" data concentration issues and utilized monthly aggregation to ensure statistical reliability[cite: 356, 361].

### Feature Engineering
[cite_start]We developed custom metrics to measure system performance and priority[cite: 495]:
* [cite_start]**Maintenance Stress Index (MSI):** Measures the burden of update activity relative to new enrollments[cite: 652].
* [cite_start]**Outreach Priority Score (OPS):** A population-adjusted score identifying high-impact zones for service expansion[cite: 704].
* [cite_start]**Gini Coefficient Analysis:** Used to track Aadhaar access inequality over time, showing a drop in per-capita inequality from ~0.93 to ~0.50[cite: 464, 468].

### Clustering
[cite_start]Using **K-Means Clustering** ($k=5$ for districts; $k=3$ for states), we segmented regions into distinct maturity profiles[cite: 779, 788, 789]:
1. [cite_start]**High-Pressure Mature Systems:** Very high biometric load (e.g., UP, Maharashtra)[cite: 835].
2. [cite_start]**Education-Driven Systems:** Teen-dominated enrollment structures[cite: 829].
3. [cite_start]**Low-Digitization Rural:** High priority for mobile enrollment centers[cite: 861].

## 📊 Key Insights
* [cite_start]**Service Dominance:** Biometric updates dominate total activity (~68M) compared to demographic updates (~36M) and enrollments (~5M)[cite: 434, 450, 447].
* [cite_start]**Temporal Patterns:** Activity peaks midweek and drops sharply on weekends, indicating office-driven operational patterns[cite: 429].
* [cite_start]**Concentration:** The top 30% of states account for 70-75% of total Aadhaar activity[cite: 490].

## 🚀 Recommendations
* [cite_start]**Infrastructure Scaling:** Automate processes in "Cluster 0" high-pressure zones to reduce maintenance stress[cite: 861].
* [cite_start]**Targeted Outreach:** Deploy mobile units specifically to high-OPS states like **Meghalaya**[cite: 667, 861].
* [cite_start]**School Integration:** Plan for peak periods by integrating Aadhaar updates directly with educational cycles for the 5-17 age group[cite: 861].

## 📂 Repository Structure
* `/data`: Preprocessing scripts for cleaning and state-split corrections.
* `/notebooks`: EDA, Lorenz Curve generation, and K-Means implementation.
* `/src`: Source code for MSI and OPS index calculations.
* `submission.pdf`: Consolidated project report.

---
[cite_start]*Developed for the UIDAI Data Hackathon 2026.* [cite: 1]
