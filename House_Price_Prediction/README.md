# House Price Prediction with Linear Regression

> **IncodeVision Machine Learning Internship · Task 02**

A supervised machine learning project that builds a baseline regression
model to estimate house prices from property characteristics and
location-related features.

## Project Overview

The goal of this project is to practise an end-to-end regression
workflow: inspecting a dataset, cleaning and preparing features,
exploring patterns, training a model, and evaluating its predictions on
held-out data.

## Highlights

-   Dataset inspection and data-quality checks using **Pandas** and
    **NumPy**
-   Exploratory data analysis (EDA) with **Matplotlib** and **Seaborn**
-   Feature engineering, including a `house_age` feature
-   Numeric preprocessing and one-hot encoding within a **Scikit-learn
    pipeline**
-   Linear Regression model training and test-set evaluation
-   Actual-versus-predicted visualization

## Tech Stack

-   Python
-   Pandas and NumPy
-   Matplotlib and Seaborn
-   Scikit-learn
-   Jupyter Notebook

## Repository Contents

  ---------------------------------------------------------------------------
  File                                    Description
  --------------------------------------- -----------------------------------
  `house_price_prediction_simple.ipynb`   Notebook containing data
                                          inspection, cleaning, EDA,
                                          preprocessing, model training,
                                          evaluation, and visualizations

  `data.csv`                              Dataset used by the notebook

  `requirements.txt`                      Python package dependencies

  `README.md`                             Project documentation
  ---------------------------------------------------------------------------

## Workflow

1.  **Inspect the data** --- review the dataset structure, summary
    statistics, missing values, and duplicate rows.
2.  **Clean and prepare** --- remove non-positive target prices and
    records where both bedroom and bathroom counts are zero; review
    columns and data types.
3.  **Explore the data** --- visualize price distributions and
    relationships between selected features.
4.  **Engineer features** --- derive `house_age` from the date and year
    built.
5.  **Prepare model inputs** --- use numeric features and
    one-hot-encoded `statezip`; fit preprocessing on the training data
    through a pipeline.
6.  **Train the model** --- fit a Scikit-learn `LinearRegression`
    estimator.
7.  **Evaluate** --- calculate Mean Squared Error (MSE), Root Mean
    Squared Error (RMSE), and the coefficient of determination (R²).
8.  **Visualize predictions** --- compare actual and predicted prices.

## Results

Recorded results from the notebook's held-out test split:

  Metric                                        Result
  -------------------------------- -------------------
  Mean Squared Error (MSE)           15,378,916,831.64
  Root Mean Squared Error (RMSE)            124,011.76
  R²                                             0.782

The **R² score of 0.782** means the model explains approximately 78.2%
of the variation in target prices in this particular test set. RMSE is
expressed in the same units as the target price.

These values describe this run and test split; they are not a guarantee
of performance on other datasets or housing markets.

## Run Locally

### 1. Clone the repository

If you are viewing this project inside the IncodeVision internship
repository, clone the parent repository and move into this task folder:

``` bash
git clone https://github.com/suryachaitanyachettupalli-hub/IncodeVision_Machine_Learning_Internship.git
cd IncodeVision_Machine_Learning_Internship/Task-02-House-Price-Prediction
```

### 2. Create and activate a virtual environment (recommended)

**Windows PowerShell:**

``` powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**macOS / Linux:**

``` bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

``` bash
python -m pip install -r requirements.txt
```

### 4. Run the notebook

Open the notebook in Jupyter Notebook, JupyterLab, or VS Code. Keep
`data.csv` in the same directory as the notebook, then run the cells
from top to bottom.

## Notes and Limitations

-   This is a baseline model intended for learning and demonstration,
    not a property valuation service.
-   The notebook uses a 3 × IQR rule to filter extreme target-price
    values. Some removed observations could represent legitimate
    high-value properties.
-   Linear Regression may not capture nonlinear relationships or complex
    interactions between features.
-   Results depend on the dataset, feature choices, preprocessing, and
    train/test split.
-   Before sharing the dataset publicly, confirm that its source and
    license permit redistribution. If redistribution is not permitted,
    omit `data.csv` and document how to obtain it.

## Possible Next Steps

-   Compare performance with a `DummyRegressor` baseline.
-   Try tree-based models such as Random Forest or Gradient Boosting.
-   Analyze prediction errors across different price ranges.
-   Compare feature sets and document how each change affects test
    performance.

------------------------------------------------------------------------

**Project type:** Regression · **Model:** Linear Regression ·
**Context:** IncodeVision Machine Learning Internship
