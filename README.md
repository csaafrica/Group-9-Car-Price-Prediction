# Car Price Prediction — Case Study

**A data-driven pricing model for used cars**

---

## Overview

This project implements a full end-to-end workflow for predicting used-car selling prices from raw marketplace data: data cleaning, exploratory data analysis (EDA), feature engineering, model training, evaluation, and interpretation. It was built as part of a group case study and demonstrates practical skills in data engineering, machine learning, and storytelling for business stakeholders.

---

## Highlights

* End-to-end reproducible pipeline: data ingestion → preprocessing → EDA → model training → evaluation.
* Feature engineering tailored to automotive pricing (parsing combined `Name` field into make/model/year/engine/color, car age calculation, mileage transformations).
* Rigorous evaluation using MAE, RMSE, and R² and model-interpretability (feature importance).
* Clear visualizations to support recommendations to a dealership (price distributions, brand-level analysis, mileage vs price relationships).

---

## Dataset

The dataset contains the following core columns used in modelling:

* `price` — selling price (target)
* `transmission` — gearbox type (e.g., Automatic, Manual)
* `condition` — vehicle condition (e.g., Foreign Used)
* `mileage` — distance driven (km)
* `Name` — combined string containing manufacturer, model, year, engine and color (e.g., `Toyota Premio 2015 1.8 FWD Black`)

(See project materials for the raw dataset and additional metadata.)

---

## Approach

1. **Data cleaning & parsing**

   * Split `Name` into `make`, `model`, `year`, `engine_info`, and `color`.
   * Convert `year` to numeric and compute `car_age = current_year - year`.
   * Handle missing values and outliers.
   * Encode categorical variables (one-hot or label encoding where appropriate) and scale numeric features.

2. **Exploratory Data Analysis (EDA)**

   * Identify most common brands and models.
   * Inspect price distribution and outliers.
   * Analyze relationships between mileage, age and price.
   * Compare price across transmission types and conditions.

3. **Modeling**

   * Train regression algorithms: baseline Linear Regression and Random Forest.
   * Use cross-validation and a hold-out test set.
   * Evaluate with MAE, RMSE and R².
   * Extract top features influencing price.

---

## Results & Interpretation

* Best model: `RandomForestRegressor`
* Test MAE: **157097.3990**
* Test RMSE: **688122.8292**
* Test R²: **0.9327**

Top features: `car_age`, `mileage`, `model`, `engine_size`

**Key Insight:** The analysis showed that car age and engine size are the strongest predictors of price, with premium model cars commanding a significant price premium over other brands counterparts.

---

## How to run (reproducible)

1. Clone the repository:

```bash
git clone https://github.com/csaafrica/Group-9-Car-Price-Prediction.git
cd Group-9-Car-Price-Prediction
```

2. Create and activate a virtual environment (recommended):

```bash
python -m venv venv
source venv/bin/activate   # macOS / Linux
venv\Scripts\activate    # Windows
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Open the notebooks or run the scripts in `src/` to reproduce the steps:

* `notebooks/` — exploratory notebooks and modelling experiments.
* `src/` — modular code (preprocessing, training, evaluation).

5. Re-run experiments and export results (example):

```bash
# if there is a train script available
python src/train.py --data data/raw/cars.csv --out results/
```

---

## Repository structure

```
/Group-9-Car-Price-Prediction
├─ notebooks/            # EDA and modelling notebooks
├─ src/                  # Source code: preprocessing, model training, helpers
├─ data/                 # (not stored in repo) raw and processed data
├─ requirements.txt
├─ README.md
└─ LICENSE
```

---

## Skills demonstrated

* Python, pandas, scikit-learn
* EDA & data visualization (matplotlib / seaborn)
* Feature engineering & preprocessing
* Model building & evaluation (regression)
* Clear storytelling and business-oriented recommendations

---
## Contributors

* Max Kinyua - Team Lead
* Vallarie Wakhula
* Angelica Ogato
---

License: MIT

---
