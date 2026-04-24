# UK Company Insolvency Regression Model

## Overview

The project investigates how macroeconomic conditions influence UK insolvency rates using data from the UK Insolvency Service and the Office for National Statistics (ONS).

A structured regression pipeline was built to analyse company insolvencies. The same framework was then applied to individual insolvencies, allowing comparison of how economic factors affect different types of financial distress.

## Approach

The project follows a modular and reproducible data pipeline:

- Cleaning raw datasets individually (handling inconsistent formats and structures)
- Aligning monthly and quarterly data into a consistent time series
- Merging all predictors into a unified dataset
- Creating lagged variables (12 and 24 months) to capture delayed economic effects
- Creating event dummy variables for COVID-19, Brexit and the energy crisis
- Building regression models using OLS
- Applying diagnostic tests (Durbin–Watson, Breusch–Pagan, VIF)
- Using HAC robust standard errors to address autocorrelation and heteroskedasticity

The pipeline was first developed for company insolvencies and then repeated for individual insolvencies, enabling direct comparison between firm-level and household financial behaviour.

## Key Findings

- Lagged inflation (12–24 months) is one of the strongest predictors of company insolvency  
- Electricity prices reflect short-term cost pressures affecting businesses  
- GDP shows both immediate and delayed effects on insolvency rates  
- Policy interventions during COVID-19 suppressed insolvencies despite economic stress  
- Event dummy variables captured structural breaks caused by COVID-19, Brexit and the energy crisis  
- Company and individual insolvencies respond differently to macroeconomic conditions  

## Project Structure

- src/ Python scripts for cleaning, feature engineering and modelling
- notebooks/ Notebooks for pipeline and final model
- data/ Cleaned datasets

## Technologies

Python, pandas, NumPy, statsmodels, matplotlib, Jupyter Notebook

## Data Sources

Raw datasets are not included in this repository due to file size. The repository includes cleaned/intermediate datasets used for modelling.

Original data sources:

- Company insolvency data:  
  https://www.gov.uk/government/statistics/company-insolvencies-february-2025  

- Individual insolvency data:  
  https://www.gov.uk/government/statistics/individual-insolvencies-february-2025  

- Macroeconomic indicators:  
  Office for National Statistics (ONS)
