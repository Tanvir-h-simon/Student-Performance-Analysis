# Dataset Information

## Student Performance Factors Dataset

### Overview
This dataset contains information about student performance and various factors that may influence exam scores.

### Source
- **Filename:** StudentPerformanceFactors.csv
- **Location:** `data/raw/StudentPerformanceFactors.csv`

### Dataset Characteristics
- **Total Records:** 6,607 (original)
- **Records After Cleaning:** ~6,604
- **Total Features:** 20 (7 numerical, 13 categorical)
- **Target Variable:** Exam_Score (continuous, 0-100)

### Features Description

#### Numerical Features (7):
1. **Hours_Studied** - Total hours student spent studying per week (1-44 hours)
2. **Attendance** - Student's attendance percentage (60-100%)
3. **Sleep_Hours** - Average sleep hours per night (4-10 hours)
4. **Previous_Scores** - Student's scores in previous exams (50-100)
5. **Tutoring_Sessions** - Number of tutoring sessions attended per month (0-8)
6. **Physical_Activity** - Hours of physical activity per week (0-6 hours)
7. **Exam_Score** - **TARGET VARIABLE** - Final exam score (0-100)

#### Categorical Features (13):
1. **Parental_Involvement** - Level of parental involvement (Low, Medium, High)
2. **Access_to_Resources** - Availability of learning resources (Low, Medium, High)
3. **Extracurricular_Activities** - Participation in activities (Yes, No)
4. **Motivation_Level** - Student's motivation level (Low, Medium, High)
5. **Internet_Access** - Access to internet (Yes, No)
6. **Family_Income** - Family income level (Low, Medium, High)
7. **Teacher_Quality** - Quality of teaching received (Low, Medium, High, Unknown)
8. **School_Type** - Type of school attended (Public, Private)
9. **Peer_Influence** - Influence of peers on performance (Positive, Neutral, Negative)
10. **Learning_Disabilities** - Presence of learning disabilities (Yes, No)
11. **Parental_Education_Level** - Parents' education (High School, College, Postgraduate, Unknown)
12. **Distance_from_Home** - Distance from home to school (Near, Moderate, Far)
13. **Gender** - Student's gender (Male, Female)

### Data Quality Issues (Addressed in Cleaning)
- **Missing Values:**
  - Teacher_Quality: Filled with 'Unknown'
  - Parental_Education_Level: Filled with 'Unknown'
  - Distance_from_Home: Filled with mode
  
- **Anomalies Removed:**
  - Records with Exam_Score > 100 (impossible values)
  - Students with extremely low study hours + high scores + low previous scores (data errors)
  - Total removed: ~3 records

### Statistical Summary
- **Exam Score Mean:** ~67.24
- **Exam Score Std Dev:** ~7.89
- **Exam Score Range:** 50-100 (after cleaning)

### Key Correlations with Exam Score
1. **Previous_Scores:** r = 0.989 (Strongest predictor)
2. **Hours_Studied:** r = 0.408 (Moderate positive)
3. **Attendance:** r = 0.409 (Moderate positive)
4. **Motivation_Level:** High motivation → ~10-15 points increase

## Processed Data
- **Location:** `data/processed/` (optional)
- Cleaned datasets with outliers removed and missing values handled can be saved here for future use.

## Usage Notes
- Always use relative paths when loading data: `../data/raw/StudentPerformanceFactors.csv`
- Original dataset is preserved in `raw/` folder
- Processed/cleaned versions should be saved in `processed/` folder

## Citation
This dataset is used for educational purposes in the WIA1007 Data Science course project.
