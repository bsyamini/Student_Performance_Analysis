# Student_Performance_Report
# Student Performance Analysis – Mathematics & Portuguese

## Project Overview

This project analyzes student academic performance in Mathematics and Portuguese to identify the key factors influencing final grades (G3) and pass/fail outcomes.

The objective is to:
- Identify statistically significant predictors of academic success
- Quantify the impact of demographic, academic, and lifestyle variables
- Build predictive models for final grades and passing probability
- Translate statistical findings into actionable insights

---

## Problem Statement

Student performance is influenced by multiple background, academic, and behavioral factors. However, it is unclear:

- Which factors significantly impact final grades
- Whether lifestyle variables meaningfully affect performance
- What best predicts whether a student will pass or fail

This project answers:

> Which background, family, lifestyle, and academic behavior factors significantly influence students’ final academic performance (G3)?

---

## Tools & Technologies Used

- Python  
- Pandas (Data Cleaning & Manipulation)  
- NumPy (Numerical Analysis)  
- Matplotlib / Seaborn / Plotly (Data Visualization)  
- Statistical Modeling  
  - Correlation Analysis  
  - One-Way ANOVA  
  - Multiple Linear Regression  
  - Logistic Regression  

---

## Project Structure

```
student-performance-analysis/
│
├── data/
│   ├── raw/
│   │   └── student_data.csv
│   │
│   └── processed/
│       └── cleaned_student_data.csv
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_exploratory_data_analysis.ipynb
│   ├── 03_statistical_analysis.ipynb
│   └── 04_regression_models.ipynb
│
├── src/
│   ├── data_preprocessing.py
│   ├── eda.py
│   ├── statistical_tests.py
│   └── modeling.py
│
├── visuals/
│   ├── correlation_heatmap.png
│   ├── subject_comparison.png
│   ├── regression_results.png
│   └── model_performance.png
│
├── reports/
│   ├── Student_Performance_Report.pdf
│   └── Presentation_Slides.pptx
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Dataset Overview

The dataset includes:

- Demographics (Gender, Internet Access, Higher Education Intention)
- Academic History (G1, G2, G3, Previous Failures)
- Behavioral Variables (Study Time, Absences)
- Lifestyle Variables (Workday & Weekend Alcohol Consumption)
- Course Subject (Mathematics or Portuguese)

---

## Exploratory Data Analysis (EDA)

Key descriptive findings:

- 56.6% Female | 43.4% Male
- 37.8% Mathematics | 62.2% Portuguese
- 91.5% plan to pursue higher education
- 79.2% have internet access
- Average final grade: 11.26
- Average absences: 4.43
- Average study time: ~2 hours

### Subject Comparison
- Students performed significantly better in Portuguese than Mathematics.
- Students studied slightly more for Mathematics despite lower performance.

---

## Statistical Analysis

### Correlation Analysis
- Strong positive correlation between G2 and G3
- Positive correlation between G1 and G3
- Weak negative relationship between absences and final grades
- Minor negative relationship with alcohol consumption

---

### One-Way ANOVA

Tested impact of:
- Study Time
- Workday Alcohol
- Weekend Alcohol

Findings:
- Statistically significant differences were observed.
- Effect sizes were small (1–3% variance explained).
- Lifestyle factors have limited practical impact compared to academic history.

---

### Multiple Linear Regression (Predicting Final Grade – G3)

Model Performance:
- R² = 0.842
- Explains 84.2% of variation in final grades.

Strongest Predictors:
- G2 (Second Period Grade)
- G1 (First Period Grade)
- Previous Academic Failures
- Course Subject

Not Significant After Controlling:
- Study Time
- Alcohol Consumption
- Parental Education
- Social Activities

Conclusion:
Academic history is the strongest determinant of final performance.

---

### Logistic Regression (Predicting Pass/Fail)

Model Performance:
- Accuracy: 80.7%
- Nagelkerke R² = 0.222

Significant Predictors:
- Study time increases likelihood of passing
- Previous failures significantly reduce passing odds
- Course subject influences pass probability

The model predicts passing well but is weaker at detecting failing students.

---

## Key Insights

- Past academic performance is the strongest predictor of future performance.
- Study time increases pass probability but has limited impact on grade variance.
- Alcohol consumption shows statistical significance but small practical influence.
- Subject type impacts performance outcomes.
- Academic tracking and early intervention are critical.

---

## Statistical Terms Explained

| Term | Meaning |
|------|----------|
| p-value | Indicates whether a result is statistically significant |
| F-statistic | Tests whether differences between groups are meaningful |
| η² (Eta Squared) | Measures practical impact (effect size) |
| β (Beta Coefficient) | Strength and direction of influence in regression |
| OR (Odds Ratio) | Impact of a factor on pass probability |
| R² | Overall explanatory power of the model |

---

## Project Workflow

1. Data Cleaning & Preprocessing  
2. Exploratory Data Analysis  
3. Correlation Analysis  
4. ANOVA Testing  
5. Linear Regression Modeling  
6. Logistic Regression Modeling  
7. Model Evaluation & Interpretation  
8. Insight Generation  

---

## Future Improvements

- Feature engineering
- Advanced machine learning models (Random Forest, XGBoost)
- Improved failure detection performance
- Interactive dashboard deployment

---

## 👤 Author

https://www.linkedin.com/in/sri-yamini-bandaru-a68698284/
