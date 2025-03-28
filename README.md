# Machine Learning-Guided Mapping Sleep-Promoting Volatiles in Aromatic Plants

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
```

## Usage
Data Preparation
Place your input files in the data/ directory:

-GABAA.csv: Main dataset with SMILES strings and class labels
-plant.xlsx: New compounds for prediction
```
File Structure
├── data/                   # Input data files
├── data_analysis/          # Data processing and analysis
├── models/                 # Pretrained base model files for Stacking model training
│   ├── RF/
│   │   ├── rf_MACCSkeys_random_0.ipynb
│   │   ├── rf_RDkit_random_0.ipynb
│   ├── SVM/
│   │   ├── svm_MACCSkeys_random_3.ipynb
│   ├── XGB/
│   │   ├── xgb_MACCSkeys_random_0.ipynb
│   └── stacking_predict.ipynb
├── environment.yaml        
└── README.md              
```
