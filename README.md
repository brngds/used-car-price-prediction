# 🚗 Used Car Price Prediction

Machine learning project to predict used car prices using **Linear Regression, Random Forest and LightGBM**, comparing predictive accuracy, training time and prediction speed.

## 📌 Context

Rusty Bargain is a used car sales service developing an application that allows customers to quickly estimate the market value of their vehicles.

The company needs a reliable machine learning model that provides accurate price predictions while maintaining efficient training and prediction times.

## 🎯 Business Problem

The objective is to predict the price of a used vehicle based on its technical specifications, registration information and historical data.

Three criteria are considered:

- Prediction quality
- Prediction speed
- Model training time

The primary evaluation metric is **Root Mean Squared Error (RMSE)**, expressed in euros.

## 📊 Dataset

The project uses the `car_data.csv` dataset, containing **354,369 records** before preprocessing.

The target variable is:

- `Price` — vehicle price in euros

The original dataset includes information about vehicle type, registration year, gearbox, engine power, model, mileage, fuel type, brand, repair status and listing metadata.

## 🔎 Methodology

1. Data loading and exploratory analysis
2. Identification of missing values and inconsistent records
3. Removal of duplicates and invalid observations
4. Feature selection and preprocessing
5. Categorical encoding and numerical scaling
6. Training, validation and test split
7. Linear Regression baseline
8. Random Forest hyperparameter tuning
9. LightGBM hyperparameter tuning
10. Comparison of RMSE, training time and prediction speed
11. Final evaluation on the test dataset

After data cleaning, the dataset contains **329,506 records and 11 columns**.

## 🤖 Machine Learning Models

### Linear Regression

Used as a baseline to evaluate whether more advanced models provide meaningful improvements.

The model achieved a validation RMSE of approximately **€2,654.46**.

### Random Forest

A tree-based ensemble model evaluated using different combinations of tree count and maximum depth.

The purpose was to assess whether nonlinear relationships could improve prediction quality compared with the linear baseline.

### LightGBM

A gradient boosting model evaluated using multiple hyperparameter configurations.

LightGBM was selected for final testing based on its predictive performance and computational efficiency.

## 📈 Final Results

The selected LightGBM model achieved:

**Test RMSE: €1,611.93**

This means that the model's typical prediction error, measured by RMSE, is approximately €1,612. RMSE penalizes larger prediction errors more heavily.

The project also measures training and prediction times to support the selection of a model suitable for a customer-facing price estimation application.

## 💡 Key Findings

- Data cleaning is essential when working with real-world vehicle listings.
- Linear Regression provides a useful baseline for model comparison.
- Tree-based algorithms capture nonlinear relationships in vehicle pricing.
- LightGBM provides strong predictive performance.
- Model selection should consider both accuracy and computational efficiency.

## 🚀 Business Applications

The model could support:

- Instant used car price estimates
- Vehicle valuation tools
- Pricing recommendations for sellers
- Identification of potentially overpriced or underpriced listings
- Data-driven pricing strategies

## ⚠️ Limitations

The model is trained on historical vehicle listings and may require retraining as market conditions change.

Additional limitations include potential reporting errors in vehicle characteristics, regional pricing differences and the absence of some variables that may influence vehicle value.

The reported RMSE reflects evaluation on the available dataset and does not guarantee the same performance in production.

## 🛠️ Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- LightGBM
- Jupyter Notebook

## 📁 Repository Structure

```text
used-car-price-prediction/
├── README.md
├── data/
│   └── car_data.csv
└── notebook/
    └── used_car_price_prediction.ipynb
```

## ▶️ Running the Project

Clone the repository and open the notebook located in the `notebook` directory.

The dataset is stored in the `data` directory.

Install the required Python libraries, including Pandas, NumPy, Matplotlib, Scikit-learn and LightGBM.

---

### Author

**Brunno Almeida**

Data Science | Data Analytics | Python | SQL | Machine Learning
