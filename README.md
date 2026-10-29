# US-Traffic-Accidents-Analysis-Severity-Prediction
# US Traffic Accidents Analysis & Severity Prediction

## Project Overview
This project analyzes US traffic accidents to identify the key factors influencing accident severity and traffic disruption duration.

The project combines data analysis and machine learning to explore temporal, environmental, and road-related patterns, predict high-severity accidents, and estimate accident duration.

## Objectives
- Analyze traffic accident patterns across different time periods.
- Investigate the relationship between weather, lighting, and accident severity.
- Identify road and environmental factors associated with severe accidents.
- Predict accident severity using machine learning classification models.
- Estimate accident duration using regression models.

## Dataset
- **Dataset:** US Accidents (March 2023)
- **Coverage:** US traffic accident records.
- **Analysis Period:** 2020–2023.
- **Data Format:** CSV.

Note: The dataset is not included in this repository. Download the original dataset and place `US_Accidents_March23.csv` in the project folder before running the notebook.

## Project Workflow

### 1. Data Cleaning & Preprocessing
- Removed duplicate records.
- Handled missing values using statistical and conditional imputation techniques.
- Processed date and time columns.
- Removed invalid records and outliers.
- Applied geographical validation.

### 2. Feature Engineering
Created additional features, including:
- Time of Day and Season.
- Weekend and Rush Hour indicators.
- Accident Duration.
- Impact Ratio.
- Road Complexity.
- Lighting Phase.
- Environmental risk indicators.

### 3. Exploratory Data Analysis (EDA)
Analyzed:
- Accident severity distribution.
- Accidents by hour and month.
- Weather and lighting conditions.
- Accident duration across severity levels.
- Road infrastructure impact.
- Correlations between engineered features and accident severity.

### 4. Machine Learning

**Severity Classification**
- Logistic Regression.
- XGBoost Classifier.
- Class imbalance handling.
- Hyperparameter tuning.
- Decision threshold optimization.
- Cross-validation and model evaluation.

**Duration Regression**
- XGBoost Regressor.
- Log transformation of the target variable.
- Randomized Search for hyperparameter tuning.
- MAE, RMSE, and R² evaluation.

## Key Results

### Severity Classification
Final improved XGBoost model:
- Accuracy: 89%
- Precision (High Severity): 55%
- Recall (High Severity): 67%
- F1-Score (High Severity): 60%
- AUC-ROC: 0.9101

### Duration Prediction
XGBoost Regressor:
- MAE: 55.1 minutes
- RMSE: 115.7 minutes
- R²: 0.3097

## Technologies & Tools
- **Programming:** Python
- **Data Processing:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn, XGBoost, Imbalanced-learn
- **Model Explainability:** SHAP
- **Model Persistence:** Joblib
- **Environment:** Jupyter Notebook

## Repository Structure

```text
US-Traffic-Accidents-Analysis/
│
├── depi-Final.ipynb
├── README.md
├── requirements.txt
├── .gitignore
│
└── saved_models/
    └── Trained model files
```

## How to Run

1. Clone this repository:

```bash
git clone YOUR_REPOSITORY_URL
```

2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

3. Download the dataset and place it in the project directory.

4. Open `depi-Final.ipynb` using Jupyter Notebook or VS Code.

5. Run the notebook cells sequentially.

## Disclaimer
This project is developed for educational and analytical purposes. Model predictions are experimental and should not be used as a substitute for real-world emergency response decisions.
