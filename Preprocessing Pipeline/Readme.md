# IT2011 Group Assignment - Progress Review I: Diabetes Dataset Preprocessing

## Overview
This project focuses on preprocessing and exploratory data analysis (EDA) of the "Healthcare-Diabetes.csv" dataset, a collection of medical records used to predict diabetes outcomes. The goal is to clean the data, handle preprocessing tasks, and perform EDA to prepare it for machine learning models, with a specific addition of an age binning column to the final preprocessed dataset.

## Dataset Details
- **Source**: "Healthcare-Diabetes.csv" (located at `D:\\SLIIT\\Y2S1\\AI & ML\\Project\\senal\\`).
- **Description**: Contains features such as `Pregnancies`, `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI`, `DiabetesPedigreeFunction`, `Age`, and `Outcome` (target variable indicating diabetes presence).
- **Task**: Clean and preprocess the data, normalize features, analyze importance and variance, and add an `Age_Binned` column for categorical age groups.

## Group Members and Roles
- IT24102643(Anuraheesara U.A.S.): Handling missing data (imputation of zeros in numerical columns).
- IT24102651(Disanayaka R M K S): Handling duplicates (removal of duplicate rows).
- IT24102649(Liyanage D C J): Outlier removal (using IQR method on numerical columns).
- IT24102605(Punchihewa S.D): Normalization/scaling (using MinMaxScaler on numerical features).
- IT24102575(Madhusanka S.P): Feature engineering (feature importance analysis using mutual information).
- IT24103838(Dissanayaka D. M. H.): Feature engineering (variance analysis via correlation matrix).
- Extra Member: Feature discretization (adding `Age_Binned` column to the final preprocessed dataset).

## Repository Structure
- `data/`
  - `raw/`: Original `Healthcare-Diabetes.csv` file.
- `notebooks/`
  - `group_pipeline_healthcare.ipynb`: Integrated pipeline combining all preprocessing steps.
- `results/`
  - `eda_visualizations/`: Plots (e.g., `age_binning_distribution.png`).
  - `outputs/`: Processed datasets (e.g., `final_preprocessed.csv`, `final_preprocessed_with_age_binned.csv`).

## How to Run the Code
1. **Install Dependencies**:
   - Run `pip install pandas numpy seaborn matplotlib scikit-learn` in your terminal or Anaconda prompt.
2. **Set Up Environment**:
   - Ensure Python 3.13.5 (or a compatible version) is used.
   - Activate your virtual environment (e.g., `venv\Scripts\activate` on Windows).
3. **Update Paths**:
   - Edit the `pd.read_csv()` call in the notebook to point to your local dataset path (e.g., `D:\\SLIIT\\Y2S1\\AI & ML\\Project\\senal\\Healthcare-Diabetes.csv`) if it differs.
4. **Execute**:
   - Open `group_pipeline_healthcare.ipynb` in Jupyter Notebook or a compatible environment (e.g., VS Code with Jupyter extension) and run all cells.
5. **View Results**:
   - Check `results/eda_visualizations/` for plots and `results/outputs/` for processed files.

## Preprocessing Pipeline

1. **IT24102643(Anuraheesara U.A.S.): Handling Missing Data**
   - Replaces zero values in `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, and `BMI` with `NaN`, then fills with column means.

2. **IT24102651(Disanayaka R M K S): Handling Duplicates**
   - Removes duplicate rows from the dataset.

3. **IT24102605(Punchihewa S.D): Outlier Removal**
   - Identifies and removes outliers using the IQR method across all numerical columns.

4. **IT24102575(Madhusanka S.P): Normalization/Scaling**
   - Normalizes numerical columns to a [0, 1] range using MinMaxScaler.

5. **IT24102575(Madhusanka S.P): Feature Engineering (Feature Importance Analysis)**
   - Computes feature importance using mutual information for numerical columns.

6. **IT24103838(Dissanayaka D. M. H.): Feature Engineering (Variance Analysis)**
   - Estimates explained variance via the average absolute correlation of numerical columns.

7. **Extra Member : Feature Discretization (Age Binning)**
   - Adds a new `Age_Binned` column to the `final_preprocessed.csv` file, binning `Age` into groups: `0-20`, `20-30`, `30-40`, `40-50`, `50-60`, `60+`.
   - Retains all original columns and saves the result as `final_preprocessed_with_age_binned.csv`.

## Outputs
- **Console Output**: Displays shapes, missing value counts, duplicates, feature importance, variance analysis, and value counts for `Age_Binned`.
- **Visualizations**:
  - `age_binning_distribution.png`: A countplot showing the distribution of age groups.
  - Saved in `results/eda_visualizations/`.
- **Saved Files**:
  - `final_preprocessed.csv`: The preprocessed dataset before binning, saved in `D:\\SLIIT\\Y2S1\\AI & ML\\Project\\`.
  - `final_preprocessed_with_age_binned.csv`: The dataset with the added `Age_Binned` column, saved in `D:\\SLIIT\\Y2S1\\AI & ML\\Project\\`.

