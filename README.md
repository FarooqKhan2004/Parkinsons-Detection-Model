# Early Detection of Parkinson’s Disease from Voice Features Using Logistic Regression

This repository contains the code and materials for the project:

> **Early Detection of Parkinson’s Disease from Voice Features Using Logistic Regression**  
> Farooq Khan, Virginia Tech

The goal of this project is to build an interpretable, reproducible logistic regression model that predicts Parkinson’s disease (PD) status from sustained phonation voice recordings in the UCI Parkinson’s dataset. The focus is on:

- Subject-wise data splits to avoid speaker leakage  
- Standardized feature scaling  
- L2-regularized logistic regression  
- Systematic decision-threshold analysis  
- Clear, reproducible experiments and figures

## Repository Structure

- `notebooks/`
  - `parkinsons_logreg.ipynb` – main Google Colab notebook with the full pipeline:
    - data loading and preprocessing  
    - subject-wise splits  
    - feature scaling  
    - model training and hyperparameter tuning  
    - threshold analysis and evaluation  
    - figure generation (ROC, PR, threshold curves, confusion matrix)
- `subject_splits.json` – list of subject IDs used in each split (train/val/test)
- `requirements.txt` – Python dependencies
- `LICENSE` – MIT license for this repository

> Note: If your notebook currently lives at the repo root, you can either move it into `notebooks/` or adjust the structure above.

## Dataset

This project uses the **UCI Parkinson’s Disease** dataset (sustained phonation voice recordings). Each row corresponds to a single recording; the `name` column encodes the speaker identity.

You must download the dataset manually from the UCI repository (or your course-provided source) and place it at a path used in the notebook, e.g.:

- `data/parkinsons.data`

## Reproducing the Experiments

### 1. Set up environment

```bash
python -m venv .venv
source .venv/bin/activate  # on Windows: .venv\Scripts\activate
pip install -r requirements.txt
