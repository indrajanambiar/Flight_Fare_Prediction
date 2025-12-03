# Flight_Fare_Prediction
Domestic Flight Fare Predictions

A complete end-to-end machine learning workflow for predicting taxi fare prices using Python.  
This project includes data preprocessing, exploratory analysis, feature engineering, model training using multiple algorithms, evaluation, and final model export.

---

## Project Overview
The goal of this project is to build a regression model that predicts fare amounts based on trip-related features such as distance, duration, passenger count, and other metadata.

This repository includes:
- Data cleaning and preprocessing  
- Exploratory Data Analysis (EDA)  
- Feature engineering  
- Model training using multiple ML algorithms  
- Hyperparameter tuning  
- Model evaluation  
- Final export of the best-performing model  

---

## ML Models Trained
The notebook trains and evaluates multiple regression models:

| Model | Description |
|-------|-------------|
| Linear Regression | Baseline model, simple and interpretable |
| Decision Tree Regressor | Captures non-linear relationships |
| Random Forest Regressor | Ensemble model with improved performance |
| Gradient Boosting Regressor | Boosted ensemble for higher accuracy |
| XGBoost Regressor (if installed) | Advanced boosting algorithm |

The performance of each model is compared using RMSE, MAE, and R² score.

---

## Features Used for Training
Typical engineered features include:
- Trip distance  
- Trip duration  
- Pickup hour, day, month  
- Passenger count  
- Categorical encodings  
- Outlier removal  
- Missing value imputation  
- Normalization or scaling  

---

## Project Structure
```
├── b1_fare_prediction_model.ipynb   # Main notebook
├── data/                            # Input dataset(s)
├── models/                          # Exported pickle model
├── README.md                        # Documentation
```

---

## How to Run

### 1. Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux  
venv\Scripts\activate     # Windows
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

If requirements file is missing:
```bash
pip install numpy pandas scikit-learn matplotlib seaborn xgboost
```

### 3. Open the Notebook
```bash
jupyter notebook
```
OR  
Open `.ipynb` in VS Code or Jupyter Lab.

---

## Model Training Workflow
The training runs through these steps:

1. Load and explore dataset  
2. Clean data  
   - Remove nulls  
   - Fix incorrect values  
   - Remove outliers  
3. Feature engineering  
   - Create distance and duration  
   - Extract datetime features  
   - Encode categorical values  
4. Split dataset  
   - 80 percent training  
   - 20 percent testing  
5. Train multiple models  
6. Evaluate each model  
7. Select and export best model  

Final model is saved as:
```
models/fare_prediction_model.pkl
```

---

## Model Evaluation
Metrics used:
- RMSE (Root Mean Squared Error)
- MAE (Mean Absolute Error)
- R² Score

The model with the lowest RMSE and highest R² is selected.

---

## Exporting the Best Model
The notebook serializes the final trained model using pickle:

```python
import pickle

with open("models/fare_prediction_model.pkl", "wb") as f:
    pickle.dump(best_model, f)
```

---

"""


![Demo](https://github.com/indrajanambiar/Flight_Fare_Prediction/blob/main/demo_flight_fare.png)



| Command                                     | Description                                  |
| ------------------------------------------- | -------------------------------------------- |
| `pip install virtualenv`                    | Install virtual environment                  |
| `virtualenv ENV`                            | Create virtual environment by the name ENV    |
| `source ENV/bin/activate`                   | Activate ENV                                 |
| `pip install -r requirements.txt`           | Install project dependencies                 |
| `python app.py`                             | Run the project                              |
| `deactivate`                                | Close virtual environment once done           |


python app.py  ---> To open the application in localhost


