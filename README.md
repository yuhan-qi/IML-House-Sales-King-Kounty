# King County House Sales — Price Prediction

Predicting house sale prices in King County, WA using multiple linear regression and XGBoost, and comparing model performance across two different target formulations.

## Approach

- **Exploratory analysis** — visualized relationships between house features (square footage, bedrooms, location, condition, etc.) and sale price
- **Multiple linear regression** — two models, predicting:
  - raw sale `price`
  - `price_per_sqft_living` (price normalized by living area, to reduce the influence of house size on the target)
- **XGBoost** — the same two target formulations, to compare a gradient-boosted tree model against the linear baseline

## Why compare two target formulations

Predicting raw price directly can be dominated by house size; normalizing to price-per-square-foot isolates how much *location, condition, and other features* affect price independent of size. Comparing both linear regression and XGBoost against each target shows whether a more flexible, non-linear model actually improves on a standard linear baseline for this data.

## Files

| File | Description |
|---|---|
| `kc_house_data_description_plots.R` | Exploratory data analysis and visualization |
| `Multiple Linear Regression taking price as dependent variable.R` | Linear regression, predicting raw price |
| `Multiple Linear Regression taking price_per_sqft_living as dependent variable.R` | Linear regression, predicting price per sqft |
| `XGBoost taking Price as dependent variable.R` | XGBoost, predicting raw price |
| `XGBoost taking Price_per_sqft_living as dependent variable.R` | XGBoost, predicting price per sqft |

## Data

[House Sales in King County, USA](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction) (Kaggle)

## Tech stack

R (lm, xgboost)

## License

MIT
