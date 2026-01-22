# Sales Regression Analysis

## Overview

This project performs a comprehensive regression analysis on ecommerce customer data to predict yearly spending based on customer behavior metrics. The analysis includes exploratory data analysis (EDA), multiple linear regression modeling, and residual analysis to understand the relationship between customer engagement metrics and annual spending.

## Dataset

The dataset contains information about 500 ecommerce customers with the following features:

- **Email**: Customer email address
- **Address**: Customer address
- **Avatar**: Customer avatar
- **Avg. Session Length**: Average session length (minutes)
- **Time on App**: Time spent on mobile app (minutes)
- **Time on Website**: Time spent on website (minutes)
- **Length of Membership**: Years of membership
- **Yearly Amount Spent**: Target variable - total amount spent per year (dollars)

## Methodology

### 1. Exploratory Data Analysis (EDA)

The analysis begins with comprehensive data exploration using visualizations:

- **Joint plots**: Examined relationships between individual features and yearly spending
- **Pair plots**: Analyzed correlations between all numerical features
- **Linear model plots**: Visualized linear relationships, particularly focusing on membership length

### 2. Model Building

- **Features**: Selected 4 numerical features as predictors:
  - Avg. Session Length
  - Time on App
  - Time on Website
  - Length of Membership
  
- **Target Variable**: Yearly Amount Spent

- **Train-Test Split**: 70% training, 30% testing (random_state=42)

- **Model**: Multiple Linear Regression using scikit-learn

### 3. Model Evaluation

The model performance was evaluated using multiple metrics:

- **Mean Absolute Error (MAE)**: $8.43
- **Mean Squared Error (MSE)**: 103.92
- **Root Mean Squared Error (RMSE)**: $10.19

### 4. Residual Analysis

- Distribution of residuals to check for normality
- Q-Q plot to verify residual normality assumptions

## Requirements

To run this project, you'll need the following Python packages:

```bash
pandas
matplotlib
seaborn
scikit-learn
scipy
numpy
```

Install dependencies:
```bash
pip install pandas matplotlib seaborn scikit-learn scipy numpy
```

## Usage

1. Ensure the dataset file `Ecommerce Customers` is in the project directory
2. Open `Linear Regression.ipynb` in Jupyter Notebook
3. Update the file path in the notebook if necessary (currently points to `/Users/liburn/Desktop/Linear Regression Practice/Ecommerce Customers`)
4. Run all cells sequentially

## Results

The multiple linear regression model successfully predicts yearly customer spending with:
- **RMSE of $10.19**, indicating the model's predictions are on average within approximately $10 of actual values
- The model demonstrates good predictive performance for understanding customer spending patterns

## Key Insights

- The analysis explores how different customer engagement metrics (session length, app usage, website usage, and membership duration) relate to annual spending
- Visualizations help identify which features have stronger relationships with spending
- Residual analysis validates the model assumptions for linear regression

## Files

- `Linear Regression.ipynb`: Main Jupyter notebook containing the complete analysis
- `Ecommerce Customers`: Dataset file (CSV format)
- `ReadMe.md`: This file

## Notes

- The dataset contains 500 customer records with no missing values
- All numerical features are continuous variables
- The model uses a 70/30 train-test split for evaluation
