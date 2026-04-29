# 🌍 Air Quality Index (AQI) Prediction System

## 📌 Overview

This project focuses on predicting the Air Quality Index (AQI) using Machine Learning techniques. The system analyzes pollutant concentrations and environmental factors to forecast AQI levels and classify air quality.

---

## 🎯 Objectives

* Predict AQI values using ML models
* Identify pollution trends
* Classify air quality (Good / Moderate / Poor)
* Provide insights for environmental management

---

## 📊 Dataset

The dataset used is **city_day.csv**, which contains:

### Features:

* Pollutants: PM2.5, PM10, NO, NO2, NOx, CO, SO2, O3
* Other factors: Benzene, Toluene, Xylene
* Time-based features: Year, Month, Day, Hour

### Target:

* AQI (Air Quality Index)

---

## ⚙️ Technologies Used

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn

---

## 🧠 Machine Learning Models

The following models were implemented:

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor ✅ (Best Model)

---

## 🔧 Data Preprocessing

* Missing values handled using forward fill
* Date column converted and time features extracted
* Feature engineering applied:

  * PM2.5 / PM10 ratio
  * NO2 / CO ratio
* Non-numeric columns removed
* Remaining missing values filled with mean

---

## 📈 Model Evaluation

| Model             | RMSE      |
| ----------------- | --------- |
| Linear Regression | 58.23     |
| Decision Tree     | 53.44     |
| Random Forest     | **40.54** |

Cross-Validation RMSE: **90.83**

👉 Random Forest performed best with lowest error.

---

## 📊 Results

* Accurate AQI predictions were achieved
* Predicted values closely match actual values
* Example predictions:

  * Actual: 137 → Predicted: 134.84
  * Actual: 339 → Predicted: 358.11

---

## 📉 Visualizations

### 🔹 AQI Prediction Trend

The graph shows predicted vs actual AQI values over time.
(*See output graph in notebook – page 3*)

### 🔹 Feature Importance

According to the model:

* PM2.5 is the most important feature
* CO is the second most important
* Other pollutants have smaller impact

(*Feature importance chart shown in page 3 of output*)

---

## 🏷️ AQI Classification

| AQI Range | Category |
| --------- | -------- |
| 0–50      | Good     |
| 51–100    | Moderate |
| >100      | Poor     |

Example:

* AQI 76 → Moderate
* AQI 190 → Poor

---

## 💡 Key Insights

* PM2.5 is the dominant factor affecting AQI
* High AQI levels indicate poor air quality
* Random Forest handles complex relationships effectively
* Pollution trends can be predicted in advance

---

## 🚀 How to Run the Project

### 1. Install dependencies

```
pip install -r requirements.txt
```

### 2. Run the notebook

```
jupyter notebook aqi_prediction.ipynb
```

---

## 📁 Project Structure

```
AQI-Prediction-System/
│
├── city_day.csv
├── aqi_prediction.ipynb
├── README.md
├── requirements.txt
```

---

## 🔮 Future Improvements

* Real-time AQI prediction using APIs
* Deployment using Streamlit or Flask
* Integration with weather forecasting systems
* Deep learning models for higher accuracy

---

## 👨‍💻 Author

Your Name

---

⭐ If you found this project useful, give it a star!
