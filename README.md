# House Price Prediction with Linear Regression

A machine learning project focused on predicting house prices using a Linear Regression model.

## Project Overview

The goal of this project is to build a linear regression model that predicts house prices based on various features of residential properties.

The project includes data exploration, preprocessing, feature engineering, model training, prediction, and evaluation.

## Objectives

* Explore and analyze the dataset
* Identify relationships between features and house prices
* Encode categorical features
* Create additional features
* Split the data into training and testing sets
* Build a Linear Regression model using scikit-learn
* Evaluate the model using MAE and MSE
* Visualize actual and predicted house prices

## Dataset

The dataset contains information about residential properties and their sale prices.

The target variable is:

* `SalePrice` — the sale price of the house

Some of the important features include:

* `GrLivArea` — above-ground living area
* `OverallQual` — overall material and finish quality
* `Street` — type of road access
* `SaleCondition` — condition of the sale

The dataset is stored in `data/sales.csv`.

## Exploratory Data Analysis

The analysis shows that larger living areas (`GrLivArea`) tend to be associated with higher house prices. Higher overall quality (`OverallQual`) is also associated with higher `SalePrice`.

Categorical features such as `Street` and `SaleCondition` also affect the distribution of house prices and were therefore encoded before training the model.

## Feature Engineering

An additional binary feature representing garage availability was created:

* `0` — no garage
* `1` — garage available

## Model

A Linear Regression model from the `scikit-learn` library was used for prediction.

The dataset was divided into training and testing subsets. Predictions were generated for both datasets to compare model performance.

## Model Evaluation

The model was evaluated using:

* **MAE (Mean Absolute Error)**
* **MSE (Mean Squared Error)**

The test set MAE was approximately **25,116**, meaning that the model's predictions differed from the actual house prices by about 25,000 on average.

The MAPE was approximately **13.7%**, meaning that the predicted house price differed from the actual price by about 14% on average.

MAE was considered the primary evaluation metric because MSE is more sensitive to outliers. The dataset contains expensive houses that can significantly increase the MSE value.

The training and testing errors were relatively close, suggesting that there was no significant overfitting.

## Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Project Structure

```text
house-price-linear-regression/
│
├── data/
│   └── sales.csv
├── notebooks/
│   └── linear_regression.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run

Clone the repository and install the required dependencies:

```bash
pip install -r requirements.txt
```

Then open the Jupyter Notebook:

```bash
jupyter notebook
```

Run the cells in `linear_regression.ipynb` to reproduce the analysis and model results.

## Conclusion

The project demonstrates the complete basic workflow of a supervised machine learning regression task, from data exploration and preprocessing to model training and evaluation.

The Linear Regression model achieved an average prediction error of approximately 13.7% according to MAPE, while the MAE on the test set was approximately 25,116.
