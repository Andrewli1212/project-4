Italy Real Estate Price Prediction

![](Images/housing.jpg)

This README provides an overview of the process used to predict house prices in Italy from a CSV dataset. The original dataset was in Italian, so it was translated to English. The prediction was carried out using machine learning models, including linear regression and random forest. The following sections outline the steps taken in this project:

Table of Contents

- [Introduction](#introduction)
    -[Motivation](#motivation)
- [Data Translation](#data_translation)
- [Data Cleaning](#data_cleaning)
- [Machine Learning Models](#machine_learning_models)
- [Outlier Detection and Handling](#outlier)
- [Feature Selection](#feature_selection)
- [Hyperparameter Tuning](#hyperparameter)
- [Model Selection](#model_selection)
- [Prediction](#prediction)
- [Statistical Analysis](#statistical_analysis)
- [Visualization](#visualization)

## Introduction
The real estate market in Italy is dynamic and complex, influenced by a myriad of factors such as location, property size, local amenities, economic conditions, and more. Accurately predicting house prices in such a diverse market can be a challenging yet crucial task for various stakeholders, including buyers, sellers, real estate agents, and investors. This project sets out to address this challenge by leveraging data and machine learning techniques to create a robust house price prediction model for Italy.

### Motivation
The motivation behind this project stems from the need for a reliable and data-driven approach to estimate house prices. Accurate price predictions can empower homebuyers to make informed decisions, assist real estate professionals in setting competitive prices, and guide investors in identifying profitable opportunities. By harnessing the power of machine learning, we aim to provide a tool that offers valuable insights into the Italian real estate market.

### Dataset
The heart of this project is a dataset that originally existed in Italian but has been meticulously translated into English. This dataset encompasses a wide range of features related to Italian properties, including their location, condition, amenities, and, most importantly, their sale prices. The dataset's diversity presents an opportunity to uncover meaningful patterns and relationships that can be used to make predictions.

## Methodology

The process of predicting house prices in Italy involves several crucial steps:

1. Data Translation: The dataset's translation from Italian to English ensures that all stakeholders can easily understand and work with the data.

2. Data Cleaning: To maintain data quality and reliability, we conduct thorough data cleaning, addressing missing values and data type inconsistencies.

3. Feature Selection: Not all features in the dataset are equally relevant for predicting house prices. Careful feature selection is employed to identify the most influential variables.

4. Machine Learning Models: We employ two machine learning models: Linear Regression and Random Forest. These models are chosen for their ability to capture complex relationships between features and the target variable.

5. Outlier Detection and Handling: Outliers, which can skew model predictions, are identified and appropriately handled through outlier detection techniques.

6. Hyperparameter Tuning: Fine-tuning the models' hyperparameters is essential to optimize their predictive performance. We employ both GridSearchCV and RandomizedSearchCV to find the best set of hyperparameters.

7. Model Selection: While the Random Forest model with RandomizedSearchCV demonstrates higher R-squared values, we prioritize model robustness. Thus, we choose the Random Forest model with GridSearchCV due to its ability to generalize well to unseen data.

8. Prediction: A user-friendly code is developed to enable users to input property features and receive accurate price predictions based on the selected model.

9. Statistical Analysis: We utilize Spark SQL to extract essential statistics from the dataset, providing deeper insights into property characteristics.

10. Visualization: Tableau is employed to create interactive visualizations, including charts and maps, to enhance data interpretation and model results communication.

By meticulously following these steps, we aim to deliver a house price prediction tool that not only offers accurate estimates but also contributes valuable insights into the Italian real estate market, benefitting a wide range of stakeholders.

## Machine Learning Models
Two machine learning models were considered for this project: linear regression and random forest. These models were chosen for their ability to predict house prices based on input features.

## Outlier Detection and Handling
Outliers can significantly impact the performance of machine learning models. To address this, we conducted outlier detection using boxplots and removed outliers from the dataset. Values above the upper bound were set to the upper bound value.

## Feature Selection
The target variable for prediction is "Price," and other columns were treated as features or dropped if they were not relevant for prediction.

## Hyperparameter Tuning
Hyperparameter tuning is essential for optimizing the performance of machine learning models. We used two different methods for hyperparameter tuning: GridSearchCV and RandomizedSearchCV.

- GridSearchCV:
GridSearchCV systematically tests a predefined set of hyperparameters for the model. It performs an exhaustive search over all possible hyperparameter combinations.

- RandomizedSearchCV:
RandomizedSearchCV, on the other hand, randomly samples from a range of hyperparameters, which makes it more computationally efficient than GridSearchCV. It explores a wide range of hyperparameters without trying all possible combinations.

## Model Selection
After hyperparameter tuning, we compared the performance of two Random Forest models: one tuned with GridSearchCV and the other with RandomizedSearchCV. The evaluation metric used was the R-squared (R2) value, which measures how well the model fits the data.

It's worth noting that the Random Forest model with RandomizedSearchCV yielded higher R2 values for both testing and training data:

Random Forest with GridSearchCV:

R2 for Testing Data: 0.62
R2 for Training Data: 0.70
Random Forest with RandomizedSearchCV:

R2 for Testing Data: 0.75
R2 for Training Data: 0.93
While the Random Forest model with RandomizedSearchCV showed better performance in terms of R2, it's important to consider the risk of overfitting. Overfitting occurs when a model performs exceptionally well on the training data but poorly on the testing data because it has essentially memorized the training data rather than learning the underlying patterns.

To mitigate the risk of overfitting and ensure that the selected model generalizes well to unseen data, we decided to choose the Random Forest model with GridSearchCV, which had lower R2 values for both training and testing data. This choice prioritizes the model's ability to make reliable predictions when applied to new, real-world data.

In summary, we opted for the Random Forest model with GridSearchCV despite its lower R2 values, as it offers a balance between model performance and generalization to ensure robust predictions on unseen data.

## Prediction
We developed a code that allows users to input values for each feature, and it returns a predicted house price using the selected random forest model.

## Statistical Analysis
We utilized Spark SQL to calculate statistics such as the median and other relevant information to gain insights into the dataset.

## Visualization
To enhance the understanding of the data and model results, we used Tableau to create various visualizations, including charts and maps.

In summary, this project aimed to predict house prices in Italy by translating the dataset, cleaning the data, selecting relevant features, using machine learning models, handling outliers, and visualizing the results. The Random Forest model, tuned with GridSearchCV, was chosen as the best model for this prediction task based on its R2 performance metrics.
