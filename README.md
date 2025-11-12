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
<img width="375" height="235" alt="image" src="https://github.com/user-attachments/assets/2f125a3c-7e8f-43bd-bb41-5bd3f371bf5d" />

Average length of stay by age group <img width="477" height="291" alt="image" src="https://github.com/user-attachments/assets/65a0bb72-bac8-4894-9638-d3e0dc02e69c" />

Medication counts by medical specialty <img width="376" height="261" alt="image" src="https://github.com/user-attachments/assets/e80862c0-f249-4392-96d0-20325b09e7b4" />

Impact of medication changes on readmissions <img width="519" height="248" alt="image" src="https://github.com/user-attachments/assets/436ec895-5031-4f57-abc3-d09d9d7d41e3" />

# 4. Visualizations

Bar charts for top diagnoses with highest readmissions <img width="659" height="357" alt="image" src="https://github.com/user-attachments/assets/3ddb0620-a817-43f3-a321-ecc14d256246" />

Stacked bar charts by age group and readmission <img width="690" height="380" alt="image" src="https://github.com/user-attachments/assets/2f17e491-f668-447e-91c5-cd9c5333374a" />

Heatmap: readmissions by age and medical specialty <img width="202" height="184" alt="image" src="https://github.com/user-attachments/assets/108af8a5-7c4c-46cd-9699-f20dbd83b387" />


# 5. Scenario Modeling (What-If Analysis)

Simulated reductions in readmissions using Data Tables

Example reduction factors:

Reduction Factor	Reduction %
1.00	basline
0.95	5%
0.85	15%
0.90	10% <img width="590" height="188" alt="image" src="https://github.com/user-attachments/assets/888f6030-b762-4228-bebc-ff9ff681faef" />

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
