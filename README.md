# 🏃 VO2 Estimation Project Using Multiple Linear Regression

![R](https://img.shields.io/badge/R-4.3-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Data](https://img.shields.io/badge/Dataset-2000%20participants-orange)
![Model](https://img.shields.io/badge/Model-Multiple%20Linear%20Regression-red)

---

## 📌 Project Overview

This project predicts **VO2 (ml/kg/min)** in adults using **easy-to-measure fitness variables**. The workflow includes:

- Data cleaning & outlier treatment 🧹  
- Data transformation & scaling 📊  
- Correlation analysis & multicollinearity check 🔍  
- Multiple linear regression modeling 🧮  
- Residual diagnostics & model evaluation 📈  

---

## 🎯 Objectives

- Identify key predictors of VO2  
- Apply **statistical tests** and regression in R  
- Assess model assumptions: normality, homoscedasticity, multicollinearity  
- Provide insights for fitness assessment and health monitoring  

---

## 🗂 Dataset

| Variable | Description |
|----------|-------------|
| `participant_id` | Unique participant ID |
| `sex` | Gender (M/F) |
| `age` | Age in years |
| `bmi` | Body Mass Index |
| `percent_body_fat` | Body fat percentage |
| `hand_grip_strength_kg` | Muscular strength (kg) |
| `sit_and_reach_cm` | Flexibility (cm) |
| `sit_ups_count` | Muscular endurance |
| `vo2_estimate_ml_per_kg_min` | Estimated aerobic capacity |

**Participants:** 2000 adults  

---

## 🛠 Methodology

1. **Data Cleaning** 🧹  
   - Outliers detected & treated with boxplots  

2. **Data Transformation** 🔄  
   - Standardization & Min-Max scaling  
   - Normality check using Shapiro-Wilk test  

3. **Exploratory Analysis** 🔍  
   - Correlation matrix analysis  
   - Remove highly correlated predictors  
   - VIF check for multicollinearity  

4. **Modeling** 🧮  
   - Multiple Linear Regression using `lm()`  
   - Dependent variable: `vo2_estimate_ml_per_kg_min`  
   - Independent variables: `age`, `bmi`, `percent_body_fat`, `hand_grip_strength_kg`, `sit_and_reach_cm`, `sit_ups_count`  

5. **Diagnostics & Evaluation** 📈  
   - Residual normality & Q-Q plots  
   - Homoscedasticity: residuals vs fitted values  
   - VIF < 2 → no significant multicollinearity  

---

## 💻 R Code Highlights

```r
# Build the model
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
plot(fitted(model), resid(model), xlab="Fitted Values", ylab="Residuals")
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



