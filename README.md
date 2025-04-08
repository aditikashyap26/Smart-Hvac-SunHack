
# 🌬️ Smart HVAC System

A smart HVAC (Heating, Ventilation, and Air Conditioning) system that uses environmental sensor data and machine learning to predict and optimize temperature and humidity levels across 8 different zones. Developed during a Hackathon to simulate real-world intelligent climate control.

## 💡 Project Overview

This project involves collecting IoT sensor data (temperature, humidity, air quality, sunlight intensity) and applying Decision Tree Regression to predict temperature and humidity trends. Based on these predictions and current occupancy data, the system automatically adjusts climate control settings for energy efficiency and comfort.

## 🔧 Features

- 📊 Predicts future temperature and humidity levels using **Decision Tree Regression**
- 📈 Evaluates model accuracy with **MAE** and **R² Score**
- 🌡️ Adjusts climate settings based on **predicted temperature** and **room occupancy**
- 🧪 Trains models on zone-wise temperature/humidity datasets
- 🧠 Uses **occupancy detection** to optimize energy usage

## 🧰 Tech Stack

- **Python**
- **Pandas**, **NumPy**
- **scikit-learn**
- **Joblib**
- **Matplotlib** (optional for visualization)

## 🧠 Why Decision Tree Regression?

- Handles **non-linear** relationships between time and environmental features.
- Easy to **interpret and visualize**.
- Efficient on **small to medium datasets**, which is ideal for our hackathon use case.

## 📁 Folder Structure

```
📦 smart-havac-system
 ┣ 📜 main.py (core logic for training & simulation)
 ┣ 📁 data/ (contains zone-wise CSV sensor datasets)
 ┣ 📜 README.md (this file)
```

## 📈 How It Works

1. **Data Loading**: Temperature & humidity from CSVs (8 zone readings + timestamp)
2. **Preprocessing**: Calculates standard deviation across 8 zones
3. **Model Training**: Decision Tree Regressor trained on time series
4. **Prediction**: Predicts on future timestamps
5. **Environment Simulation**: Generates real-time environmental and occupancy data
6. **Decision Logic**: Based on predictions & occupancy, control decisions are printed

## 🧪 Sample Logic

```python
if temp > 28.0 and occupancy == 1:
    print("Turn on air conditioning")
elif humidity > 50.0 and occupancy == 1:
    print("Turn on dehumidifier")
else:
    print("Maintain normal conditions")
```

## 📦 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/aditikashyap26/Smart-Hvac-SunHack
cd Smart-Hvac-SunHack
```

### 2. Install Dependencies

```bash
pip install pandas scikit-learn joblib
```

### 3. Run the System

```bash
python main.py
```

## 🏆 Hackathon Participation

This project was built during a hackathon where participants were provided 8-zone sensor datasets and required to implement a real-time predictive climate control system.
