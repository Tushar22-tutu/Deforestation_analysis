# 🚚 Food Delivery Time Prediction

## 🎯 Objective
The goal is to predict food delivery time using regression and classify delivery speed (Fast/Delayed) using logistic regression. The model uses features like:
- Customer and restaurant location
- Weather and traffic conditions
- Vehicle type
- Distance and order-related details

---

## 📊 Phase 1: Data Collection and Exploratory Data Analysis (EDA)

### 🔹 Step 1 - Data Import and Preprocessing
- **Load dataset**: `Food_Delivery_Time_Prediction.csv`

#### Handle Missing Values
- Inspect missing values in key columns like `Distance`, `Delivery_Time`
- Use **imputation** (mean/median) or **drop rows/columns** if needed

#### Data Transformation
- **Encode categorical variables**:
  - Label Encoding or One-Hot Encoding for:
    - `Weather_Conditions`
    - `Traffic_Conditions`
    - `Vehicle_Type`
- **Normalize numerical columns**:
  - Use `StandardScaler` or `MinMaxScaler` on:
    - `Distance`, `Delivery_Time`, `Order_Cost`

### 🔹 Step 2 - Exploratory Data Analysis (EDA)
- **Descriptive Statistics**:
  - Mean, median, variance for numerical columns
- **Correlation Analysis**:
  - Use heatmaps to find correlation with `Delivery_Time`
- **Outlier Detection**:
  - Use boxplots and IQR method to detect and treat outliers

### 🔹 Step 3 - Feature Engineering
- **Distance Calculation**:
  - Compute geodesic distance using Haversine formula if not available
- **Time-Based Features**:
  - Extract `hour`, `is_rush_hour`, `day_of_week` to capture delivery patterns

---

## 🔧 Phase 2: Predictive Modeling

### ✅ Step 4 - Linear Regression Model
- **Train-Test Split**:
  - Use `train_test_split` (80/20)

#### Model Building
- Use **Linear Regression** with features:
  - `Distance`, `Traffic_Conditions`, `Order_Priority`

#### Evaluation Metrics
- **Mean Squared Error (MSE)**
- **R-squared (R²)**
- **Mean Absolute Error (MAE)**

### ✅ Step 5 - Logistic Regression Model (Binary Classification)

#### Objective
- Classify delivery status as:
  - **0 = Fast**, **1 = Delayed**

#### Features
- `Traffic_Conditions`, `Weather_Conditions`, `Delivery_Person_Experience`, etc.

#### Evaluation Metrics
- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**
- **Confusion Matrix**

---

## 📌 Summary
This project demonstrates how to use regression and classification for food delivery time prediction. It builds a robust preprocessing pipeline and evaluates model accuracy using standard metrics.

📦 **Next Steps**:
- Hyperparameter tuning (GridSearch)
- Model comparison with Random Forest, SVM
- Deploy with Flask or Streamlit
