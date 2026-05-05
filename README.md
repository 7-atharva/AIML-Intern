Based on the Exploratory Data Analysis (EDA) we've performed, here is the final summary of what we've learned from the machine manufacturing dataset:

1. Data Health & Preparation
The dataset of 10,000 machines was very clean, with no missing values or duplicates.
We streamlined the data by removing identifiers (UDI, Product ID) and focusing on physical metrics.
2. Key Predictive Insights
The Torque-Speed Relationship: There is a very strong inverse relationship (-0.88). When the machine spins faster, the torque drops. High torque is a major 'danger zone'.
Temperature Coupling: Air and Process temperatures move together closely (0.88), which is expected but confirms sensors are working correctly.
3. Understanding Machine Failure
Failure is Rare but Predictable: Only 3.39% of the machines failed.
Torque is a Critical Indicator: Our boxplots and anomaly detection showed that while normal machines run at 40 Nm, failures happen most often when torque becomes erratic or exceeds **60 Nm**.
The Power Factor: By creating the Power and Temp_Diff metrics, we found that failures like PWF (Power Failure) and OSF (Overstrain) are the most significant contributors to overall machine breakdown.
4. Anomalies
We identified 239 extreme operating instances. These aren't just 'odd data points'; they represent machines under high physical stress that are significantly more likely to fail than the rest of the fleet.
