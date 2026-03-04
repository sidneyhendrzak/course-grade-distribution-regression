# Predicting University Course Grade Distributions

This project models final university course grade distributions (percent of students earning A, B, C, D, F) from assessment and grading data as part of the MATH 637 – Mathematical Techniques in Data Science final project. 

## Project Overview

We use multiple regression models to predict the distribution of final course grades based on different combinations of features such as exams, homework, quizzes, and grade weights. The goal is to understand which assessment components are most informative for predicting overall outcomes. 

## Methods

- **Models:** Linear Regression, Ridge, Lasso, Elastic Net, Decision Tree, Random Forest, K‑Nearest Neighbors. 
- **Techniques:** Train/test split, feature scaling, hyperparameter tuning with `GridSearchCV`, repeated runs across multiple random seeds to assess consistency. 
- **Evaluation:** Mean Absolute Error (MAE), Mean Squared Error (MSE), custom error metric, R² scores. 
- **Visualization:** Bar plots comparing predicted vs. true grade distributions for different models. 

## Data

- The data consists of anonymized course‑level summaries with features derived from exams, homework, quizzes, and grading weights. 
- Multiple feature sets are considered:
  - All parameters
  - No quiz or miscellaneous components
  - Exams & homework only
  - Combined exam scores & homework only
  - Weights only 
- Data files are stored as CSVs and as a combined Excel workbook with multiple sheets for convenience. 

> Note: All data have been anonymized and contain no individual student identifiers.

## Key Results

- Across multiple feature sets and random seeds, Elastic Net and Linear Regression often achieve the lowest and most consistent MAE, around 7–8 percentage points in predicted grade distributions. 
- Comparing feature sets shows how much information is retained when quizzes or miscellaneous components are removed, and how far you can go using only weighted components. 

## Repository Structure

- `MATH637_FinalProject.ipynb` – Main notebook with all model training, evaluation, and plots. 
- `Final Datasheet - XDataImport*.csv` – Input feature tables for different feature sets. 
- `Final Datasheet - YDataImport - DISTRIBUTION.csv` – Target grade distribution table. 
- `course_grades_data.xlsx` – Combined Excel workbook with all sheets (optional convenience format). 

## How to Run

1. Clone or download this repository.
2. Ensure all CSV data files (and/or the Excel workbook) are in the same directory as `MATH637_FinalProject.ipynb`. 
3. Open the notebook in Jupyter or Google Colab.
4. Run all cells from top to bottom; the notebook will:
   - Load the datasets
   - Train multiple regression models
   - Evaluate them with MAE and other metrics
   - Plot predicted vs. true grade distributions. 

## Authors

Team project for **MATH 637 – Mathematical Techniques in Data Science**. 

- Jacob Meredith  
- Madison Johnson  
- Sidney Hendrzak  
- Joshua LaFrance 
