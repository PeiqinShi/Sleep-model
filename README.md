# GABAA Receptor Modulator Prediction using Stacked Ensemble Learning

## Project Description
This repository contains a machine learning pipeline for predicting GABAA receptor modulators using:
- Molecular fingerprinting (MACCS keys and RDKit descriptors)
- Feature selection with Variance Threshold
- Stacked ensemble modeling combining Random Forest, SVM, and XGBoost predictions

## Features
- Dual molecular featurization (MACCS fingerprints and RDKit descriptors)
- Variance-based feature selection
- Two-level stacked ensemble architecture
- Pretrained models for immediate inference

## Installation

### Conda Environment Setup
First create the environment using the provided `environment.yaml`:
```bash
conda env create -f environment.yaml -n sleep-model
conda activate sleep-model

Usage
Data Preparation
Place your input files in the data/ directory:

GABAA.csv: Main dataset with SMILES strings and class labels
plant.xlsx: New compounds for prediction

File Structure
├── data/                   # Input data files
├── data_analysis/          # Input data files
├── models/                 # Pretrained model files
│   ├── rf_maccs_model.pkl
│   ├── rf_rdkit_model.pkl
│   ├── svm_maccs_model.pkl
│   ├── xgb_maccs_model.pkl
│   └── stacking_model.pkl
├── notebooks/              # Jupyter notebooks for exploration
├── src/                    # Source code
│   ├── featurization.py    # Feature generation code
│   └── stacking.py         # Ensemble modeling code
├── requirements.txt        # Dependency list
└── README.md               # This file
