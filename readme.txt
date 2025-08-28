# Thesis Project Repository

This repository contains the code, data, and outputs related to the MSc thesis on streamflow prediction in large river basins using LSTM models.  
It includes exploratory analysis, model training results, evaluation metrics, and interpretability experiments.

---

##  Folder Structure

### 1. `Dataset/`
- Contains the data used for modeling.
- Includes hydrological, meteorological, and static attributes from the CABra dataset.

### 2. `eda_outputs/`
- Stores outputs from exploratory data analysis (EDA).
- Includes descriptive statistics, plots of input features, and distribution visualizations.

### 3. `lstm_outputs (all catchments)/`
- Contains the model outputs for the multi-catchment experiments.
- Includes training/validation/test results, best model checkpoints, and performance plots.

### 4. `lstm_outputs (ID31)/`
- Contains the model outputs for the Catchment 31.
- Includes incremental feature experiments, ablation tests, and corresponding performance figures.

### 5. `result_output/`
- Contains the relationship between performance metrics(KGE, NSE, CCC) and catchmnet attributes with p value.

### 6. `thesis_pictures/`
- Stores finalized figures used in the thesis 
- Includes EDA charts, performance evaluation plots, and interpretability visualizations.

---

## Jupyter Notebooks

### `All catchments (including IG analysis).ipynb`
- Main notebook for multi-catchment LSTM modeling.  
- Includes:
  - Data preprocessing and sliding window generation.
  - Lookback sensitivity analysis.
  - Hyperparameter tuning via grid search.
  - Model training across multiple catchments.
  - Performance evaluation.
  - Integrated Gradients (IG) interpretability analysis.

### `Catchment 31 (not include IG).ipynb`
- Notebook for **single-basin experiments (ID=31).  
- Includes:
  - Lookback sensitivity analysis.
  - Hyperparameter tuning via grid search.
  - Incremental feature experiments and ablation tests.  

### `Catchment 31 (Catchment 31 ).ipynb`
- Notebook for IG analysis of Catchment 31 .

### `Data exploration.ipynb`
- Notebook for exploratory data analysis (EDA).  
- Generates summary statistics, distribution plots.

### `Evaluation Metrics Result Analysis.ipynb`
- Notebook for*model performance evaluation.  
- Explore the relationship between performance metrics(KGE, NSE, CCC) and catchmnet attributes

### `Integrated Gradients analysis (Catchment 31).ipynb`
- Notebook for IG interpretability analysis of Catchment 31.  
- Produces feature importance plots (bar charts, and heatmaps).

---

##  How to Use
1. Prepare the dataset in `Dataset/` (CABra inputs).
2. Run `Data exploration.ipynb` for feature statistics and sanity checks.
3. Train models:
   - For multi-catchment :  use `All catchments.ipynb`.
   - For single-catchment  : use `Catchment 31.ipynb`.
4. Analyze results in `Evaluation Metrics Result Analysis.ipynb`.
5. Collect final plots and tables from `result_output/` and `thesis_pictures/`.

---

##  Notes
- The single-catchment analysis (ID31) serves as a methodological starting point, while the multi-catchment experiments form the main focus of the thesis.  
- All results (metrics, plots, and IG outputs) are stored for reproducibility and reporting.