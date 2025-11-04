# 🩺 Diabetes Progression Simulation

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](PASTE_YOUR_COLAB_LINK_HERE)

---

## 📘 Overview

This project simulates **diabetes progression** using AI models to predict one-year disease outcomes for clinical trial design.  
It demonstrates how machine learning can enable **Synthetic Control Arms**, reducing placebo usage and accelerating ethical medical trials.

---

## ⚙️ Methodology

- Dataset: **442 patients** from Scikit-learn’s diabetes dataset  
- Features: Age, sex, BMI, blood pressure, and six serum measurements  
- Models tested: Ridge, Lasso, Random Forest, Gradient Boosting  
- Final model: **Ridge Regression** (best tradeoff between bias & variance)  

**Evaluation:**
- 80/20 split for train/test  
- Metrics: R², RMSE, MAE, feature importance  

---

## 📈 Results

| Metric | Value |
|--------|-------|
| **R² Score** | 0.45 |
| **RMSE** | 53.8 |
| **MAE** | 43 |
| **Top Predictors** | BMI, Blood Pressure, S5 (lipids) |

⚠️ *Note:* Prototype trained on small public dataset — production models require large-scale EHR or trial data.

---

## 💡 Clinical Impact

### 🎯 Synthetic Control Arms
Use model predictions instead of placebo patients →  
Reduces trial cost by **40–60%**, makes studies **faster and more ethical**.

### 🔍 Patient Stratification
Predict high-risk patients early → enables personalized treatment strategies.

### 🧬 Trial Enrichment
Focus on patients most likely to respond → smaller, more effective studies.

---

## 🧠 Tech Stack

| Layer | Current | Production |
|-------|----------|------------|
| Model | Ridge Regression | Ensemble (XGBoost, RF) |
| Framework | Scikit-learn | PyTorch / FastAPI |
| Visualization | Matplotlib, Seaborn | Streamlit Dashboard |
| Storage | CSV | PostgreSQL / Cloud Data |

---

## 🚀 Production Roadmap

1. **Collect real-world clinical data** (10K+ patients)
2. **Upgrade model** to ensemble or neural regression
3. **Add explainability** with SHAP values
4. **Deploy API** for real-time prediction and integration
5. **Validate** results through clinical trial simulation

---

## 🧭 Usage

### 🧪 Run in Google Colab
[🔗 Open in Colab](https://colab.research.google.com/drive/1vAdbXmc9GUHZtqHBavdiNWFBNd9kbWU8?usp=drive_link)

### 💻 Run Locally
```bash
git clone https://github.com/mostafathemar/Diabetes-Progression-Simulation.git
cd Diabetes-Progression-Simulation
pip install -r requirements.txt
jupyter notebook diabetes_simulation.ipynb
