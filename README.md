# 🏠 House Price Prediction — Ames Housing Dataset

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Latest-orange.svg)
![Kaggle](https://img.shields.io/badge/Kaggle-Competition-20BEFF.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

> Predicting house sale prices using the Ames Housing Dataset with advanced feature engineering and ensemble modeling techniques.

---

## 📌 Project Overview

This project tackles the classic **House Prices: Advanced Regression Techniques** Kaggle competition. The goal is to predict the final sale price of homes in Ames, Iowa based on 79 explanatory variables describing almost every aspect of residential homes.

The project follows a structured ML pipeline:

```
Data Cleaning → EDA → Preprocessing → Feature Engineering → Modeling
```

---

## 📁 Project Structure

```
house-price-prediction/
│
├── 📁 notebooks/
│   ├── 01_Data_Cleaning.ipynb
│   ├── 02_Data_Preprocessing.ipynb
│   ├── 03_Feature_Engineering.ipynb
│   ├── 04_EDA.ipynb
│   ├── 05_Linear_Regression.ipynb
│   └── 06_Advanced_Modeling.ipynb
│
├── 📁 data/
│   ├── raw/                        # Original Kaggle data
│   ├── processed/                  # Cleaned & engineered data
│   └── submissions/                # Kaggle submission files
│
├── 📁 docs/
│   ├── data_description.txt        # Feature descriptions
│   └── new_features_list.txt       # Engineered features list
│
├── .gitignore
└── README.md
```

---

## 🔧 Pipeline

### 1. Data Cleaning
- Handled missing values using domain knowledge
- Removed outliers based on GrLivArea vs SalePrice analysis
- Fixed data type inconsistencies


### 2. Data Preprocessing
- Label encoding for ordinal features
- One-hot encoding for nominal features
- Log transformation on skewed features

### 3. Feature Engineering
Created **28 new features** including:

| Feature | Description |
|---|---|
| `TotalSF` | Total square footage (all floors + basement) |
| `TotalBathrooms` | Combined bathroom count |
| `Quality_x_Area` | Overall quality × living area |
| `HouseAge` | Age of house at time of sale |
| `IsNewHouse` | Binary flag for new construction |
| `OverallQual_Squared` | Non-linear quality interaction |
| `GrLivArea_Squared` | Non-linear area interaction |

> Full list available in `docs/new_features_list.txt`


### 4. Exploratory Data Analysis (EDA)
- Analyzed target variable distribution (SalePrice)
- Identified key correlations with sale price
- Visualized neighborhood, quality, and area trends

### 5. Modeling

| Model | RMSE (Log Scale) |
|---|---|
| Linear Regression | 0.13 |
| **Advanced Ensemble** | **0.11** ✅ |

---

## 🏆 Results

| Metric | Score |
|---|---|
| Best Kaggle RMSE | **0.11** |
| Baseline RMSE | 0.13 |
| Improvement | ~15% |

The best performing model achieved a Kaggle score of **0.11** using ensemble methods with engineered features.

---

## ⚙️ Installation & Usage

### Requirements
```bash
pip install pandas numpy scikit-learn matplotlib seaborn xgboost lightgbm
```

### Run the project
```bash
# Clone the repository
git clone https://github.com/AliAbbasov/house-price-prediction.git
cd house-price-prediction

# Run notebooks in order
jupyter notebook notebooks/01_Data_Cleaning.ipynb
```

> Follow notebooks in sequential order (01 → 06) for full pipeline.

---

## 📊 Dataset

- **Source:** [Kaggle — House Prices: Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)
- **Train set:** 1,460 samples, 79 features
- **Test set:** 1,459 samples
- **Target:** `SalePrice` (continuous)

---

## 🛠️ Tech Stack

- **Python 3.8+**
- **Pandas & NumPy** — Data manipulation
- **Matplotlib & Seaborn** — Visualization
- **Scikit-learn** — Preprocessing & modeling
- **XGBoost / LightGBM** — Advanced modeling

---

## 👤 Author

**Ali Abbasov**  
[![GitHub](https://img.shields.io/badge/GitHub-AliAbbasov-black.svg)](https://github.com/AliAbbasov)

---

## 📄 License

This project is licensed under the MIT License.
