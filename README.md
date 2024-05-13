# Yojo.com Review Popularity Prediction Model

Yojo.com, a leading player in the online shopping industry, aims to enhance customer satisfaction by predicting the popularity of product reviews based on textual features. This proactive approach will allow Yojo.com to address potential issues highlighted in reviews before they impact customer satisfaction and brand reputation negatively.

## Problem Statement

Can Yojo.com predict the popularity of product reviews based on textual features to proactively address potential issues and enhance customer satisfaction in the competitive online shopping market?

## Motivations and Approach

The motivation behind this project is to improve customer satisfaction and business performance for Yojo.com in the competitive online shopping industry. By leveraging machine learning techniques to predict review popularity, Yojo.com can intervene in potential issues highlighted in reviews, maintain high customer satisfaction levels, mitigate negative impacts on reputation, and drive growth and success.

## Dataset Analysis

### Data Preprocessing

Upon reviewing the `model.csv` dataset:
- Two categorical columns (`day` and `product_category`) need to be converted to numerical format for model inclusion.
- The `days` column will be mapped to numerical values.
- The `product_category` column will be encoded using dummy variables.

### Covariance Analysis and Feature Reduction

- Analyzed covariance between columns to identify redundant features.
- Columns with covariance greater than 50% with any other column were considered redundant and removed from the dataset.

### Outlier Detection and Handling

- Outliers were identified using the Interquartile Range (IQR) method.
- Outliers were capped instead of dropped to maintain data integrity.
- Summary statistics were reassessed post-outlier removal to ensure data representativeness.

## Modeling Process

### Data Splitting

- Separated the dataset into features (`X`) and target variable (`y`).
- The `shares` column was used as the target variable.
- Split the data into training and testing sets using `train_test_split`.

### Model Fitting and Evaluation

#### Decision Tree Model

- Developed a decision tree regression model to predict the number of shares.
- Trained the model and evaluated performance using Mean Absolute Error (MAE).

#### Random Forest Model

- Utilized a Random Forest regression model to predict the number of shares.
- Evaluated model performance using MAE and R^2.

#### Gradient Boosting Machines (XGBoost) Model

- Trained an XGBoost regression model to predict shares.
- Assessed model performance using MAE and R^2.
- Employed RandomizedSearchCV for hyperparameter tuning to optimize model performance.

## Conclusion

This project involved data preprocessing, feature reduction, outlier handling, and model training to predict the popularity of product reviews for Yojo.com. By leveraging machine learning models, Yojo.com can proactively address potential issues highlighted in reviews and enhance customer satisfaction in the competitive online shopping market.

---

*Note: This project was a collaborative effort with peers from the international Business Analytics and Big Data Master's program at POLIMI General School of Management.*
