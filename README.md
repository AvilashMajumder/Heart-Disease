# ❤️ Heart Disease Prediction using Machine Learning

A machine learning project that predicts whether a person is likely to have heart disease based on clinical parameters.  
This project uses **Logistic Regression** on the popular UCI-style heart disease dataset and is implemented in a Jupyter Notebook.

---

## 📌 Project Overview

Cardiovascular disease is one of the leading causes of death worldwide. Early prediction can assist in timely diagnosis and preventive care.

In this project, I built a binary classification model to predict heart disease presence:

- **1 → Defective Heart (Heart Disease Present)**
- **0 → Healthy Heart (No Heart Disease)**

The workflow includes:

- Data loading and inspection
- Data preprocessing checks
- Feature-target split
- Train-test split with stratification
- Logistic Regression model training
- Accuracy-based model evaluation
- Single-sample prediction system

---

## 🧠 Tech Stack

- **Python**
- **NumPy**
- **Pandas**
- **Scikit-learn**
- **Jupyter Notebook**

---

## 📂 Repository Structure

```text
Heart-Disease/
│
├── Heart_Disease.ipynb          # End-to-end ML workflow
├── heart_disease_data.csv       # Dataset (303 rows, 14 columns)
└── README.md                    # Project documentation
```

---

## 📊 Dataset Information

The dataset contains **303 patient records** and **14 columns**:

### Features

1. `age` – Age of patient  
2. `sex` – Gender (1 = male, 0 = female)  
3. `cp` – Chest pain type  
4. `trestbps` – Resting blood pressure  
5. `chol` – Serum cholesterol (mg/dl)  
6. `fbs` – Fasting blood sugar > 120 mg/dl  
7. `restecg` – Resting electrocardiographic results  
8. `thalach` – Maximum heart rate achieved  
9. `exang` – Exercise induced angina  
10. `oldpeak` – ST depression induced by exercise  
11. `slope` – Slope of peak exercise ST segment  
12. `ca` – Number of major vessels colored by fluoroscopy  
13. `thal` – Thalassemia category  

### Target

- `target`:
  - `1` = Heart disease present
  - `0` = No heart disease

### Class Distribution

- Heart disease present (`1`): **165**
- No heart disease (`0`): **138**

---

## ⚙️ Model Building Pipeline

1. Loaded CSV data using Pandas
2. Checked:
   - shape
   - data types
   - null values (none found)
   - summary statistics
3. Split data:
   - `X` = all input features
   - `Y` = target
4. Train-test split:
   - `test_size=0.2`
   - `stratify=Y`
   - `random_state=2`
5. Trained a **LogisticRegression** classifier
6. Evaluated performance using accuracy score

---

## ✅ Results

- **Training Accuracy:** `0.8512` (~85.12%)
- **Testing Accuracy:** `0.8197` (~81.97%)

These results indicate good generalization with a small train-test gap.

---

## 🔍 Sample Prediction

The notebook includes a manual prediction system for a single patient input:

```python
input_data = (62,0,0,140,268,0,0,160,0,3.6,0,2,2)
```

Output example from your notebook:

- Prediction: `[0]`
- Interpretation: **The person does not have heart disease**

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/AvilashMajumder/Heart-Disease.git
   cd Heart-Disease
   ```

2. Install dependencies:
   ```bash
   pip install numpy pandas scikit-learn jupyter
   ```

3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

4. Open and run:
   - `Heart_Disease.ipynb`

---

## 📈 Possible Improvements

For future enhancement, this project can be extended by:

- Adding feature scaling (`StandardScaler`)
- Hyperparameter tuning (`GridSearchCV`)
- Trying other models:
  - Random Forest
  - XGBoost
  - SVM
- Evaluating with:
  - Precision / Recall / F1-score
  - ROC-AUC
  - Confusion Matrix
- Deploying as a web app (Streamlit / Flask)

---

## 👤 Author

**Avilash Majumder**  
GitHub: [@AvilashMajumder](https://github.com/AvilashMajumder)
