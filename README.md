# Prediction of Wheat Yield in Faisalabad District Using Regression Analysis

---

## Project Overview

This project predicts **wheat yield** in Faisalabad district, Punjab, Pakistan, using **historical data on area, production, and fertilizer usage**.  

The analysis explores how **Area and fertilizers (Nitrogen, Phosphate, Potash)** impact wheat yield and evaluates different regression models:

- Linear Regression  
- Ridge Regression  
- Polynomial Ridge Regression  

Both **single fertilizer models** and **combined fertilizers (N+P+K)** are tested to understand their individual and combined effects.

---

## Data Source

All historical data was collected from:

- **Pakistan Bureau of Statistics** ([http://www.pbs.gov.pk](http://www.pbs.gov.pk))  
- **National Fertilizer Development Centre, Islamabad**

Data includes:

- Wheat **area** and **production** (2011-12 to 2021-22)  
- Fertilizer consumption (**Nitrogen, Phosphate, Potash**)  

---

## Dataset Sample

| Year | Area (ha) | Production (t) | Yield (t/ha) | N | P | K |
|------|------------|----------------|---------------|---|---|---|
| 2018-19 | 6484 | 18362 | 2.832 | 2306.95 | 276.83 | 69.21 |
| 2019-20 | 6481 | 19347 | 2.985 | 2274.15 | 272.90 | 68.22 |
| 2020-21 | 6709 | 20842 | 3.107 | 2504.00 | 300.48 | 75.12 |
| 2021-22 | 6305 | 19417 | 3.079 | 2500.50 | 300.10 | 75.00 |

---

## Models Implemented

1. **Area + Nitrogen (N)** – Polynomial Ridge Regression  
2. **Area + Phosphate (P)** – Polynomial Ridge Regression  
3. **Area + Potash (K)** – Polynomial Ridge Regression  
4. **Area + N + P + K** – Polynomial Ridge Regression  

**Regression metrics calculated for each model:**

- R² Score  
- Mean Absolute Error (MAE)  
- Mean Squared Error (MSE)  
- Root Mean Squared Error (RMSE)  
- Mean Absolute Percentage Error (MAPE)  

---

## Results

| Model | Predicted 2022-23 (t/ha) | Predicted 2023-24 (t/ha) | R² | MAE | RMSE | MAPE |
|-------|-----------------|-----------------|-----|-----|------|------|
| **Area + N** | 3.033 | 3.019 | 0.8998 | 0.0283 | 0.0346 | 0.95% |
| **Area + P** | 3.024 | 3.007 | 0.8772 | 0.0324 | 0.0383 | 1.08% |
| **Area + K** | 3.025 | 3.008 | 0.8749 | 0.0326 | 0.0386 | 1.09% |
| **Area + N+P+K** | 2.803 | 2.722 | 0.9967 | 0.0052 | 0.0062 | 0.18% |

> **Observation:**  
> - Single nutrient models, especially **Area + Nitrogen**, produce predicted yields closer to the **actual 2022-23 yield of 3.304 t/ha**.  
> - Combined nutrient model (N+P+K) fits training data almost perfectly but underpredicts new years due to **polynomial interactions + small dataset + regularization**.

---

## Visualization

- Actual vs predicted yield plots for each model  
- Predictions for 2022-23 and 2023-24 highlighted in plots  



