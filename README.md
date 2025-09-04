# Machine Learning-Guided Mapping Sleep-Promoting Volatiles in Aromatic Plants

## Project Description
This repository provides a machine-learning pipeline for identifying sleep-promoting volatile organic compounds (VOCs) from aromatic plants, including pretrained base models and a stacking predictor for quick inference.
![image](https://github.com/user-attachments/assets/2fbe4d84-0f63-40aa-b340-3f0d605319bc)

## Installation
```
Download miniconda : https://mirrors.tuna.tsinghua.edu.cn/anaconda/miniconda/
```
```
conda create -n sleep python=3.8
pip install sleep-model
```

## Dependency
The code has been tested in the following environment:

|  Package    | Version  |
|  ----  | ----  |
| Python  | 3.8.16 |
| Conda  | 23.5.0 |
| RDKit  | 2023.3.1 |
| Scikit-learn  | 1.0.2 |

# Check the code in detail

### Option A: Conda environment
```bash
conda create -n sleep_model python=3.8
conda activate sleep_model
pip install sleep-model
conda install jupyter notebook
conda install ipykernel
python -m ipykernel install --user --name sleep_model --display-name "sleep_model"
```

### Option B: uv 
```bash
python -m pip install uv
.venv\Scripts\activate  # Windows PowerShell
uv sync
```

## File Structure
```
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
│   │── stacking_predict.ipynb
├── predict_smiles.py 
└── README.md

These four models (rf_MACCSkeys, rf_RDkit, svm_MACCSkeys, xgb_MACCSkeys) are the base models that we use to train the final stacking model.
```

## Predicting


### From PyPI 
```
pip install sleep-model

After installation, a console command is available:

sleep-predict --smiles "CC(=O)OC1=CC=CC=C1C(=O)O"

prediction from CSV
sleep-predict --csv example/input.csv --out example/preds.csv --smiles-column SMILES
```

### As a Python module
```bash
python predict_smiles.py --smiles "CC(=O)OC1=CC=CC=C1C(=O)O"
```
### Batch prediction from CSV
Customize the SMILES column name and encoding when needed (e.g., column `SMILES`):
```bash
python predict_smiles.py --csv example/input.csv --out example/preds.csv --smiles-column SMILES
```

### Notes
- Models and training data are loaded from the installed package resources (project `models/` and `data/GABAA.csv`). Ensure they are present if running from source.

## Troubleshooting
- RDKit/DeepChem wheels can be environment-specific. If installation via `pip` fails, prefer the Conda-based installation.
- If you see a file-not-found error for `models/` or `data/GABAA.csv`, run from the project root or install the project so resources are available in the environment.
- We strongly recommend running this project using Python 3.8.
