# Synthetic MedHealth Analysis

This project analyzes healthcare data to uncover trends, patterns, and insights. The dataset includes information on patients, medical conditions, billing, and healthcare providers. The analysis uses Python and various libraries to explore, preprocess, and visualize data for actionable insights.

## Dataset
The dataset is retrieved from [Kaggle](https://kaggle.com/datasets/prasad22/healthcare-dataset?resource=download). It contains information such as:
Each column provides specific information about the patient, their admission, and the healthcare services provided, making this dataset suitable for various data analysis and modeling tasks in the healthcare domain. Here's a brief explanation of each column in the dataset -

## Column Descriptions

### Name
This column represents the name of the patient associated with the healthcare record.

### Age
The age of the patient at the time of admission, expressed in years.

### Gender
Indicates the gender of the patient, either `"Male"` or `"Female"`.

### Blood Type
The patient's blood type, which can be one of the common blood types (e.g., `"A+"`, `"O-"`, etc.).

### Medical Condition
This column specifies the primary medical condition or diagnosis associated with the patient, such as `"Diabetes"`, `"Hypertension"`, `"Asthma"`, and more.

### Date of Admission
The date on which the patient was admitted to the healthcare facility.

### Doctor
The name of the doctor responsible for the patient's care during their admission.

### Hospital
Identifies the healthcare facility or hospital where the patient was admitted.

### Insurance Provider
This column indicates the patient's insurance provider, which can be one of several options, including `"Aetna"`, `"Blue Cross"`, `"Cigna"`, `"UnitedHealthcare"`, and `"Medicare"`.

### Billing Amount
The amount of money billed for the patient's healthcare services during their admission. This is expressed as a floating-point number.

### Room Number
The room number where the patient was accommodated during their admission.

### Admission Type
Specifies the type of admission, which can be `"Emergency"`, `"Elective"`, or `"Urgent"`, reflecting the circumstances of the admission.

### Discharge Date
The date on which the patient was discharged from the healthcare facility, based on the admission date and a random number of days within a realistic range.

### Medication
Identifies a medication prescribed or administered to the patient during their admission. Examples include `"Aspirin"`, `"Ibuprofen"`, `"Penicillin"`, `"Paracetamol"`, and `"Lipitor"`.

### Test Results
Describes the results of a medical test conducted during the patient's admission. Possible values include `"Normal"`, `"Abnormal"`, or `"Inconclusive"`, indicating the outcome of the test.

## Features
- Data preprocessing:
  - Handled missing and inconsistent data.
  - Standardized columns and calculated new features (e.g., billing per day).

- Data visualization:
  - Total billing by age group, gender, and medical condition.
  - Correlation analysis to uncover relationships between variables.

## Insights

### 1. Age Group Distribution
- The dataset is skewed toward patients aged **17-86**, with smaller data coverage for those aged 14-16 and above 86.
- **Seniors** represent the largest group, contributing significantly to total billing amounts, while **children** form the smallest group. 
- The distributions for **youth, middle-aged, and adults** are balanced, with no significant deviations.

---

### 2. Billing Amount Trends
- The maximum single invoice amount is **$52,764.28**, with most billing amounts per day below **$10,000**.
- Billing trends suggest that while high-cost cases exist, they are rare, and most invoices fall within reasonable bounds.
- The correlation heatmap highlights:
  - A **moderate positive correlation** between **billing amount** and **billing per day** (\( r = 0.32 \)).
  - A **strong negative correlation** between **billing per day** and **admission duration** (\( r = -0.54 \)). 
  - This indicates that longer stays generally reduce daily costs, likely due to reduced treatment intensity or discounts.

---

### 3. Admission Type Analysis
- Gender has little influence on the type of admission, with men showing slightly higher emergency admissions.
- There is no significant difference in billing amounts across different admission types, indicating balanced treatment costs.
- Admissions do not appear to be seasonal, with no observable patterns such as reduced admissions during COVID-19 lockdowns.

---

### 4. Medical Condition Trends
- Total billing amounts are similar across different diseases, suggesting no single condition dominates healthcare costs.
- For most conditions, billing amounts for males and females are nearly equal, highlighting equitable treatment costs across genders.

---

### 5. Healthcare Provider and Insurance Observations
- **Cigna** has the highest number of patients in the dataset, while **Aetna** has the least.
- Billing amounts are evenly distributed across healthcare providers, with no provider dominating the total billing.
- Each provider contributes similarly across diseases, reflecting balanced healthcare coverage.

---

### 6. Doctor-Level Insights
- **Dr. Michael Smith** is the most expensive doctor, with billing amounts approximately **22.2% higher** than the second most expensive doctor.
- This could reflect specialization or higher treatment complexity.

---

### 7. Dataset Balance
- The dataset shows strong balance in multiple dimensions:
  - Gender distribution is perfectly balanced at **50% male and 50% female**.
  - Age group distributions are proportional, except for the outliers (children and seniors).
  - Admissions are evenly distributed among **elective, urgent, and emergency types**.
  - Insurance providers and diseases contribute similar total billing amounts, suggesting no systemic bias.

---

## Conclusion
The dataset reflects a balanced healthcare environment with proportional representation across genders, age groups, medical conditions, and providers. 

- While seniors and chronic conditions such as **diabetes** contribute more to total costs, these patterns align with real-world healthcare trends.
- The even distribution of billing amounts and admission types supports the reliability and generalizability of this dataset for further analysis or predictive modeling.





