# UIDAI Data Hackathon 2026: Tempo-Spatial Analysis of Aadhaar Activity

**Team Members:** Dheerajpreet Singh, Rishit Gakhar, Swastik Panda (IIT Roorkee)

## 📌 Project Overview
 This project addresses the uneven distribution of Aadhaar service usage across India[ : 10]. While some mature states face infrastructure stress due to high update volumes, remote districts remain underserved[ : 10]. Our approach moves beyond simple volume reporting to build data-driven indicators for fair access and system reliability[ : 13, 15].

## 🛠️ Methodology & Technical Stack
### Data Preprocessing
 We implemented a robust pipeline to handle significant data anomalies found in the initial datasets[ : 300, 311]:
* **Canonicalization:** Standardized misspelled state/district names and resolved historical boundary changes (e.g., Telangana-Andhra Pradesh split)[ : 212, 239, 277].
* **Anomaly Mitigation:** Identified "first-of-the-month" data concentration issues and utilized monthly aggregation to ensure statistical reliability[ : 356, 361].

### Feature Engineering
 We developed custom metrics to measure system performance and priority[ : 495]:
* **Maintenance Stress Index (MSI):** Measures the burden of update activity relative to new enrollments[ : 652].
* **Outreach Priority Score (OPS):** A population-adjusted score identifying high-impact zones for service expansion[ : 704].
* **Gini Coefficient Analysis:** Used to track Aadhaar access inequality over time, showing a drop in per-capita inequality from ~0.93 to ~0.50[ : 464, 468].

### Clustering
 Using **K-Means Clustering** ($k=5$ for districts; $k=3$ for states), we segmented regions into distinct maturity profiles[ : 779, 788, 789]:
1. **High-Pressure Mature Systems:** Very high biometric load (e.g., UP, Maharashtra)[ : 835].
2. **Education-Driven Systems:** Teen-dominated enrollment structures[ : 829].
3. **Low-Digitization Rural:** High priority for mobile enrollment centers[ : 861].

## 📊 Key Insights
* **Service Dominance:** Biometric updates dominate total activity (~68M) compared to demographic updates (~36M) and enrollments (~5M)[ : 434, 450, 447].
* **Temporal Patterns:** Activity peaks midweek and drops sharply on weekends, indicating office-driven operational patterns[ : 429].
* **Concentration:** The top 30% of states account for 70-75% of total Aadhaar activity[ : 490].

## 🚀 Recommendations
* **Infrastructure Scaling:** Automate processes in "Cluster 0" high-pressure zones to reduce maintenance stress[ : 861].
* **Targeted Outreach:** Deploy mobile units specifically to high-OPS states like **Meghalaya**[ : 667, 861].
* **School Integration:** Plan for peak periods by integrating Aadhaar updates directly with educational cycles for the 5-17 age group[ : 861].

## 📂 Repository Structure
* `/data`: Preprocessing scripts for cleaning and state-split corrections.
* `/notebooks`: EDA, Lorenz Curve generation, and K-Means implementation.
* `/src`: Source code for MSI and OPS index calculations.
* `submission.pdf`: Consolidated project report.

---
 *Developed for the UIDAI Data Hackathon 2026.* [ : 1]
