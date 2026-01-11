# Student Performance Analysis - Data Science Project

## Overview
This project analyzes factors influencing student exam performance using machine learning techniques. The analysis explores the relationship between various factors (study habits, socioeconomic background, support systems) and exam scores, then builds predictive models to identify at-risk students.

## Research Questions
1. **Which factors most significantly influence exam performance?**
2. **What is the relative importance of controllable vs. uncontrollable factors?**
3. **Can we build a predictive model to identify at-risk students early?**
4. **Are there unexpected patterns or anomalies in student performance?**

## Project Structure
```
Data-Science-Student-Performance/
├── README.md                          # This file
├── requirements.txt                   # Python dependencies
├── .gitignore                        # Files to exclude from Git
│
├── data/
│   ├── raw/
│   │   └── StudentPerformanceFactors.csv      # Original dataset
│   ├── processed/                    # Cleaned data (generated)
│   └── README.md                     # Data description & source
│
├── notebooks/
│   └── Student_performance_factors.ipynb      # Complete analysis notebook
│
├── models/                           # Saved trained models (generated)
│   └── best_model.pkl
│
├── reports/
│   └── figures/                      # Visualizations (generated)
│
├── results/                          # Model metrics & predictions (generated)
│
└── docs/                             # Additional documentation
```

## Dataset
- **Source:** StudentPerformanceFactors.csv
- **Size:** 6,607 records (6,604 after cleaning)
- **Features:** 20 original features (7 numerical, 13 categorical)
- **Target Variable:** Exam_Score (0-100)

### Key Features:
- **Numerical:** Hours_Studied, Attendance, Previous_Scores, Sleep_Hours, Tutoring_Sessions, Physical_Activity
- **Categorical:** Parental_Involvement, Access_to_Resources, Motivation_Level, Family_Income, Teacher_Quality, School_Type, Gender, etc.

## Methodology
1. **Data Collection & Inspection** - Load and explore dataset structure
2. **Data Cleaning** - Handle missing values, remove anomalies
3. **Exploratory Data Analysis (EDA)**
   - Univariate analysis with statistical tests (Shapiro-Wilk, skewness, kurtosis)
   - Bivariate analysis (correlation, scatter plots, box plots)
   - Outlier detection using IQR method
4. **Feature Engineering** - Create 7 new features (Study_Efficiency, Support_Score, etc.)
5. **Model Training** - Train 3 models: Linear Regression, Decision Tree, Neural Network
6. **Model Evaluation** - Compare models using R², RMSE, MAE metrics

## Key Findings
- **Best Model:** Decision Tree (R² = ~0.98, RMSE = ~1.5 points)
- **Top Predictors:** Previous_Scores, Hours_Studied, Attendance, Motivation_Level, Parental_Involvement
- **Controllable factors** (study hours, attendance) have stronger impact than uncontrollable factors (family income, distance)
- **High motivation** adds ~10-15 points to exam scores on average

## Setup Instructions

### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook or JupyterLab

### Installation
1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd Data-Science-Student-Performance
   ```

2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

4. Open `notebooks/Student_performance_factors.ipynb` and run all cells

## Usage
1. **Explore the Data:** Run cells in `Student_performance_factors.ipynb` sequentially
2. **View Visualizations:** All plots are generated inline in the notebook
3. **Model Training:** Models are trained automatically when running the notebook
4. **Make Predictions:** Use the trained models to predict exam scores for new students

## Results
- **Model Performance:**
  - Linear Regression: R² ≈ 0.80
  - Decision Tree: R² ≈ 0.98 (Best)
  - Neural Network: R² ≈ 0.85
  
- **Feature Importance:** Previous_Scores > Hours_Studied > Attendance > Motivation_Level

## Technologies Used
- **Python 3.x**
- **Data Analysis:** pandas, numpy
- **Visualization:** matplotlib, seaborn
- **Statistical Tests:** scipy.stats
- **Machine Learning:** scikit-learn (LinearRegression, DecisionTreeRegressor, MLPRegressor)

## Project Status
✅ Complete - Ready for submission

## Author
WIA1007 Data Science Course Project

## License
This project is for educational purposes only.
