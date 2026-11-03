# Exploring Housing Prices with Python

This project is a hands-on notebook for practicing data analysis and introductory
machine learning with housing data.

## Learning goals

- Load an Excel dataset with pandas.
- Inspect columns, data types, and missing values.
- Visualize numerical and categorical features.
- Encode categorical data for machine learning.
- Compare regression models and evaluation metrics.
- Think critically about how data preparation affects model evaluation.

## Getting started

Install the dependencies:

```bash
python -m pip install pandas openpyxl numpy matplotlib seaborn scikit-learn jupyter
```

Then launch Jupyter, open `house_pricing_predicts.ipynb`, and run the notebook
cells in order. The notebook expects `HousePricePrediction.xlsx` in the same
folder.

## Files

- `house_pricing_predicts.ipynb` — guided analysis and model experiments
- `HousePricePrediction.xlsx` — dataset
- `correlation_heatmap.png` — numerical feature visualization
- `cat_feat_distribution.png` — categorical feature visualization

## Before interpreting the scores

Some rows in the spreadsheet do not have a known `SalePrice`. The notebook
currently fills those missing prices with an average before training. That is a
useful opportunity to explore a key modeling lesson: missing target values
should generally not be treated as real labels. For a meaningful validation
score, evaluate only on rows with known prices and document the split and metric.

## Ideas to extend the project

- Compare models using the same train/validation split.
- Add a preprocessing pipeline for missing feature values and categorical data.
- Report MAE, RMSE, and R² alongside MAPE.
- Record the dataset source, license, and any assumptions.
