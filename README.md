# 🌳 Deforestation Issue Analysis Using Support Vector Machine (SVM)

## 🎯 Objective
Analyze deforestation across countries using SVM. Predict forest loss based on features like:
- CO₂ emissions
- Rainfall
- Population
- GDP
- Policy factors

---

## 📊 Phase 1: Data Preprocessing

### 🔹 Loading the Data
- Load dataset: `deforestation_dataset.csv`
- Inspect for missing values, anomalies, and data inconsistencies

### 🔹 Data Cleaning
- **Missing Values**: Impute or drop missing entries
- **Encoding**:
  - Label encode or one-hot encode categorical features such as:
    - `Deforestation_Policy_Strictness`
    - `Corruption_Index`

### 🔹 Feature Scaling
- Apply normalization/standardization to numerical features:
  - `CO2_Emission_mt`, `Population`, `GDP_Billion_USD`, etc.
- Optionally perform **feature selection** to improve model performance

### 🔹 Train-Test Split
- Split dataset: 80% training / 20% testing using `train_test_split`
- Ensure shuffle for unbiased training

---

## 🧠 Phase 2: Model Building and Evaluation

### ✅ Support Vector Machine (SVM) Model
- **Model Goal**:
  - Predict either `Forest_Loss_Area_km2` or `Tree_Cover_Loss_percent`

### 🔹 Implementation
- Train initial SVM model with **linear kernel**

### 🔹 Evaluation Metrics
- **MAE** (Mean Absolute Error)
- **MSE** (Mean Squared Error)
- **RMSE** (Root Mean Squared Error)
- **R-squared (R²)**

### 🔹 Visualization and Tuning
- Visualize results using scatter plots or regression lines
- If applicable, plot decision boundaries (for classification)

### 🔹 Hyperparameter Tuning
- Try other kernels: `rbf`, `poly`
- Tune hyperparameters:
  - `C`, `gamma`, `kernel`
- Use **GridSearchCV** or **RandomizedSearchCV**
- Apply **cross-validation** to validate performance

---

## 🔬 Phase 3: Feature Analysis and Interpretation

### 🔹 Feature Importance
- Analyze which features influence forest loss most
- Example insights:
  - High CO2 = greater forest loss
  - Poor policy strictness = higher deforestation

### 🔹 Results Interpretation
- Interpret coefficients (for linear kernel)
- Discuss:
  - Impact of GDP
  - Effect of corruption & illegal logging
  - Influence of rainfall and other natural factors

---

## 📌 Summary
This project applies Support Vector Machines to analyze global deforestation trends. Through data preprocessing, model evaluation, and feature interpretation, we extract key insights about deforestation drivers.

📦 **Future Steps**:
- Test on updated datasets
- Compare SVM with Random Forest or Gradient Boosting
- Integrate into dashboard for real-time deforestation monitoring
