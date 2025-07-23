# ML Based Crop Price Prediction 

This project focuses on predicting monthly average prices of agricultural commodities using historical data. The dataset includes prices for 22 commodities from 2014 to 2023. The objective is to build machine learning models that can forecast future prices to aid farmers, policy makers, and supply chain managers.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Approach](#approach)
- [Technologies Used](#technologies-used)
- [Usage Instructions](#usage-instructions)
- [Results](#results)
- [Future Work](#future-work)

## Overview

Forecasting agricultural prices helps mitigate market volatility and supports data-informed decision-making. This project uses machine learning to model historical price trends and predict future monthly average prices for various commodities.

## Dataset

The dataset contains:

- Price records for 22 commodities
- Monthly data from January 2014 to December 2023
- Columns: `Commodity`, `Year`, `Jan`, `Feb`, `March`, `April`, `May`, `June`, `July`, `August`, `September`, `November`, `December`

Data preprocessing steps include:

- Encoding categorical variables (Commodity and Month)
- Z-score normalization to scale features
- Capping outliers based on standard deviation thresholds

## Approach

The modeling process included the following:

1. **Data Preprocessing**: Encoding categorical variables, applying Z-score normalization, and capping extreme outliers
2. **Modeling**: Two models were trained and compared:
   - **Linear Regression** (baseline)
   - **Support Vector Regression (SVR)**  
3. **Evaluation**: Model performance was assessed using error metrics like Mean Squared Error (MSE)

SVR was found to outperform Linear Regression in terms of prediction accuracy.

## Technologies Used

- Python (via Google Colab)
- pandas, numpy for data processing
- scikit-learn for machine learning
- matplotlib, seaborn for data visualization

## Results

Both Linear Regression and SVR models were trained and evaluated. SVR demonstrated better performance in capturing nonlinear patterns in price fluctuations and achieved lower prediction errors on the test set.

Visualizations of predicted vs. actual prices are included in the notebook to show the model's effectiveness across commodities.

## Future Work

- Incorporate more features such as region, crop yield, or market demand indicators
- Explore additional regression models like XGBoost and LSTM
- Deploy the model as an API or integrate it into a web interface for broader access
- Automate monthly data updates and retraining
