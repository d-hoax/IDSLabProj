# Autonomous Vehicles Disengagement Reports Analysis

## Table of Contents
- [Project Structure](#project-structure)
- [Link To Repo](#link-to-repo)
- [Overview](#overview)
- [Data Source](#data-source)
- [Features and Visualizations](#features-and-visualizations)
- [Results and Conclusion](#results-and-conclusion)
- [Acknowledgments](#acknowledgements)
- [Requirements](#requirements)

---

## Project Structure
```bash
├── code
│   └── autonomous_disengagement_analysis.ipynb
├── data
│   ├── 2018-19_AutonomousVehicleDisengagementReports(firsttimefilers).csv
│   └── 2019AutonomousVehicleDisengagementReports.csv
├── README.md
└── figures
    └── poster
```

---

## Link to Repo:
https://github.com/d-hoax/IDSLabProj
---
--- 

## Overview
This project analyzes and visualizes disengagement reports from the California Department of Motor Vehicles (DMV) for self-driving cars tested from 2018 to 2019. The main goal is to understand where the technology still struggles, identify trends, and gain insights that can guide improvements in autonomous vehicle (AV) systems.

The accompanying poster, **“Autonomous Vehicles Disengagement Reports Analysis,”** highlights the major findings from the data, including:
- The progression of disengagements over time.
- The proportion of disengagements initiated by different actors (e.g., test driver vs. AV system).
- The common locations where disengagements occurred.
- Key words/phrases in the descriptions of disengagement causes (e.g., “software,” “weather,” “construction”).

By using Python libraries—**pandas**, **matplotlib**, **numpy**, and **seaborn**—we clean the data, reconcile inconsistent entries (e.g., “street (high speed)” vs. “street”), and generate a variety of visualizations to help interpret the findings.

---

## Data Source
The data for this analysis comes from Kaggle, specifically:
1. `2018-19_AutonomousVehicleDisengagementReports(firsttimefilers).csv`  
2. `2019AutonomousVehicleDisengagementReports.csv`

These two CSV files are combined into a single DataFrame to have a more comprehensive view of the disengagement reports for 2018 and 2019.

---

## Features and Visualizations
1. **Data Cleaning & Preparation**  
   - Inconsistent text values are standardized (e.g., “Safety Driver” → “test driver”).  
   - Date columns are converted to a consistent format.  
   - Unnecessary columns are renamed or dropped for improved readability.

2. **Descriptive Statistics**  
   - Number of unique manufacturers, vehicles, total reports, etc.  
   - Distribution of disengagements over time (quarterly).

3. **Pie & Bar Charts**  
   - **Disengagement Initiated By**: Pie chart showing the proportion of test-driver-initiated vs. AV-system-initiated disengagements.  
   - **Disengagement Location**: Bar chart of street, highway, rural roads, etc.  
   - **Disengagements by Manufacturer**: Bar chart comparing the frequency of disengagements across manufacturers.  
   - **Driver Present** vs. **Vehicle Capable of Operating Without a Driver**: Pie charts showing the availability of a human driver and the vehicle’s capability.

4. **Keyword Analysis**  
   - Counts of specific words in the “Description Of Facts Causing Disengagement” field.  
   - Focus on software/hardware, mapping, sensors, weather conditions, road conditions (traffic, construction), etc.

---

## Results and Conclusion 
1. **Overall Statistics**

	-	**Total Reports:** Demonstrates the scope of the dataset.
	-	**Unique Manufacturers:** Reflects how many different companies are actively testing autonomous vehicles and reporting disengagements.
	-	**Unique Vehicles:** Shows how many distinct vehicles are being tested.
	-	**Unique Permits:** Indicates how many permits were granted for testing autonomous vehicles.

With the combined dataset, we expect hundreds to thousands of reported disengagements, spread across various companies and vehicle models.

2. **Disengagement Frequency Over Time**

	-	**Quarterly Trend:** The code resamples disengagements on a quarterly basis.
        -	This helps reveal whether disengagements are increasing or decreasing over time.
        -	A rising trend could mean more vehicles are being tested or more stringent reporting.
        -	A declining trend might indicate technology improvements or changes in test conditions.

3. **Disengagement Initiated By**

	-	**Test Driver vs. AV System:**
        -	A higher percentage of disengagements initiated by the test driver often suggests the driver’s caution in uncertain or problematic scenarios.
        -	A larger share of system-initiated disengagements might signal robust software detecting conditions it can’t handle.

4. **Disengagement Location**

	-	**Urban Streets, Rural Roads, Parking Facilities, Highways:**
        -	Comparing these categories can highlight the most challenging or frequently tested environments.
        -	For instance, if “street” dominates, it may indicate complex urban scenarios lead to more frequent takeovers.

5. **Disengagements by Manufacturer**

	-	**Manufacturer Comparison:**
        -	The bar chart shows which manufacturers have the highest number of disengagements.
        -	High disengagement counts may simply mean a company has more vehicles and more testing hours on the road.
        -	Low counts could mean fewer overall tests or advanced technology requiring fewer interventions.

6. Driver Presence & Vehicle Capability

	-	**Driver Present:**
        -	Most tests often have a safety driver physically present to intervene.
        -	A low share of driver-present tests might mean the company is focusing on driverless (Level 4 or 5) trials.
	-	**Vehicle Capable of Operating Without a Driver:**
        -	Identifies how many vehicles are technically equipped for fully autonomous operation.
        -	A larger “unknown” segment sometimes indicates incomplete or unreported data.

7. **Keyword Analysis of Disengagement Causes**

    -   **Software vs. Hardware:**
        - Software-based issues (e.g., planning, perception) tend to occur more often than outright hardware failures. This might direct future R&D efforts.
	-   **Sensor Technology:**
	    -	Keywords like lidar, radar, camera, and sensor appear frequently, suggesting that sensor or perception issues are common triggers for disengagement.
	-	**Environmental Factors:**
	    -	Mentions of traffic, weather, construction, and intersection indicate complex or unpredictable road conditions that necessitate manual override.
	-	**Map, GPS, Localization:**
	    -	These terms highlight how critical up-to-date, accurate mapping and localization data are for safe autonomy.

**Key Takeaways:** 
- **Most Disengagements** are initiated by the test driver rather than the AV system, indicating that human intervention is still critical.
- **Increasing Disengagements:** As more vehicles are tested, the number of disengagements reported also grows.
- **External Factors:** Adverse weather, traffic, and construction zones frequently appear in disengagement triggers.
- **Software vs. Hardware:** Software-related issues (trajectory planning, perception, etc.) appear more frequently than hardware failures.
- **Varied Performance Among Manufacturers:** While some companies report high disengagement counts (often due to extensive testing), others may report fewer due to limited test miles or better software maturity.


--- 

## Acknowledgements
- **University of Delaware Information and Decision Science Laboratory** for supporting the associated research.
- Mentors: **Logan Beaver**, **Behdad Chalaki**, **Heeseung Bang**, and **Professor Andreas A. Malikopoulos** at the University of Delaware.

--- 


## Requirements
- Python 3.x
- NumPy
- pandas
- matplotlib
- seaborn

You can install these requirements using:
```bash
pip install numpy pandas matplotlib seaborn
