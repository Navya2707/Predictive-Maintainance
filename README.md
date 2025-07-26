# Predictive-Maintainance
Built an LSTM and RNN-based predictive model to forecast aircraft engine failures using time-series sensor data, enabling proactive maintenance planning. ◦ Performed data preprocessing, sequence generation, and model tuning to improve prediction accuracy for binary classification of engine health status.
# 🚀 Aircraft Engine Failure Prediction using RNN/LSTM

This repository demonstrates how to build **RNN** and **LSTM** models to predict **aircraft engine failure** using time-series sensor data. The project focuses on forecasting whether an engine will fail within a specific number of cycles, allowing predictive maintenance and reducing unnecessary repair costs.

> 📌 Inspired by and adapted from an excellent notebook (original authors credited).

---

## 📚 Problem Statement

Aircraft engines are critical components that require careful monitoring to ensure safety and minimize costs. The goal of this project is to predict whether an engine will fail within a given **time window** (e.g., 30 cycles), using historical sensor data and cycles as input.

### Why It Matters:
- ✈️ Prevent sudden engine failures
- 💸 Reduce unnecessary maintenance and avoid high repair/replacement costs
- 🛠️ Enable timely and predictive maintenance scheduling

---

## 📂 Project Structure

📁 aircraft-engine-predictive-maintenance
│
├── data/ # Raw training and testing datasets
├── notebooks/
│ └── RNN_LSTM_Engine_Failure.ipynb # Main Jupyter notebook
├── models/ # Saved model files (optional)
├── README.md # Project documentation
└── requirements.txt # Python dependencies


---

## 📊 Dataset

The dataset contains information about multiple aircraft engines across operational cycles. Each record includes:

- Engine ID
- Cycle number
- 21 sensor measurements
- 3 operational settings

The aim is to predict whether an engine will fail within the next 30 cycles.

---

## 🔄 Preprocessing Steps

The preprocessing involves:

1. **Generating the Classification Target Variable**
   - Binary variable `failure_within_w1`, where `1` indicates failure within the next 30 cycles.

2. **Normalization**
   - Scaling sensor and operational data for stable training.

3. **Windowing**
   - Creating sequences of fixed window size for feeding into RNN/LSTM models.

---

## 🔍 Exploratory Data Analysis

Performed EDA to understand:
- Sensor trends before failures
- Cycle distribution
- Variation across engine IDs

---

## 🧠 Models Built

### 🔁 RNN Architectures:
- Simple RNN with 1 feature
- Simple RNN with 25 features
- Bi-Directional RNN with 25 features

### 🔄 LSTM Architecture:
- LSTM model built on multivariate time-series data (25 features)
- Designed to capture long-term dependencies

---

## 🧪 Evaluation

- Models evaluated using metrics like:
  - Accuracy
  - Precision, Recall
  - Confusion Matrix

---

## 🧮 Window Size Explanation

The **window** (`w1 = 30`) represents how early we want to flag a possible failure. By predicting engine failure 30 cycles in advance, we aim to give engineers enough time to schedule maintenance. This parameter can be adjusted (15, 45, etc.) based on business needs and desired accuracy.

---

## 🛠️ Tech Stack

- Python 3.x
- NumPy, Pandas
- Matplotlib, Seaborn
- Scikit-learn
- TensorFlow / Keras

---

## 📈 Future Enhancements

- Hyperparameter tuning
- Attention-based LSTM
- Integration with real-time IoT sensor streams
- Transformer-based time-series model

---

## 📝 References

- [Original Notebook Inspiration - Link to Notebook]
- NASA C-MAPSS Dataset
- [Kaggle Datasets](https://www.kaggle.com)
- TensorFlow Documentation

---





## 📌 Tags

`#LSTM` `#RNN` `#DeepLearning` `#PredictiveMaintenance` `#TimeSeries` `#AircraftFailurePrediction` `#Keras` `#AI` `#Python` `#DataScience`

