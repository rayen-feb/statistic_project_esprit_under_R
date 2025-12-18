# 🧬 Health-Related Physical Fitness (HRPF) Estimation Project

![R](https://img.shields.io/badge/R-4.3-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Project Type](https://img.shields.io/badge/Project-Static-orange)
![Data](https://img.shields.io/badge/Dataset-2000%20participants-red)

---

## 📖 Project Type

This repository contains a **static data analysis project** focusing on estimating **VO2 (ml/kg/min)** in adults using multiple linear regression.  

It reproduces and interprets the methodology of a scientific study on **health-related physical fitness (HRPF)** using easy-to-measure anthropometric and fitness variables.  

**Reference Paper:**  
> Example: *"Estimating Health-Related Physical Fitness in Korean Adults Using Multiple Linear Regression,"* Journal of Exercise Science, 2021.

---

## 🎯 Project Goal

- Build a **multiple linear regression model** to predict VO2 from variables like:
  - Age
  - BMI
  - Percent Body Fat
  - Hand Grip Strength
  - Sit-and-Reach
  - Sit-ups Count
- Assess **gender differences** in fitness variables.
- Detect and handle **outliers**.
- Check assumptions: normality of residuals, homoscedasticity, multicollinearity.

---

## 📊 Exploratory Data Analysis & Visualizations

### 1. Distribution of VO2
![VO2 Histogram](plots/vo2_histogram.png)

### 2. Percent Body Fat vs VO2
![Body Fat vs VO2](plots/bodyfat_vo2_scatter.png)

### 3. Hand Grip Strength vs VO2
![Hand Grip vs VO2](plots/handgrip_vo2_scatter.png)

### 4. Correlation Matrix Heatmap
![Correlation Heatmap](plots/corr_heatmap.png)

### 5. Residual Diagnostics
- **Residuals vs Fitted Values**  
![Residuals Plot](plots/residuals_fitted.png)

- **Q-Q Plot of Residuals**  
![QQ Plot](plots/qq_residuals.png)

---

## 🧮 Statistical Methods & Analysis

1. **Data Preparation**
   - Handling missing values
   - Outlier detection using **boxplots**
   - Scaling numeric variables (Min-Max / Standardization)
   - Removing highly correlated variables (correlation > 0.8)

2. **Normality Tests**
   - Shapiro-Wilk test for all numeric variables
   - Transformation applied if necessary

3. **Multiple Linear Regression**
   - Formula:  
     ```
     VO2 ~ age + bmi + percent_body_fat + hand_grip_strength_kg + sit_and_reach_cm + sit_ups_count
     ```
   - **VIF** checked to ensure no multicollinearity
   - **Residual analysis** for normality & homoscedasticity

4. **Model Interpretation**
   - Significant predictors: `age`, `percent_body_fat`, `hand_grip_strength_kg`
   - Adjusted R²: 0.2387
   - F-statistic: p < 2.2e-16
   - Gender differences confirmed via t-tests

---

## 🔧 How to Run & Reproduce

1. Clone this repo:
```bash
git clone https://github.com/username/HRPF_VO2_Project.git
```
2.Install required packages:
install.packages(c("tidyverse", "ggplot2", "car"))
3.Load data & run analysis scripts:
source("analysis/data_preparation.R")
source("analysis/multi_linear_regression.R")
