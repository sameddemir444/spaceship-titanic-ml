# Spaceship Titanic - Classification Project

This project is part of the Kaggle competition **Spaceship Titanic**.  
We approach the problem with a professional, real-world machine learning pipeline.
(https://www.kaggle.com/competitions/spaceship-titanic/overview)

---

## Problem Definition

The goal is to predict whether a passenger was transported to another dimension during the Spaceship Titanic incident.  
This is a **binary classification problem** where the target variable is `Transported` (True or False).

---

## Dataset Overview

The dataset includes two files:

| File        | Description                                              |
| ----------- | -------------------------------------------------------- |
| `train.csv` | Contains passenger data with labels (`Transported`)      |
| `test.csv`  | Contains passenger data without labels (for predictions) |

---

## Data Dictionary

| Column Name    | Description                                                       |
| -------------- | ----------------------------------------------------------------- |
| `PassengerId`  | Passenger ID (e.g., 0001_01)                                      |
| `HomePlanet`   | Planet the passenger departed from (Earth, Europa, Mars)          |
| `CryoSleep`    | Was the passenger in cryosleep? (True/False)                      |
| `Cabin`        | Cabin number (deck/num/side)                                      |
| `Destination`  | Destination planet (e.g., TRAPPIST-1e)                            |
| `Age`          | Passenger's age                                                   |
| `VIP`          | Was the passenger a VIP? (True/False)                             |
| `RoomService`  | Amount spent on room service                                      |
| `FoodCourt`    | Amount spent on food court                                        |
| `ShoppingMall` | Amount spent at shopping mall                                     |
| `Spa`          | Amount spent on spa                                               |
| `VRDeck`       | Amount spent on VR deck                                           |
| `Name`         | Full name of the passenger                                        |
| `Transported`  | **Target variable** – Was the passenger transported? (True/False) |

---

## Target Variable

- **Name:** `Transported`
- **Type:** Boolean
- **Task:** Binary Classification
- **Goal:** Predict if a passenger was transported (`True`) or not (`False`)

---

## Logistic Regression Model – Top 8 Features

We trained a **Logistic Regression model** using a fully optimized scikit-learn pipeline with only the **top 8 most important features**, selected based on **cumulative feature importance (95%)**.

### Model Pipeline

- **Preprocessing:** `StandardScaler` for numerical features, `OneHotEncoder` for categorical features
- **Model:** `LogisticRegression` tuned with `RandomizedSearchCV`
- **Hyperparameter Tuning:** 10 iterations, 5-fold cross-validation

### Final Model Metrics

- **ROC-AUC Score:** `0.8647`
- **F1 Score:** `0.79`
- **Accuracy:** `0.79`

### Model File

- Trained model saved as: `models/logistic_model_top8.pkl`
- Includes entire pipeline (preprocessing + estimator)
- Can be easily loaded via `joblib.load(...)`

### Features Used

| Feature             | Description                        |
| ------------------- | ---------------------------------- |
| `Spa`               | Amount spent on spa                |
| `VRDeck`            | Amount spent on VR deck            |
| `RoomService`       | Amount spent on room service       |
| `HomePlanet_Europa` | Binary feature for Europa          |
| `FoodCourt`         | Amount spent on food court         |
| `CryoSleep`         | Whether passenger was in cryosleep |
| `ShoppingMall`      | Amount spent at the shopping mall  |
| `HomePlanet_Mars`   | Binary feature for Mars            |

---

## Project Structure

spaceship-titanic/
├── data/
├── models/
├── notebooks/
├── utils/
├── spaceship_pipeline.py
└── README.md

---

## How to Run

1. Clone the repository
2. Install dependencies with: `pip install -r requirements.txt`
3. Run training: `python spaceship_pipeline.py`
4. Load model and predict using: `joblib.load("../models/logistic_model_top8.pkl")`

---

## Author

Samed Demir
[LinkedIn](https://www.linkedin.com/in/samed-demir/)
