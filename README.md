# Predictive Maintenance in High-Performance Engineering ⚙️📊

## Overview
This project bridges the gap between data science and automotive mechatronics. It features a Machine Learning pipeline designed to analyze real-time sensor telemetry and predict catastrophic mechanical failures before they occur. 

Rather than relying on reactive maintenance, this model identifies the critical physical thresholds where high thermal and mechanical stress lead to hardware failure.

## Engineering Context
In high-performance environments—such as managing the thermal limits of a high-revving internal combustion engine—mechanical failure is rarely instantaneous. It is preceded by specific patterns in operational load. 

By analyzing variables like **Rotational Speed (RPM)**, **Torque (Nm)**, and **Process Temperatures**, this project simulates the logic required for an active safety net. If integrated into an Engine Control Unit (ECU), this algorithmic approach could automatically cut ignition or reduce boost pressure the millisecond the telemetry enters a known failure cluster.

## Technical Workflow
1. **Exploratory Data Analysis (EDA):** Mapping the operational boundaries and identifying physical correlations (e.g., the inverse relationship between RPM and Torque, and the clustering of failures at extreme power-band limits).
2. **Time Series Simulation:** Applying rolling averages to raw temperature data to filter out digital sensor noise and isolate true thermal trends.
3. **Data Preprocessing:** Standardizing multi-scale sensor data (`StandardScaler`) to ensure thermal and mechanical stresses are evaluated equally by the distance-based algorithm.
4. **Predictive Modeling:** - **PCA (Principal Component Analysis):** For dimensionality reduction and 2D visualization of standard vs. failure states.
   - **KNN (K-Nearest Neighbors):** Trained to classify incoming telemetry data and flag high-risk operational states based on historical failure proximity.

## Key Findings
* **Failure Zones:** Failures consistently cluster at the extremes of the torque curve (e.g., maximum torque at sub-optimal RPMs) and during severe thermal overload.
* **Algorithmic Proximity:** The KNN model successfully distinguishes between safe operation and impending mechanical failure, proving that real-time stress monitoring is a viable method for preventing hardware destruction.

## Technologies Used
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn
* **Algorithms:** K-Nearest Neighbors (KNN), Principal Component Analysis (PCA)

---
*This project was developed to demonstrate the application of predictive data analytics to physical mechanical systems.*
