# 🌦️ Comprehensive Weather Data Analysis & Predictive Modeling

### *A Case Study of Mansoura, Egypt (1994–2024)*

## 🧭 Overview

This project explores **30 years of historical weather data for Mansoura, Egypt (1994–2024)** to uncover patterns, trends, and predictive insights.
The goal is to build a **complete data science pipeline**: from cleaning and engineering features to modeling and evaluating predictive performance.

This project was developed during a **machine learning training program**, and served as a capstone to consolidate all learned concepts—covering real-world challenges such as handling multi-format datasets, feature engineering at scale, and model selection.

---

## 🎯 Objectives

* Analyze historical weather patterns and identify seasonal trends.
* Engineer advanced temporal features to improve model accuracy.
* Build classification and regression models for temperature and weather conditions.
* Evaluate model performance and extract actionable insights for forecasting and planning.

---

## 📊 Dataset Description

### Source & Time Range

* **Location:** Mansoura, Egypt
* **Time span:** August 1994 → June 2024
* **Data Format:** Multiple files and formats (CSV, Excel, etc.) were merged and standardized.
* **Challenge:** The data came in **different formats, encodings, and column naming conventions**, requiring careful preprocessing to unify and structure it.

### Columns Overview

| Category             | Example Columns                                     | Description                                             |
| -------------------- | --------------------------------------------------- | ------------------------------------------------------- |
| Temperature          | `temp`, `tempmax`, `tempmin`                        | Daily max, min, and average temperatures                |
| Humidity & Dew Point | `humidity`, `dew`                                   | Atmospheric humidity and dew point                      |
| Wind & Solar         | `winddir`, `windspeed`, `uvindex`, `solarradiation` | Environmental factors                                   |
| Precipitation        | `precip`, `precipprob`, `precipcover`               | Rainfall metrics                                        |
| Temporal Features    | `month`, `season`, `week_number`, `day`             | Engineered for time-series patterns                     |
| Target Labels        | `temp_category`                                     | Categorical variable based on previous-year temperature |

📎 **Note:** A classification column was added to label each day as *Higher*, *Lower*, or *Normal* compared to the same date in the previous year.

---

## 🧹 Data Preprocessing & Feature Engineering

The dataset required extensive preprocessing to prepare it for analysis:

* ✅ Unifying column names across multiple files.
* 🧽 Handling missing values and inconsistent encodings.
* 🧮 Creating **rolling statistics** (`temp_7d_avg`, `temp_30d_avg`, `humidity_7d_avg`, `wind_30d_avg`, etc.).
* 🕒 Extracting **temporal features**: day, week number, season, month.
* 📊 Generating **lag and delta features**: `previous_temp`, `temp_change`, `temp_range`, `prev_year_month_temp_std`.
* ⚙️ Scaling and encoding variables for model input.

---

## 🔍 Exploratory Data Analysis (EDA)

EDA was conducted to explore patterns and relationships across 30 years of weather data:

* 🌡️ Seasonal temperature trends and anomalies.
* 🌧️ Rainfall distribution and seasonal shifts.
* 🌬️ Wind and solar radiation variability.
* 📈 Correlations between humidity, temperature, and dew point.

🖼️ **Figures to include**:

* [ ] Temperature trend over years (Line chart)
* [ ] Monthly average temp vs humidity (Bar/Line combo)
* [ ] Correlation heatmap
* [ ] Precipitation distribution per season

---

## 🧠 Modeling & Machine Learning

The project includes **both classification and regression tasks**:

| Type           | Models Used                                                                                      | Targets                          | Metrics            |
| -------------- | ------------------------------------------------------------------------------------------------ | -------------------------------- | ------------------ |
| Classification | Logistic Regression, Random Forest, KNN, Naive Bayes, Gradient Boosting, Decision Tree           | `temp_category`                  | Accuracy           |
| Regression     | Linear Regression, Random Forest Regressor, KNN Regressor, Gradient Boosting, Decision Tree, SGD | temperature and related features | MAE, MSE, RMSE, R² |

---

## 🧪 Evaluation & Results

* Baseline classification accuracy: `XX%` *(replace with actual number)*
* Best regression R² score: `X.XX` *(replace with actual number)*
* Feature engineering significantly improved both accuracy and R² compared to using raw columns.

🖼️ **Figures to include**:

* [ ] Classification model performance comparison (bar plot)
* [ ] Regression error distribution (histogram or residual plot)
* [ ] Actual vs Predicted temperature scatter plot

---

## 🧭 Key Challenges

* ⏳ **Time Constraints**: This project was built as part of an intensive training program with limited delivery time.
* 🧾 **Data Complexity**: Data collected from multiple files and formats required standardization and careful handling.
* 🧠 **Feature Engineering**: Creating lag features and rolling windows at scale for 30 years of daily data was computationally demanding.
* ⚖️ **Model Tuning**: Balancing simplicity (baseline models) with performance under limited time.

---

## 🛠️ Tech Stack

* **Language:** Python 3.12+
* **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn, windrose
* **Environment:** Jupyter Notebook
* **Version Control:** Git (planned for deployment)

---

## 📌 Next Steps

* Add cross-validation and hyperparameter tuning.
* Integrate forecasting models (SARIMAX, Prophet, LSTM).
* Containerize pipeline for deployment.
* Build interactive dashboard for insights visualization.

---

## 📝 How to Run

```bash
# 1. Clone this repository
git clone [your-repo-link]

# 2. Install dependencies
pip install -r requirements.txt

# 3. Open the notebook
jupyter notebook final-project-weather.ipynb

# 4. Run all cells in sequence
```

---

## 🏁 Acknowledgements

This project was developed as part of a machine learning training program to apply end-to-end ML workflow skills on a **real-world, long-span dataset**.

---
