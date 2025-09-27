# California Housing Price Prediction

This project uses the **California Housing Dataset** from Kaggle to build and compare multiple regression models for predicting house prices.  

Dataset: [California Housing Prices – Kaggle](https://www.kaggle.com/datasets/camnugent/california-housing-prices)

---

## Dataset Information
- **Rows**: ~20,640  
- **Columns**: 10 features + 1 target  
- **Target Variable**: `median_house_value`  

Features include:
- `longitude`, `latitude` → Location coordinates  
- `housing_median_age` → Median age of houses in the block  
- `total_rooms`, `total_bedrooms` → Housing size indicators  
- `population`, `households` → Demographic indicators  
- `median_income` → Average income of households  
- `ocean_proximity` → Categorical (distance from ocean)  

---

## Preprocessing
- Handled **missing values** and **duplicates**  
- Applied **QuantileTransformer** (normalization) for numeric features  
- Applied **OneHotEncoder** for categorical features (`ocean_proximity`)  
- Split dataset: **75% train / 25% test**

---

## Models Used
We implemented and compared the following models:
1. **Linear Regression**
2. **Ridge Regression**
3. **Polynomial Regression (degree=2)**
4. **Random Forest Regressor**
5. **XGBoost Regressor**

---

## Model Results

### 1. Linear Regression
```python
MAE: 53611.76
RMSE: 71585.14
R²: 0.6212
```
### 2. Ridge
```python
MAE: 53598.32
RMSE: 71559.10
R²: 0.6215
```
### 3. Polynomial Regression
```python
MAE: 43051.65
RMSE: 60659.85
R²: 0.7280
```
### 4. RandomForest Regressor
```python
MAE: 31480.80
RMSE: 48504.61
R²: 0.8207
```
### 5. XGBoost Regressor
```python
MAE: 30414.61
RMSE: 46262.56
R²: 0.8418
```
### How to Run
```bash
git clone <https://github.com/here-2007/House-Pricing.git>
pip install -r requirements.txt
jupyter notebook house_price.ipynb
```
