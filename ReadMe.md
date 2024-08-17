# Predicting CPU Performance: Multiple Linear Regression Model

## Project Overview

This project focuses on building a Multiple Linear Regression model to estimate the relative CPU performance of computer hardware based on various hardware attributes. The dataset used is from the UCI Machine Learning Repository and contains information about different computer models, including machine cycle time, main memory, cache memory, and more. The goal is to predict the Estimated Relative Performance (ERP) of these computers.

## Problem Statement

In this project, the primary objective is to estimate the relative CPU performance (ERP) of various computer hardware configurations. This estimation is based on several factors such as machine cycle time (MYCT), minimum and maximum main memory (MMIN and MMAX), cache memory (CACH), and the number of minimum and maximum channels (CHMIN and CHMAX).

The problem can be framed as a regression task where we aim to predict a continuous target variable, ERP, using the given features.

## Dataset

The dataset used in this project is the **Computer Hardware Dataset** from the UCI Machine Learning Repository. It consists of 209 rows and 10 columns. The columns include:

- **Vendor Name**: The name of the computer vendor.
- **Model Name**: The unique identifier for each computer model.
- **MYCT**: Machine cycle time in nanoseconds.
- **MMIN**: Minimum main memory in kilobytes.
- **MMAX**: Maximum main memory in kilobytes.
- **CACH**: Cache memory in kilobytes.
- **CHMIN**: Minimum channels in units.
- **CHMAX**: Maximum channels in units.
- **PRP**: Published relative performance (not used in model building).
- **ERP**: Estimated relative performance (target variable).

The dataset is clean, with no missing values, and contains both categorical and numerical variables. However, only numerical variables are used in building the regression model.

## Exploratory Data Analysis (EDA)

Exploratory Data Analysis was performed to gain insights into the dataset. Key steps included:

- **Checking the dimensions** of the dataset (209 rows, 10 columns).
- **Renaming columns** for better readability.
- **Identifying categorical and numerical variables**.
- **Exploring the distribution** of numerical variables.
- **Detecting correlations** between features and the target variable using Pearson’s correlation coefficient.
- **Visualizing correlations** using a heatmap.

Key findings from EDA:
- Strong positive correlations were observed between ERP and memory-related features (MMIN, MMAX).
- Some weak negative correlations were found between ERP and MYCT.

## Model Building

### Data Preparation

The dataset was divided into predictor variables (X) and the target variable (y). The predictor variables were then split into training and test sets using an 80-20 split. Feature scaling was applied to standardize the predictor variables.

### Model Training

A Multiple Linear Regression model was built using the Scikit-Learn library. The model was trained on the training set and used to predict ERP on the test set.

### Model Evaluation

The model's performance was evaluated using standard regression metrics, including:

- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **R-squared (R²)**

The evaluation showed that the model performs well on the dataset, with a reasonable R² score indicating the model's effectiveness in explaining the variability in ERP.

## Learning Outcomes

Through this project, the following skills and concepts were reinforced:

- **Understanding and implementing Multiple Linear Regression**: The project provided hands-on experience in building and interpreting a multiple linear regression model.
- **Data preprocessing**: Techniques such as feature scaling and handling categorical variables were practiced.
- **Exploratory Data Analysis (EDA)**: The importance of EDA in understanding data and guiding model development was highlighted.
- **Model evaluation**: Learned how to evaluate regression models using different metrics and interpret the results to assess model performance.

## Future Work

Potential improvements and extensions of this project could include:

- **Feature Engineering**: Adding polynomial features or interaction terms to capture non-linear relationships.
- **Regularization**: Applying techniques like Ridge or Lasso regression to handle potential multicollinearity and improve model generalization.
- **Model Comparison**: Comparing the performance of multiple linear regression with other regression techniques like Decision Trees, Random Forests, or Support Vector Machines.

## Conclusion

This project successfully demonstrates the application of Multiple Linear Regression to predict the estimated relative CPU performance of computer hardware. By leveraging Python and Scikit-Learn, a robust model was developed, offering insights into the factors that influence CPU performance.
