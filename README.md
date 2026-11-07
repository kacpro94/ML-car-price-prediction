# Used-Car Price Prediction

## Bachelor's thesis

**Title:** Comparing the Effectiveness of Machine Learning Algorithms and Econometric Methods in Modeling Used-Car Prices on the Secondary Market  
**Author:** Kacper Prorok  
**Field of study:** Computer Science and Econometrics  
**Supervisor:** Dr. Artur Machno  
**Location and year:** Kraków, 2025

## Project overview

This project compares machine-learning algorithms and econometric methods for modeling used-car prices on the secondary market. The analysis covers data cleaning and exploratory data analysis, feature preparation, model fitting and diagnostics, hyperparameter tuning, and a comparison of prediction errors.

## Repository contents

- [`EDAlast.ipynb`](./EDAlast.ipynb) — data cleaning, feature preparation, exploratory analysis, model diagnostics, and the final model comparisons.
- [`ParameterTuning.ipynb`](./ParameterTuning.ipynb) — hyperparameter searches for Ridge regression, Random Forest, MLP, and XGBoost models, including experiments with the original, log-transformed, and square-root-transformed target.
- [`requirements.txt`](./requirements.txt) — pinned Python dependencies for running both notebooks.
- [`otomoto_offers_eng_23-04-2023.csv`](./otomoto_offers_eng_23-04-2023.csv) — the raw source dataset.
- [`dane_po_transformacji.csv`](./dane_po_transformacji.csv) — the processed dataset used by the parameter-tuning notebook.

## Running the notebooks

The project uses Python 3.11. From the project folder, create a virtual environment:

```bash
python3.11 -m venv .venv
source .venv/bin/activate
```

On Windows PowerShell, use `py -3.11 -m venv .venv` and activate it with `.venv\Scripts\Activate.ps1`.

With the environment active, install the pinned dependencies:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

Start JupyterLab with:

```bash
jupyter lab
```

Both notebooks read their CSV files from the project folder using relative paths. Run `EDAlast.ipynb` to repeat the cleaning and EDA workflow; it can recreate `dane_po_transformacji.csv`. `ParameterTuning.ipynb` uses that processed file and can also be run directly with the copy already included here.

Both notebooks contain saved cell outputs from previous runs. These outputs are retained as part of the project and may not correspond to a fresh run in your environment.
