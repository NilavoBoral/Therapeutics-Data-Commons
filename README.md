# Prediction of Drug ADMET Properties
Predicting Absorption, Distribution, Metabolism, Excretion and Toxicity (ADMET) Properties of Drug Molecule.

---

Run [ADMET_Properties_Prediction_Using_Descriptors.ipynb](https://github.com/NilavoBoral/Therapeutics-Data-Commons/blob/main/ADMET_Properties_Prediction_Using_Descriptors.ipynb) for `feature extraction`, `model selection` and `predict for test set`.

---
## Results
**Results for test set, after 5 independent runs:**

| **Dataset**                    | Model                     |Matric      | Performance   | Rank |
| ------------------------------ | ------------------------- |:----------:|:-------------:|:----:|
| *`ABSORPTION`*                                                                                 |
| caco2_wang                     | AdaBoostRegressor         | MAE ↓      | 0.321 ± 0.005 | 2    |
| hia_hou                        | BaggingClassifier         | AUROC ↑    | 0.818 ± 0.01  | 9    |
| pgp_broccatelli                | ExtraTreesClassifier      | AUROC ↑    | 0.818 ± 0.0   | -    |
| bioavailability_ma             | RandomForestClassifier    | AUROC ↑    | 0.523 ± 0.011 | -    |
| lipophilicity_astrazeneca      | AdaBoostRegressor         | MAE ↓      | 0.617 ± 0.003 | 8    |
| solubility_aqsoldb             | AdaBoostRegressor         | MAE ↓      | 0.828 ± 0.002 | 4    |
| *`DISTRIBUTION`*                                                                               |
| bbb_martins                    | BaggingClassifier         | AUROC ↑    | 0.811 ± 0.013 | 10   |
| ppbr_az                        | GradientBoostingRegressor | MAE ↓      | 9.185 ± 0.0   | 2    |
| vdss_lombardo                  | AdaBoostRegressor         | SPEARMAN ↑ | 0.627 ± 0.01  | 1    |
| *`METABOLISM`*                                                                                 |
| cyp2d6_veith                   | ExtraTreeClassifier       | AUPRC ↑    | 0.358 ± 0.0   | -    |
| cyp3a4_veith                   | XGBClassifier             | AUPRC ↑    | 0.654 ± 0.0   | -    |
| cyp2c9_veith                   | BaggingClassifier         | AUPRC ↑    | 0.556 ± 0.0   | -    |
| cyp2d6_substrate_carbonmangels | BaggingClassifier         | AUPRC ↑    | 0.605 ± 0.0   | -    |
| cyp3a4_substrate_carbonmangels | XGBClassifier             | AUROC ↑    | 0.556 ± 0.0   | 7    |
| cyp2c9_substrate_carbonmangels | BaggingClassifier         | AUPRC ↑    | 0.281 ± 0.0   | -    |
| *`EXCRETION`*                                                                                  |
| half_life_obach                | AdaBoostRegressor         | SPEARMAN ↑ | 0.438 ± 0.011 | 1    |
| clearance_microsome_az         | AdaBoostRegressor         | SPEARMAN ↑ | 0.518 ± 0.005 | 8    |
| clearance_hepatocyte_az        | ExtraTreesRegressor       | SPEARMAN ↑ | 0.44 ± 0.003  | 1    |
| *`TOXICITY`*                                                                                   |
| herg                           | BaggingClassifier         | AUROC ↑    | 0.715 ± 0.011 | -    |
| ames                           | ExtraTreesClassifier      | AUROC ↑    | 0.716 ± 0.0   | -    |
| dili                           | KNeighborsClassifier      | AUROC ↑    | 0.7 ± 0.0     | -    |
| ld50_zhu                       | ExtraTreesRegressor       | MAE ↓      | 0.636 ± 0.001 | 4    |

---
## Summary
**Using 31 Descriptors & different ML models with Parameter tuning.**

  Regression Problems :-
  
    Rank 1 : 3 Datasets
    Rank 2 : 2 Datasets
    Rank 4 : 2 Datasets
    Rank 8 : 2 Dataset

  Classification Problems :-
  
    Rank 7 : 1 Dataset
    Rank 9 : 1 Dataset
    Rank 10 : 1 Dataset
    Unranked : 10 Datasets
