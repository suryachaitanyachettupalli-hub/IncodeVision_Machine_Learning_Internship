# House Price Prediction Using Linear Regression

This repository contains an introductory machine-learning project that predicts house prices using a Linear Regression model.

## Files
- `house_price_prediction_simple.ipynb` — notebook with data inspection, cleaning, EDA, preprocessing, training, evaluation, and plots.
- `data.csv` — dataset used by the notebook.

## Run locally
1. Install Python 3.10 or newer.
2. Install dependencies: `pip install -r requirements.txt`
3. Open the notebook in Jupyter Notebook, JupyterLab, or VS Code.
4. Run all cells from top to bottom. Keep `data.csv` in the same directory as the notebook.

## Workflow
- Inspect missing values and duplicate rows.
- Exclude zero-price targets and two records with both bedroom and bathroom counts equal to zero.
- Engineer `house_age`; treat extreme target values using a 3 × IQR rule.
- Split into training and test sets.
- Fit numeric scaling and one-hot encoding on the training data using a Scikit-learn pipeline.
- Train Linear Regression and evaluate with MSE, RMSE, and R².

## Results
The recorded run produced an R² score of approximately 0.782 on the held-out test split. Results can vary with changes to the dataset, preprocessing, or library versions. This score is not a guarantee of performance on other housing data.

## Limitations
This is a baseline model. The IQR filter may exclude legitimate high-value homes, and Linear Regression may not capture nonlinear relationships. More models and error analysis should be compared before using predictions in a real-world setting.
