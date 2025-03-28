# Machine Learning-Guided Mapping Sleep-Promoting Volatiles in Aromatic Plants

## Project Description
Project Description:
This repository presents an advanced machine learning pipeline for identifying sleep-promoting volatile organic compounds (VOCs) from aromatic plants. 
![image](https://github.com/user-attachments/assets/967c2866-bf5b-4832-9524-75947ef89c8a)


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

- GABAA.csv: Main dataset with SMILES strings and class labels
- plant.xlsx: New compounds for prediction
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
