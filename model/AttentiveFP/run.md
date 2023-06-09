```
chemprop_train --data_path ../../data/refined_gabaa.csv  --dataset_type classification --split_type scaffold_balanced --metric auc --extra_metrics ba f1 mcc --split_sizes 0.7 0.15 0.15 --save_dir result_scaffold_1
```

```python
chemprop_predict --test_path data/test.csv --checkpoint_path MPNN/result_scaffold_1/fold_0/model_0/model.pt --preds_path MPNN/result_scaffold_1/result_scaffold_test_pred.csv
```

chemprop_train --data_path mpnn.csv  --dataset_type classification  --split_type cv --num_folds 5 --metric auc --extra_metrics accuracy pre rec  --seed 42 --save_dir result_random

chemprop_train --data_path ../../data/refined_gabaa.csv  --dataset_type classification --split_type scaffold_balanced --metric f1 --extra_metrics auc  ba  mcc --split_sizes 0.56 0.14 0.3  --seed 500 --save_dir result_scaffold_4



chemprop_train --data_path ../../data/refined_gabaa.csv  --dataset_type classification  --metric f1 --extra_metrics auc  ba  mcc --split_sizes 0.56 0.14 0.3 --save_dir result_random_0

--separate_test_path data/test.csv --separate_val_path data/val.csv

--split_type scaffold_balanced
