# Housing Price Prediction using Linear Regression

## Overview

This project focuses on implementing **Simple Linear Regression** and **Multiple Linear Regression** techniques to predict housing prices based on various features such as area, number of bedrooms, bathrooms, and other categorical attributes. The objective is to understand how linear models behave with one or multiple independent variables and how to evaluate and interpret their performance.

---

## Project Objective

To build predictive models using linear regression to estimate housing prices from structured data. The key goals include:

- Applying simple and multiple linear regression using `scikit-learn`.
- Preprocessing and preparing data for regression analysis.
- Evaluating model accuracy using various metrics.
- Visualizing relationships and interpreting model coefficients.

---

## Dataset Description

- **Dataset Source**: [Kaggle - Housing Prices Dataset](https://www.kaggle.com/datasets/yasserh/housing-prices-dataset)
- **File Used**: `Housing.csv`

### Features in the dataset:

| Feature Name        | Description                                               |
|---------------------|-----------------------------------------------------------|
| price               | Target variable (house price in INR)                     |
| area                | Area of the house in square feet                          |
| bedrooms            | Number of bedrooms                                        |
| bathrooms           | Number of bathrooms                                       |
| stories             | Number of floors/stories                                  |
| mainroad            | Whether the house is on the main road (yes/no)            |
| guestroom           | Whether it has a guest room (yes/no)                      |
| basement            | Whether it has a basement (yes/no)                        |
| hotwaterheating     | Availability of hot water heating (yes/no)                |
| airconditioning     | Availability of air conditioning (yes/no)                 |
| parking             | Number of parking spaces                                  |
| prefarea            | Whether it is in a preferred area (yes/no)                |
| furnishingstatus    | Furnishing status (unfurnished, semi-furnished, furnished)|

---

## Tools and Libraries Used

- Python 3.13.3
- `pandas` - for data manipulation
- `numpy` - for numerical operations
- `scikit-learn` - for model building and evaluation
- `matplotlib` & `seaborn` - for data visualization

---

## Project Workflow

### 1. Data Loading and Exploration
- The dataset was loaded using `pandas`.
- Basic information such as data types, missing values, and sample entries were explored.

### 2. Data Preprocessing
- **Missing values**: Checked and handled (if any).
- **Encoding**: Categorical variables such as `mainroad`, `guestroom`, etc., were label-encoded using `LabelEncoder`.
- **Feature selection**: Target (`price`) and predictor variables were separated.
- **Scaling/Normalization**: Not mandatory for linear regression but considered based on distribution.

### 3. Train-Test Split
- Data was split into 80% training and 20% testing using `train_test_split` from `sklearn.model_selection`.

### 4. Simple Linear Regression
- A model was built using only one independent variable (`area`) to predict `price`.
- Model trained using `LinearRegression()` from `sklearn.linear_model`.
- Predictions and a regression line were visualized using `matplotlib`.

### 5. Multiple Linear Regression
- All independent variables were used to train a model.
- Model trained on training data and predictions made on test data.
- Coefficients were extracted and interpreted.
- Multicollinearity was assessed using a correlation matrix heatmap.

### 6. Model Evaluation
The model's performance was measured using the following metrics:
- **Mean Absolute Error (MAE)**: Average absolute difference between actual and predicted values.
- **Mean Squared Error (MSE)**: Average of squared differences between actual and predicted values.
- **R² Score**: Indicates how well features explain the variability in the target variable.

---

## Key Findings

- The simple linear regression model using only `area` provided a baseline performance.
- The multiple regression model achieved higher accuracy by leveraging all available features.
- Features such as `area`, `airconditioning`, and `furnishingstatus` had significant influence on housing prices.
- Multicollinearity was assessed using correlation matrices to ensure model reliability.

---

## File Structure

```

housing-price-prediction-linear-regression/
│
├── dataset/
│   └── Housing.csv
│
├── linear_regression_model.ipynb      # Main notebook for analysis
├── requirements.txt                   # Required packages
└── README.md                          # Project documentation

```

---

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/atharmshaikh/housing-price-prediction-linear-regression.git
cd housing-price-prediction-linear-regression
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Open in Jupyter Notebook

You can run the notebook locally using:

```bash
jupyter notebook linear_regression_model.ipynb
```

Or use Google Colab by replacing the GitHub URL in the browser like this:

```
https://githubtocolab.com/atharmshaikh/housing-price-regression-analysis/blob/main/linear_regression_model.ipynb
```

---

## Requirements

The following packages are required and can be installed via `pip`:

```txt
pandas
numpy
scikit-learn
matplotlib
seaborn
```

---
