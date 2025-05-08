# Spaceship Titanic - Classification Project

This project is part of the Kaggle competition **Spaceship Titanic**.  
We approach the problem with a professional, real-world machine learning pipeline.

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
