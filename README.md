# Used Car Price Prediction (Epochs '26 - Assignment 5)

## Business Objective
To build and evaluate multiple regression models capable of predicting the fair market value (selling price) of used cars based on historical attributes like vehicle age, kilometers driven, engine power, and fuel type.

## Dataset Overview
- **Source:** CarDekho Used Car Dataset from Kaggle.
- **Total Records:** 15,411 rows after cleaning and preprocessing.

## Features and Target Variable
- **Target Variable:** `selling_price`
- **Key Features:** `vehicle_age`, `km_driven`, `mileage`, `engine`, `max_power`, `seats`, along with one-hot encoded categorical features (`seller_type`, `fuel_type`, `transmission_type`, `brand`, `model`).

## Regression Models Implemented
1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor

## Performance Comparison Table

| Model | MAE | MSE | RMSE | R² Score |
| :--- | :--- | :--- | :--- | :--- |
| **Linear Regression** | 179292.23 | 1.56e+11 | 395382.57 | 0.7923 |
| **Decision Tree** | 122190.61 | 8.79e+10 | 296523.53 | 0.8832 |
| **Random Forest** | 98906.53 | 4.64e+10 | 215621.01 | 0.9382 |

## Best-Performing Model & Justification
- **Best Model:** Random Forest Regressor
- **Justification:** It achieved the highest $R^2$ Score of **0.938** and the lowest RMSE (**21,562**), meaning it explains ~94% of the variance in used car prices and generalizes much better by averaging multiple decision trees to minimize overfitting.

## Key Observations & Future Improvements
- **Observations:** Tree-based models (Decision Tree and Random Forest) significantly outperformed Linear Regression because car pricing involves complex non-linear relationships.
- **Future Improvements:**
  1. Perform hyperparameter tuning using `GridSearchCV` on the Random Forest model.
  2. Explore advanced gradient boosting algorithms like XGBoost or LightGBM to further drive down the error metrics.
