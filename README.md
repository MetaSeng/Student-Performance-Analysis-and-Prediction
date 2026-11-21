# Student Performance Analysis and Prediction

This project analyzes student performance data to understand the factors influencing exam scores and builds a predictive model to estimate final scores.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset Description](#dataset-description)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Machine Learning Model](#machine-learning-model)
- [Key Results](#key-results)
- [Technologies Used](#technologies-used)

---

## Project Overview
The goal of this project is to identify the most significant factors that contribute to a student's final exam performance and leverage these factors to build a predictive Multiple Linear Regression model.

## Dataset Description
The dataset (`student_exam_scores.csv`) consists of 200 student records with 6 features:
- **`student_id`**: Unique identifier for each student.
- **`hours_studied`**: Number of hours spent studying.
- **`sleep_hours`**: Average daily hours of sleep.
- **`attendance_percent`**: Percentage of classes attended.
- **`previous_scores`**: Scores in previous exams (scale 0-100).
- **`exam_score`**: The target variable representing the final exam score.

## Exploratory Data Analysis (EDA)
- **Correlations**:
  - Study hours showed the strongest linear relationship with exam scores.
  - Previous scores showed a moderate positive correlation ($r \approx 0.43$).
  - Attendance rate showed a weak positive correlation ($r \approx 0.23$).
- A complete heatmap visualization is included in the notebook to show the exact linear relationships between all numerical features.

## Machine Learning Model
We trained a **Multiple Linear Regression** model using a 80/20 train-test split.

### Feature Importances (Model Coefficients)
- **`hours_studied`**: +1.55 increase in exam score per hour
- **`sleep_hours`**: +0.88 increase in exam score per hour
- **`attendance_percent`**: +0.11 increase in exam score per percentage point
- **`previous_scores`**: +0.18 increase in exam score per unit score

## Key Results
- **Root Mean Squared Error (RMSE)**: 2.79
- **R² Score**: 0.854 (The model explains approximately 85.4% of the variance in final exam scores).

## Technologies Used
- Python
- Pandas & NumPy (Data manipulation)
- Matplotlib & Seaborn (Data visualization)
- Scikit-learn (Machine Learning modeling)
