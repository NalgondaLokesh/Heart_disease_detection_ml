# 🧠 Heart Disease Risk Predictor - MediMystery Labs

Welcome to **MediMystery Labs**, where data meets diagnostics!  
This project uses Bayesian Networks to predict heart disease risk from simulated patient data using probabilistic modeling with `pgmpy`.

---

## 📁 Dataset

**Source:** [heart_disease.csv](https://bit.ly/3T1A7Rs)  
A dataset of anonymized patient records with features like age, fasting blood sugar (fbs), cholesterol (`chol`), maximum heart rate (`thalach`), and diagnosis outcome (`target`).

---

## 🎯 Problem Statement

> As a Data Detective at MediMystery Labs, your mission is to predict the **risk of heart disease** using a probabilistic model.  
You must clean the dataset, apply min-max normalization, discretize features, define a Bayesian structure, and draw diagnostic inferences.

---

## 🧪 Approach

1. **Data Cleaning**
   - Removed duplicates and missing values.

2. **Feature Engineering**
   - Min-max normalization of numerical columns.
   - Discretized `age`, `chol`, and `thalach` into categories (`low`, `medium`, `high`).

3. **Bayesian Network Construction**
   - Defined structure as:
     ```
     age → fbs → target → chol, thalach
     ```
   - Trained using **Maximum Likelihood Estimation (MLE)** with `pgmpy`.

4. **Inference**
   - Used `VariableElimination` to answer key questions:
     - What is the probability of heart disease given age?
     - How does cholesterol level vary if heart disease is present?
     - How do age and fbs influence risk?

---

## 📊 Visualizations

- Network structure graph
- Bar plots for disease probability by age
- Heatmap for risk across cholesterol and thalach levels
- Cholesterol distribution conditioned on disease

---

## 🔍 Key Insights

- Middle-aged and old patients with high fasting blood sugar showed increased risk.
- Cholesterol tends to be high among patients with heart disease.
- Low `thalach` and high `chol` together significantly raise risk levels.

---

## 🛠️ Tech Stack

- Python
- `pandas`, `scikit-learn` for preprocessing
- `pgmpy` for Bayesian modeling
- `matplotlib`, `seaborn`, `networkx` for visualization

---

## 🚀 How to Run

1. Clone this repo or open the notebook in Google Colab.
2. Install dependencies:
   ```bash
   pip install pgmpy pandas scikit-learn matplotlib seaborn networkx
