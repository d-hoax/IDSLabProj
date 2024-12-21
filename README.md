# Autonomous Vehicles Disengagement Reports Analysis
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
1. **Key Takeaways:** 
    - **Most Disengagements** are initiated by the test driver rather than the AV system, indicating that human intervention is still critical.
    - **Increasing Disengagements:** As more vehicles are tested, the number of disengagements reported also grows.
    - **External Factors:** Adverse weather, traffic, and construction zones frequently appear in disengagement triggers.
    - **Software vs. Hardware:** Software-related issues (trajectory planning, perception, etc.) appear more frequently than hardware failures.

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
