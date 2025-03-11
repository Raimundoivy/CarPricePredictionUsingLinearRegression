# Car Price Prediction with Linear Regression

## Description

This project focuses on predicting the Manufacturer's Suggested Retail Price (MSRP) of cars using a linear regression model. The analysis includes data exploration, preprocessing, feature engineering, model training, and evaluation. The original Jupyter Notebook has been converted to a Python script (`car_prediction.py`).

## Installation

This project requires the following Python libraries:

*   pandas
*   numpy
*   scikit-learn
*   seaborn
*   matplotlib

You can install these dependencies using pip:

```bash
pip install pandas numpy scikit-learn seaborn matplotlib


It is also necessary to download the dataset and place it in a directory relative to your script location, in this case "C:\Users\Raimu\PastaMain\Documentos\car_prediction_linear_sklearn\data.csv". Ensure this path exists and is accessible or modify it to be your dataset path.

Usage

The car_prediction.ipynb script performs the entire workflow, from data loading to model evaluation. Conceptually, the script is structured like a Jupyter Notebook, with "cells" of code performing specific tasks. To run the script and reproduce the analysis, follow these steps:

Ensure Dependencies are Installed: Make sure you have installed all the required libraries as described in the "Installation" section.

Download the Dataset: Obtain the data.csv file. This file is assumed to be located at C:\Users\Raimu\PastaMain\Documentos\car_prediction_linear_sklearn\data.csv. If you place the file elsewhere, you must update the file path in the script.

Run the Script: Execute the Notebook script from your IDE :)

python car_prediction.py

Script Walkthrough and expected output:

Cell 1 & 2 (Import Libraries and Load Data): Imports necessary libraries (pandas, numpy, scikit-learn, seaborn, matplotlib) and loads the car dataset from the specified CSV file. Defines the columns to be used.

Cell 3 (Basic Data Overview): Prints the shape of the dataset, the first 5 rows, data types of each column, missing values, and descriptive statistics. This provides an initial understanding of the data.

Cell 4 & 5 (Univariate Analysis - MSRP): Visualizes the distribution of the target variable (MSRP) using a histogram and a Kernel Density Estimate (KDE) plot. A second plot is then generated showing the effect of log transformation on the distribution.

Cell 6 (Univariate Analysis - Numerical Features): Creates histograms and KDE plots for numerical features like 'Year', 'Engine HP', 'Engine Cylinders', 'highway MPG', 'city mpg', and 'Popularity'.

Cell 7 (Multivariate Analysis - Correlation): Generates a correlation heatmap to show the relationships between numerical features and MSRP.

Cells 8-10 (Data Preprocessing): Handles missing values using SimpleImputer (mean imputation for numerical features and most frequent imputation for categorical features) and performs one-hot encoding on categorical features.

Cells 11-13 (Data Splitting): Splits the data into training and testing sets (80% train, 20% test) using train_test_split. Handles any discrepancies in columns between training and testing sets resulting from one-hot encoding.

Cells 14 & 15 (Model Training and Evaluation): Trains a Linear Regression model on the training data and evaluates its performance on the testing data. Prints Mean Squared Error (MSE), R-squared, and Mean Absolute Error (MAE).

Cell 16 (Actual vs. Predicted Distribution): Displays a histogram comparing the distribution of actual MSRP values with the predicted values. This visualization helps assess the model's performance.

Cell 17-19 (Feature Engineering & Retraining - 'Engine HP Squared'): Introduces a new feature, 'Engine HP Squared', to capture potential non-linear relationships. Then it retrains and re-evaluates the model, outputting MSE, R-squared, MAE, and the Actual vs Predicted plot. The new feature's effect on performance is shown. The .to_markdown() calls output formatted tables of the dataframe's head and info.

Cell 20-22 (Feature Engineering & Retraining - Log & Ratio): Adds two new features: 'Engine HP Log' (logarithmic transformation of 'Engine HP') and 'Popularity per HP' (ratio of 'Popularity' to 'Engine HP'). The model is then retrained and re-evaluated, with results (MSE, R-squared, MAE, and Actual vs Predicted plot) printed. The .to_markdown() calls output formatted tables of the dataframe's head and info.

The script will print various outputs to the console, including:

Dataframe shapes, head previews, data types, missing value counts, and descriptive statistics.

Evaluation metrics (MSE, R-squared, MAE) for the initial model and after each feature engineering step.

Formatted tables showing the dataframes after feature engineering.

Several plots will also be displayed showing:

Histograms of MSRP and numerical features.

A correlation heatmap.

Histograms comparing actual and predicted MSRP distributions.

Dependencies

pandas

numpy

scikit-learn

seaborn

matplotlib

(Specific version numbers were not tracked in the original notebook, but the latest versions available at the time of writing should work.)
