# 🫀 Heart Disease Prediction

This project applies **Logistic Regression** to predict the likelihood of heart disease based on patient health data.  
It uses the [Heart Disease UCI Dataset](https://raw.githubusercontent.com/kb22/Heart-Disease-Prediction/refs/heads/master/dataset.csv) and performs **exploratory data analysis (EDA)**, feature understanding, and model evaluation.

---

## 📂 Dataset Information

**Source:** [Kaggle / GitHub Dataset](https://github.com/kb22/Heart-Disease-Prediction)  
**Rows:** 303  
**Columns:** 14  

### Data Dictionary

| Column      | Description |
|-------------|-------------|
| **age**     | Age of the patient (in years) |
| **sex**     | Sex of the patient (1 = Male, 0 = Female) |
| **cp**      | Chest pain type (0 = Typical Angina, 1 = Atypical Angina, 2 = Non-Anginal Pain, 3 = Asymptomatic) |
| **trestbps**| Resting blood pressure (in mm Hg) |
| **chol**    | Serum cholesterol level (in mg/dL) |
| **fbs**     | Fasting blood sugar > 120 mg/dL (1 = True, 0 = False) |
| **restecg** | Resting ECG results (0 = Normal, 1 = ST-T wave abnormality, 2 = LV hypertrophy) |
| **thalach** | Maximum heart rate achieved |
| **exang**   | Exercise-induced angina (1 = Yes, 0 = No) |
| **oldpeak** | ST depression induced by exercise |
| **slope**   | Slope of the peak exercise ST segment (0 = Upsloping, 1 = Flat, 2 = Downsloping) |
| **ca**      | Number of major vessels (0–3) colored by fluoroscopy |
| **thal**    | Thalassemia (1 = Normal, 2 = Fixed Defect, 3 = Reversible Defect) |
| **target**  | Presence of heart disease (1 = Disease, 0 = No Disease) |

---

## 📊 Exploratory Data Analysis (EDA) Findings

- **Target Variable Distribution:**  
  - Patients with heart disease (1) ≈ **54%**  
  - Patients without heart disease (0) ≈ **46%**
  
- **Age Distribution:**  
  - Most patients are between **40–60 years old**.  
  - Mean age ≈ **54 years**.

- **Gender Distribution:**  
  - **Male:** ~68%  
  - **Female:** ~32%  

- **Correlation Insights:**  
  - Strong positive correlation between `cp` (chest pain type) and `target`.  
  - Negative correlation between `exang` (exercise-induced angina) and `target`.  
  - Higher `thalach` (max heart rate) tends to indicate no heart disease.  

---

## 🤖 Model Building

- **Model Used:** Logistic Regression  
- **Train/Test Split:** 80/20  
- **Performance Metrics:**
  - **Accuracy:** ~85%  
  - **Precision, Recall, F1-score:** Balanced across both classes  
  - **Confusion Matrix:** Shows strong classification performance with minimal false predictions.

---

## 📌 Insights

1. **Chest pain type (`cp`)** is one of the strongest predictors of heart disease.  
2. **Max heart rate (`thalach`)** being higher is associated with lower heart disease risk.  
3. **Exercise-induced angina (`exang`)** is a significant negative predictor.  
4. Older patients tend to have a slightly higher likelihood of heart disease, but age alone is not a definitive predictor.

---

## 💡 Recommendations

- **For Patients:**  
  - Regular health screenings, especially if over 40 years old.  
  - Monitor cholesterol and blood pressure levels regularly.  
  - Engage in safe cardiovascular exercises to improve heart rate capacity.

- **For Healthcare Providers:**  
  - Use predictive analytics to identify at-risk patients early.  
  - Pay special attention to chest pain patterns and exercise test results.  

- **For Further Model Improvement:**  
  - Experiment with other ML models like Random Forest, XGBoost, or Neural Networks.  
  - Include additional health data (e.g., BMI, smoking habits, family history).  

---

## 🏁 Conclusion

The Logistic Regression model achieved **~85% accuracy** in predicting heart disease using only basic patient metrics.  
With more diverse data and advanced models, predictive accuracy can be improved to assist medical professionals in **early diagnosis and prevention**.
