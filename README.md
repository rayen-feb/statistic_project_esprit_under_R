# 🏃 VO2 Estimation Project Using Multiple Linear Regression

![R](https://img.shields.io/badge/R-4.3-blue)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📌 Project Overview

This project aims to **predict health-related physical fitness (VO2, ml/kg/min)** in adults using easy-to-measure variables such as age, BMI, body fat percentage, and muscular fitness indicators. The analysis uses **R programming** and includes data cleaning, exploratory analysis, outlier treatment, scaling, correlation checks, and multiple linear regression modeling.

---

## 🎯 Objectives

- Explore and preprocess adult fitness data  
- Detect and treat outliers using **boxplots**  
- Standardize numeric variables using **Min-Max scaling** and **Standardization**  
- Analyze correlations and remove highly correlated predictors  
- Build a **multiple linear regression model** to predict VO2  
- Assess model assumptions:  
  - Normality of residuals  
  - Homoscedasticity  
  - Multicollinearity (VIF)  
- Interpret results and identify key predictors of VO2  

---

## 📊 Dataset

| Variable | Description |
|----------|-------------|
| `participant_id` | Participant identifier |
| `sex` | Gender (M/F) |
| `age` | Age in years |
| `bmi` | Body Mass Index |
| `percent_body_fat` | Body fat percentage |
| `hand_grip_strength_kg` | Muscular strength (kg) |
| `sit_and_reach_cm` | Flexibility (cm) |
| `sit_ups_count` | Muscular endurance |
| `vo2_estimate_ml_per_kg_min` | Estimated aerobic capacity (dependent variable) |

- **Number of participants:** 2000

---

## 🛠 Methodology

1. **Data Cleaning**  
   - Checked for missing values  
   - Detected and treated outliers using boxplots  

2. **Data Transformation**  
   - Standardization and Min-Max scaling applied to numeric variables  
   - Normality checked using **Shapiro-Wilk test**  

3. **Exploratory Analysis**  
   - Correlation analysis and removal of highly correlated predictors  
   - Multicollinearity checked with **Variance Inflation Factor (VIF)**  

4. **Modeling**  
   - Multiple Linear Regression using `lm()`  
   - Dependent variable: `vo2_estimate_ml_per_kg_min`  
   - Predictors: age, BMI, percent body fat, hand grip strength, sit-and-reach, sit-ups count  

5. **Diagnostics**  
   - Normality of residuals: Shapiro-Wilk test & Q-Q plots  
   - Homoscedasticity: residuals vs fitted values plot  
   - Multicollinearity: VIF < 2  

---

## 💻 R Code Highlights

```r
# Build multiple linear regression model
model <- lm(vo2_estimate_ml_per_kg_min ~ age + bmi + percent_body_fat + 
            hand_grip_strength_kg + sit_and_reach_cm + sit_ups_count, 
            data = data_reg_scaled)

# Model summary
summary(model)

# Check multicollinearity
library(car)
vif(model)

# Residual diagnostics
shapiro.test(resid(model))
plot(fitted(model), resid(model))
```
---
### 📈 Key Results

Significant predictors of VO2: age, percent body fat, hand grip strength

Sit-and-reach and sit-ups count were not significant

Model explains ~24% of variance in VO2 (Adjusted R² = 0.2387)

ANOVA confirms overall model significance (p < 0.001)

### ⚡ Conclusions

VO2 is strongly influenced by age, body fat, and muscular strength

Simple fitness tests can predict aerobic capacity effectively

Methodology can be applied to other populations for VO2 estimation

### 🔧 Dependencies

R (>= 4.0)

Packages: dplyr, car, ggplot2, scales

### 🔮 Future Work

Explore non-linear models or machine learning algorithms for better prediction

Include additional predictors (e.g., lifestyle, physical activity)

Conduct cross-validation to assess model generalizability



