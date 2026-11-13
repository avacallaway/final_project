# Customer Churn Analysis

This repository is an organized project that demonstrates how to perform an EDA, do feature engineering, and create valuable models on customer churn data for reproducibility. It includes a minimal end-to-end workflow for detecting whether a customer will churn using scikit‑learn.

## Purpose

The purpose of this project is to evaluate if a customer will churn based on their measured variables. It takes a realistic business setting and demonstrates how to perform data cleaning, exploratory analysis, feature selection, and predictive modeling to gain insight into real-world subscription behavior.

## Project layout

```
.
├── main.py                 # Entry point that runs the entire pipeline
├── requirements.txt        # Python dependencies
├── data/
│   ├── processed/          # Created after running the pipeline
│   └── raw/
|       └── test.csv
|       └── train.csv
├── notebooks/
|   └── customer_churn_analysis.ipynb
└── src/
    ├── data/
    │   ├── load_data.py
    │   ├── preprocess.py
    │   └── split_data.py
    ├── features/
    │   └── build_features.py
    ├── models/
    │   ├── train_model.py
    │   ├── dumb_model.py
    │   └── knn_model.py
    ├── utils/
    │   └── helper_functions.py
    └── visualization/
        ├── eda.py
        └── performance.py
```

`main.py` imports the modules inside `src/` and executes them to reproduce the analysis and results. Jupyter notebooks are provided only for prototyping and exploration

Note that some directories such as `data/external/`, `src/utils/` and `tests/` may be empty.

## Running the project

Install the dependencies and run the pipeline. You should use the versions of the dependencies as specified by the requirements file:

```bash
conda create -n customer_churn --file requirements.txt
conda activate customer_churn
python main.py
```

This will load the dataset, perform basic feature engineering, train a simple model and produce visualizations similar to those in the notebook.
The cleaned data will be written to `data/processed/` and all plots will be displayed interactively.
