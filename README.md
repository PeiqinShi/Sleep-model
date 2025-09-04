# Machine Learning-Guided Mapping Sleep-Promoting Volatiles in Aromatic Plants

## Project Description
Project Description:
This repository presents an advanced machine learning pipeline for identifying sleep-promoting volatile organic compounds (VOCs) from aromatic plants. 
![image](https://github.com/user-attachments/assets/2fbe4d84-0f63-40aa-b340-3f0d605319bc)



## Installation

## Dependency
The code has been tested in the following environment:

|  Package    | Version  |
|  ----  | ----  |
| Python  | 3.8.16 |
| conda  | 23.5.0 |
| RDKit  | 2023.3.1 |

# How to Use

## Installation
```python
# Create a new environment, here is conda as an example
conda create --name sleep_model python=3.8.10

# Activate the newly created environment
conda activate sleep_model

# Installation package
pip install sleep_model==0.0.11
pip install imblearn

# Suggest the pipeline of Jupyter notebook [optional, recommended]
conda install jupyter notebook
conda install ipykernel 
python -m ipykernel install --user --name sleep_model --display-name   "sleep_model"
jupyter notebook

# Method2
# Use the yaml environment file on the GitHub homepage to directly copy the current environment
conda env create -f environment.yaml -n sleep_model
conda activate sleep_model
conda install jupyter notebook
conda install ipykernel
python -m ipykernel install --user --name sleep_model --display-name   "sleep_model"
jupyter notebook
```
```
# Usage
Data Preparation
Place your input files in the data/ directory:

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
