# 📊 Hotel Price Prediction

## 📌 Project Overview
This project aims to predict hotel room prices based on real-world data scraped from Booking.com and Expedia. The pipeline includes automated web scraping, data preprocessing, exploratory data analysis (EDA), machine learning regression models, deep learning architectures, and ranking algorithms to reverse-engineer the sorting mechanisms of hotel booking platforms.

---

## 📂 Project Structure
```
hotel-price-prediction/
├── data/
│   ├── raw/               # Scraped raw data
│   └── processed/         # Cleaned and preprocessed data
│
├── notebooks/
│   ├── scraping/          # Web scraping scripts
│   │   ├── booking_scraping.ipynb
│   │   └── expedia_scraping.ipynb
│   │
│   ├── preprocessing/     # Data preprocessing and feature engineering
│   │   ├── preprocessing_partB_1+2.ipynb
│   │   ├── preprocessing_partB3.ipynb
│   │   ├── preprocessing_partB4.ipynb
│   │   └── preprocessing_partB5.ipynb
│   │
│   └── modeling/          # Model training and evaluation
│       ├── regression_models.ipynb
│       └── sorting_algorithms.ipynb
│
├── reports/
│   └── images/            # Visualizations and graphs
│
├── README.md              # Project description
└── requirements.txt       # Required Python packages
```

---

## 📥 Data Collection (Scraping)
- Web scraping is performed using **Selenium**, **BeautifulSoup**, and **Scrapy**.
- Data is collected from **Booking.com** and **Expedia**, considering multiple factors:
  - Number of guests, room types, hotel stars, cancellation policies, price, and reviews.
  - `TTT (Time to Travel)`: The number of days between the search date and check-in.
  - `LOS (Length of Stay)`: The number of nights spent at the hotel.

---

## 📊 Data Preprocessing & Feature Engineering
- Cleaning missing values and handling inconsistencies.
- Removing outliers based on **Tukey’s method (1.5 IQR rule)**.
- Encoding categorical variables:
  - **Ordinal encoding** (e.g., room types, review scores: `Good < VeryGood < Excellent`).
  - **One-hot encoding** for categorical features (e.g., cancellation policies, neighborhoods).
- Feature engineering:
  - Extracting **day of the week** from check-in dates.
  - Identifying peak/off-peak pricing trends.
  - Distance to city center and impact on pricing.

---

## 🧠 Machine Learning Models

### 🔹 Regression Models for Price Prediction
Implemented various regression techniques to predict hotel prices:
- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **XGBoost Regressor**
- **Gradient Boosting Regressor**
- **Support Vector Regressor (SVR)**
- **Gaussian Process Regressor**
- **Neural Networks (MLP, CNN-based)** with an embedding layer for hotel categories

### 🔹 Feature Importance Analysis
- Used **SHAP values** and **Permutation Importance** to rank feature importance.
- Evaluated model performance using:
  - **MSE (Mean Squared Error)**
  - **RMSE (Root Mean Squared Error)**
  - **MAE (Mean Absolute Error)**
  - **R² (Coefficient of Determination)**

---

## 🔄 Reverse Engineering Sorting Algorithms
- Analyzed how hotel booking sites sort search results.
- Implemented models to predict ranking position:
  - **Gradient Boosting**
  - **Deep Learning-based ranking model**
- Evaluated results by comparing predicted ranking vs. actual site sorting.

---

## 🚀 Running the Project
### 1️⃣ Install dependencies
```bash
pip install -r requirements.txt
```

### 2️⃣ Run Web Scraping
```bash
python notebooks/scraping/booking_scraping.ipynb
python notebooks/scraping/expedia_scraping.ipynb
```

### 3️⃣ Preprocess Data
```bash
python notebooks/preprocessing/preprocessing_partB_1+2.ipynb
```

### 4️⃣ Train Regression Models
```bash
python notebooks/modeling/regression_models.ipynb
```

### 5️⃣ Evaluate Sorting Algorithms
```bash
python notebooks/modeling/sorting_algorithms.ipynb
```

---

