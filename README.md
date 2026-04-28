# multiclass-classification-and-used-car-price-prediction

Supervised learning project combining multiclass handwritten character classification with **KNN**, **SVM**, and **Decision Trees**, and used-car price prediction with **linear regression**. The repository includes data preprocessing, hyperparameter tuning, model evaluation, and visual analysis.

## Project overview

This repository contains two complementary machine learning tasks:

1. **Multiclass classification**
   - Dataset: handwritten character samples from **EMNIST**
   - Goal: classify five uppercase handwritten letters
   - Models: **K-Nearest Neighbors**, **Support Vector Machines**, and **Decision Trees**
   - Additional work: dimensionality reduction with **UMAP**, confusion matrices, and decision-boundary visualization

2. **Regression**
   - Dataset: used-car records from **CarDekho**
   - Goal: predict vehicle selling price from technical and categorical features
   - Model: **Linear Regression**
   - Additional work: data cleaning, missing-value imputation, categorical encoding, scaling, and exploratory data analysis

## Main objectives

- Compare different supervised learning algorithms on the same classification problem
- analyze how hyperparameters affect model behavior and performance
- visualize decision boundaries in a low-dimensional space
- build a complete regression workflow on a real tabular dataset
- evaluate model performance using appropriate metrics

## Repository structure

```text
.
├── .gitignore
├── Car details v3.csv
├── EMNIST_sample.pickle
├── M2_891_20252_PEC3_Victor_Suesta_Arribas.ipynb
├── M2_891_20252_PEC3_Victor_Suesta_Arribas.html
├── environment_uoc20252pec3.yml
└── README.md
````

## Files description

* **Car details v3.csv**
  Tabular dataset used for the regression task on used-car price prediction.

* **EMNIST_sample.pickle**
  Preprocessed handwritten character dataset used for the multiclass classification task.

* **M2_891_20252_PEC3_Victor_Suesta_Arribas.ipynb**
  Main notebook containing the full workflow: loading data, preprocessing, exploratory analysis, model training, hyperparameter tuning, evaluation, and written conclusions.

* **M2_891_20252_PEC3_Victor_Suesta_Arribas.html**
  Exported HTML version of the notebook, including code, outputs, figures, and comments.

* **environment_uoc20252pec3.yml**
  Conda environment file with the required dependencies to reproduce the project.

## Methods used

### Classification task

* **UMAP** for 2D projection
* **KNN**

  * baseline model
  * hyperparameter tuning for `n_neighbors`
* **SVM**

  * RBF kernel
  * hyperparameter tuning for `C` and `gamma`
* **Decision Tree**

  * baseline model
  * tuning of `max_depth` and `min_samples_split`

### Regression task

* missing-value imputation
* extraction and cleaning of numerical information from raw text fields
* categorical encoding with one-hot encoding
* feature scaling with `StandardScaler`
* **Linear Regression**
* evaluation with **MAPE**

## Key results

### Classification

The classification task achieved strong performance across the three models:

* **Best SVM test accuracy:** `0.9706`
* **Best KNN test accuracy:** `0.9686`
* **Tuned Decision Tree test accuracy:** `0.9626`

Among the evaluated models, **SVM** provided the best overall classification performance on the EMNIST projection.

### Regression

For the used-car price prediction task:

* **Linear Regression test MAPE:** `44.38%`

This result works as a baseline and suggests that the regression problem may benefit from more flexible non-linear models in future iterations.

## How to run

### 1. Clone the repository

```bash
git clone https://github.com/Suesta/multiclass-classification-and-used-car-price-prediction.git
cd multiclass-classification-and-used-car-price-prediction
```

### 2. Create the Conda environment

```bash
conda env create -f environment_uoc20252pec3.yml
conda activate uoc20252pec3
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Then open:

```text
M2_891_20252_PEC3_Victor_Suesta_Arribas.ipynb
```

## Libraries and tools

The project mainly uses:

* **Python**
* **pandas**
* **numpy**
* **matplotlib**
* **seaborn**
* **scikit-learn**
* **umap-learn**
* **Jupyter Notebook**

## Notes

* The notebook contains both the code and the interpretation of the results.
* The HTML file is included for quick review without running the notebook.
* The repository is intended as a compact portfolio project showing practical work on supervised learning for both **classification** and **regression**.

## Author

**Víctor Suesta Arribas**
