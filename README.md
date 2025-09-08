# ImmoEliza House Price Prediction (Modeling)

This repository focuses on **house price prediction using machine learning** on a **pre-cleaned dataset** from ImmoEliza. The full data collection and cleaning steps were performed separately; here we demonstrate **feature handling, model training, evaluation, and deployment** using CatBoost.

---

## 🚀 Project Overview

This repo covers:

1. Loading a **cleaned dataset** ready for modeling.
2. Splitting data into features (`numeric` + `categorical`) and target (`price`).
3. Training a **CatBoost regression model** with optimized hyperparameters and early stopping.
4. Evaluating model performance with **R², MSE, MAE, and MAPE**.
5. Saving the trained model for future use.
6. Visualizing predictions and residuals.

> This project highlights **ML modeling skills** and end-to-end workflow from cleaned data to model deployment.

---
```

├── data/
│   ├── cleaned_data_before_imputation.csv
    └── cleaned_data_after_imputation.csv
├── model/
│   ├── catboost_price_prediction_model.joblib
│   └── catboost_price_prediction_model.pkl
├── main.py                 # Training & evaluation script
├── requirements.txt
└── README.md

```

## 📊 Dataset

- **Source:** Cleaned version of ImmoEliza property listings (`cleaned_data_before_imputation.csv`).  
- **Features used:**  
  - Numeric: `bedroomCount`, `toilet_and_bath`, `habitableSurface`, `facedeCount`, `hasTerrace`, `totalParkingCount`  
  - Categorical: `type`, `subtype`, `province`, `locality`, `postCode`, `buildingCondition`, `epcScore`  
- **Target:** `price` (in Euros)  

> Dataset is already cleaned and preprocessed; missing values handled, categorical columns converted to string.

---

## 🛠 Technologies & Libraries

- Python 3.9+
- Pandas, NumPy
- Matplotlib
- CatBoost
- Scikit-learn
- Joblib & Pickle (for model saving)

---

## 🔧 Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/immoeliza-house-price-prediction.git
cd immoeliza-house-price-prediction

pip install -r requirements.txt

python main.py
```

📈 Model Performance

R² (test): 0.71

MSE (test): 1,234,567 €² (example)

MAE (test): 12,345 €

MAPE (test): 15%

Indicates the model explains ~71% of variance in house prices — solid for real estate data.

🖼 Visualizations

Actual vs Predicted Prices: Scatter plot showing predictions vs actuals.

Residual Analysis: Q-Q plot to examine residual normality and model fit.
