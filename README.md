# 🌾 Crop Recommendation System (Machine Learning)

A machine learning–based crop recommendation system built using **Decision Tree**, **Random Forest**, and **XGBoost** classifiers.  
This project emphasizes **model reliability, probabilistic recommendations, and dataset limitations**, rather than blind accuracy.

---

## 📌 Project Motivation

Most crop prediction projects focus only on achieving high accuracy.  
However, in real-world agriculture, **high accuracy does not guarantee trustworthy predictions**.

This project explores:
- Why models can be highly accurate yet agronomically unreliable
- How dataset limitations affect predictions
- Why probabilistic and hybrid approaches are safer for real-world use

---

## 🧠 Models Used

- Decision Tree Classifier
- Random Forest Classifier (primary & most reliable)
- XGBoost Classifier (analyzed for overconfidence)

---

## 📊 Dataset

- **Crop Recommendation Dataset**
- Features used:
  - Nitrogen
  - Potassium
  - Temperature
  - Humidity
  - pH Value
  - Rainfall
- Target:
  - Crop name (multi-class classification)

⚠️ *Phosphorus was removed during experimentation to study feature impact.*

---

## ⚙️ Machine Learning Pipeline

1. Data preprocessing & feature selection  
2. Train–test split with stratification  
3. Hyperparameter tuning using **GridSearchCV**  
4. Model evaluation using:
   - Accuracy
   - Precision, Recall, F1-score
   - Confusion Matrix
5. Manual testing with real-like inputs
6. Probability-based crop recommendations (Top-K)

---

## ✅ Key Findings

- High accuracy (**~99%**) does NOT guarantee correct real-world predictions
- XGBoost often becomes **overconfident** due to tight dataset clusters
- Random Forest provides **more stable and trustworthy predictions**
- Dataset lacks critical agronomic features (soil type, altitude, season, irrigation)

---

## 🚨 Important Limitations

- This system is **NOT suitable for real farming decisions**
- Predictions are **statistical**, not agronomic advice
- Dataset contains overlapping feature ranges for multiple crops
- Missing causal features prevent full generalization

---

## ✅ Recommended Usage

✔ Educational purposes  
✔ Machine learning experimentation  
✔ Understanding model bias & limitations  

❌ Real-world agricultural deployment  
❌ Single-crop blind prediction systems  

---

## 📈 Example Output (Top-3 Recommendation)

```text
Maize        0.42
Coffee       0.31
ChickPea     0.18
