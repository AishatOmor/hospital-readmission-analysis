# hospital-readmission-analysis
Excel-based healthcare analytics project focused on identifying factors influencing hospital readmission rates. Includes data cleaning, pivot table analysis, visualizations, and a what-if scenario model to evaluate the impact of reducing readmissions.

# Excel Readmission Analysis
Project Overview

This project analyzes hospital patient data to identify factors influencing hospital readmissions. The dataset includes patient demographics, medical procedures, lab tests, diagnoses, medication information, and readmission status.

Using Microsoft Excel, the project demonstrates:

Data cleaning and transformation

Exploratory analysis with pivot tables

Visualizations (bar charts, stacked bars, heatmaps)

Scenario modeling / What-If Analysis to estimate reductions in readmissions

This project highlights healthcare analytics, forecasting, and data-driven decision-making skills.

Dataset

The dataset used in this project is publicly available on Kaggle:
Hospital Readmissions Dataset – Dubradave https://www.kaggle.com/datasets/dubradave/hospital-readmissions

Note: The data is anonymized and used for educational and analytical purposes. No personal patient information is included.

The dataset contains anonymized hospital patient records. Each row represents a patient visit.

Column	Description
age	Patient age group ([50-60), [60-70), etc.)
time_in_hospital	Length of hospital stay (days)
n_lab_procedures	Number of laboratory procedures performed
n_procedures	Number of procedures performed during the visit
n_medications	Number of medications administered
n_outpatient	Outpatient visits in the prior year
n_inpatient	Inpatient visits in the prior year
n_emergency	ER visits in the prior year
medical_specialty	Treating physician specialty
diag_1, diag_2, diag_3	Diagnoses
glucose_test, A1Ctest	Test results (high/normal/not performed)
change	Whether medication was changed (yes/no)
diabetes_med	Whether diabetes medication was prescribed (yes/no)
readmitted	Whether the patient was readmitted (yes/no)
Methods
# 1. Data Cleaning

Standardized age groups

Converted categorical values to numeric flags where necessary (e.g., readmission_count)

Created calculated columns (e.g., total_procedures = n_lab_procedures + n_procedures, total visit = n_outpatient + n_inpatient + n_emergency)

# 2. Descriptive Statistics

Calculated summary statistics for key numeric columns:

time_in_hospital (length of stay)

n_lab_procedures (number of lab tests)

Metrics included:

Mean, Median, Minimum, Maximum

Standard Deviation

Count / Distribution

Helps identify typical hospital stays, variation in lab testing, and outliers for further analysis

# 3. Exploratory Analysis

Pivot tables to explore:

Readmissions by diagnosis
<img width="1084" height="455" alt="image" src="https://github.com/user-attachments/assets/34b89b58-c5a3-4fca-8c3e-83c349305667" />


Average length of stay by age group <img width="609" height="656" alt="image" src="https://github.com/user-attachments/assets/ba8ceef4-ecf7-4bca-a444-702c11c9d03d" />


Medication counts by medical specialty <img width="414" height="270" alt="image" src="https://github.com/user-attachments/assets/98e23c1e-4b48-4d03-8922-1285aca59502" />


Impact of medication changes on readmissions <img width="681" height="638" alt="image" src="https://github.com/user-attachments/assets/f7e38637-6e2b-4aef-b3d7-8d53fab73408" />


# 4. Visualizations

Bar charts for top diagnoses with highest readmissions 

Stacked bar charts by age group and readmission

Heatmap: readmissions by age and medical specialty

# 5. Scenario Modeling (What-If Analysis)

Simulated reductions in readmissions using Data Tables

Example reduction factors:

Reduction Factor	Reduction %
1.00	basline
0.95	5%
0.85	15%
0.90	10%

Formula: Adjusted_Readmission = Readmission_Flag × Reduction_Factor

Shows potential improvements in patient outcomes and reduced readmission. 

# 6. Key insights
## 1. Readmissions by Diagnosis

Patients with Circulatory, Respiratory, and “Other” diagnoses have the highest readmission rates.

Targeted interventions for these groups could reduce hospital readmissions and improve patient outcomes.

## 2. Average Hospital Stay by Age Group

Older patients tend to stay slightly longer in the hospital.

Patients who were readmitted generally had longer hospital stays, suggesting a potential correlation between length of stay and readmission risk.

## 3. Medication Counts by Physician Specialty

Surgery prescribes the highest average number of medications per patient.

Emergency/Trauma and Family Practice prescribe fewer medications on average.

Understanding prescription patterns can help standardize care and manage medication-related readmission risk.

## 4. Effect of Medication Changes on Readmissions

Patients who had their diabetes medication changed and were prescribed a diabetes med have the highest readmissions.

Careful monitoring and personalized medication adjustments could potentially lower readmission rates.

## 5. Scenario Modeling / What-If Analysis

Reducing readmission rates through intervention strategies (e.g., medication management) can be quantified using reduction factors.

Example: A 5% reduction factor decreases expected readmissions slightly, while larger reduction factors (42% or 75%) demonstrate the potential for significant improvement.

Scenario modeling highlights the impact of strategic decisions on patient outcomes and hospital efficiency.
