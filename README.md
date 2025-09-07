# ☕ Coffee, Health & Stress Prediction

This project explores the relationship between **coffee consumption, health, lifestyle factors, and stress levels** using machine learning.  
We build models to predict whether an individual’s stress level is **Low, Medium, or High**, based on features such as caffeine intake, sleep duration, BMI, physical activity, and more.  

---

## 📖 Dataset Description

The dataset is synthetic but modeled after real-world patterns, containing **10,000 records from 20 countries**.  
It includes demographics, coffee intake, caffeine levels, sleep duration/quality, BMI, heart rate, physical activity, smoking, alcohol consumption, and health issues.  

For this project:
- We focus on **stress level prediction**.
- **Coffee_Intake** and **Caffeine_mg** are proportional, so only one feature was retained to avoid redundancy.

---

## 🧹 Data Preprocessing

1. **Handling Missing Values**  
   - No missing values in the dataset.  

2. **Feature Encoding**  
   - `Country` → One-hot encoding  
   - `Gender` and other categorical variables → Label encoding  

3. **Feature Selection**  
   - Dropped redundant features (kept only `Caffeine_mg` instead of both caffeine & coffee intake).  

4. **Class Imbalance**  
   - Stress levels were imbalanced:  
     - Low: 69.9%  
     - Medium: 20.5%  
     - High: 9.6%  
   - **SMOTE** was applied on the training set only to balance classes.

---

## 📊 Exploratory Data Analysis (EDA)

- Higher **caffeine intake** and **lower sleep duration** correlated with higher stress.  
- **BMI** and **physical activity** also influenced stress levels.  
- Country-wise variations were observed in average caffeine intake and stress levels.  

---

## 🤖 Modeling

We trained two machine learning models:

1. **Logistic Regression**  
   - Accuracy: **98%**  
   - Strength: Simple, interpretable, and strong performance.  

2. **Support Vector Machine (SVM)**  
   - Accuracy: **97%**  
   - Strength: Effective with non-linear relationships, slightly lower accuracy compared to Logistic Regression.  

---

## 📈 Evaluation

### Logistic Regression Results
- **Accuracy:** 98%  
- **Macro F1:** 0.97  
- Confusion matrix showed very few misclassifications.  

### Support Vector Machine (SVM) Results
- **Accuracy:** 97%  
- **Macro F1:** 0.95  
- Slightly higher misclassifications than Logistic Regression.  

**Comparison:**  
While Logistic Regression achieved slightly higher overall accuracy (98%) compared to SVM (97%), both models proved effective for predicting stress levels.

---

## ✅ Conclusion

Lifestyle factors such as **sleep hours, caffeine intake, BMI, and physical activity** show strong influence on stress levels.  

Both **Logistic Regression** and **SVM** provided high predictive performance, with Logistic Regression performing marginally better.  

This project demonstrates how machine learning can provide insights for **wellness apps** and **lifestyle management tools**, enabling stress detection and promoting healthier lifestyle choices.  
