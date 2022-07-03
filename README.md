# Prediction of Drug ADMET Properties
**Predicting `Absorption`, `Distribution`, `Metabolism`, `Excretion` and `Toxicity` (ADMET) Properties of Drug Molecule**.

**Using `31 Descriptors` & `different ML models with Parameter tuning`.**

Checking correlation between every features for each dataset : [Features_Correlation.ipynb](https://github.com/NilavoBoral/Therapeutics-Data-Commons/blob/main/Features_Correlation.ipynb).

Checking importance of every feature for each dataset : [Feature_Rank.ipynb](https://github.com/NilavoBoral/Therapeutics-Data-Commons/blob/main/Feature_Rank.ipynb).

Model selection for each dataset : [Model selection for all datasets.ipynb](https://github.com/NilavoBoral/Therapeutics-Data-Commons/blob/main/Model%20selection%20for%20all%20datasets.ipynb).

---

## <ins>To reproduce and reuse selected models, follow the steps mentioned below</ins> :

1. Load selected models for regression datasets from [best_model_series.pkl](https://github.com/NilavoBoral/Therapeutics-Data-Commons/blob/main/best_model_series.pkl).

2. Load selected models for classification datasets from [best_Cmodel_series.pkl](https://github.com/NilavoBoral/Therapeutics-Data-Commons/blob/main/best_Cmodel_series.pkl).

3. Run [ADMET Prediction.ipynb](https://github.com/NilavoBoral/Therapeutics-Data-Commons/blob/main/ADMET%20Prediction.ipynb) to `extract features` and `predict for test set by selected models`.

---
### <ins>Results</ins> :
**Results for test set (after 5 independent runs) are shown in the following table.**

| **Dataset**                    | Model                     |No. of Parameters `[Details](https://github.com/NilavoBoral/Therapeutics-Data-Commons/blob/main/Model%20selection%20for%20all%20datasets.ipynb)`| Matric     | Performance   | Rank |
| ------------------------------ | ------------------------- |:----:|:----------:|:-------------:|:----:|
| *`ABSORPTION`*                                                                                 |
| caco2_wang                     | AdaBoostRegressor         |4| MAE ↓      | 0.321 ± 0.005 | 2    |
| hia_hou                        | BaggingClassifier         |4| AUROC ↑    | 0.818 ± 0.01  | 9    |
| pgp_broccatelli                | ExtraTreesClassifier      |2| AUROC ↑    | 0.818 ± 0.0   | -    |
| bioavailability_ma             | RandomForestClassifier    |2| AUROC ↑    | 0.523 ± 0.011 | -    |
| lipophilicity_astrazeneca      | AdaBoostRegressor         |4| MAE ↓      | 0.617 ± 0.003 | 8    |
| solubility_aqsoldb             | AdaBoostRegressor         |4| MAE ↓      | 0.828 ± 0.002 | 4    |
| *`DISTRIBUTION`*                                                                               |
| bbb_martins                    | BaggingClassifier         |3| AUROC ↑    | 0.811 ± 0.013 | 10   |
| ppbr_az                        | GradientBoostingRegressor |3| MAE ↓      | 9.185 ± 0.0   | 2    |
| vdss_lombardo                  | AdaBoostRegressor         |4| SPEARMAN ↑ | 0.627 ± 0.01  | 1    |
| *`METABOLISM`*                                                                                 |
| cyp2d6_veith                   | ExtraTreeClassifier       |2| AUPRC ↑    | 0.358 ± 0.0   | -    |
| cyp3a4_veith                   | XGBClassifier             |1| AUPRC ↑    | 0.654 ± 0.0   | -    |
| cyp2c9_veith                   | BaggingClassifier         |3| AUPRC ↑    | 0.556 ± 0.0   | -    |
| cyp2d6_substrate_carbonmangels | BaggingClassifier         |3| AUPRC ↑    | 0.605 ± 0.0   | -    |
| cyp3a4_substrate_carbonmangels | XGBClassifier             |2| AUROC ↑    | 0.556 ± 0.0   | 7    |
| cyp2c9_substrate_carbonmangels | BaggingClassifier         |3| AUPRC ↑    | 0.281 ± 0.0   | -    |
| *`EXCRETION`*                                                                                  |
| half_life_obach                | AdaBoostRegressor         |4| SPEARMAN ↑ | 0.438 ± 0.011 | 1    |
| clearance_microsome_az         | AdaBoostRegressor         |4| SPEARMAN ↑ | 0.518 ± 0.005 | 8    |
| clearance_hepatocyte_az        | ExtraTreesRegressor       |2| SPEARMAN ↑ | 0.44 ± 0.003  | 1    |
| *`TOXICITY`*                                                                                   |
| herg                           | BaggingClassifier         |3| AUROC ↑    | 0.715 ± 0.011 | -    |
| ames                           | ExtraTreesClassifier      |2| AUROC ↑    | 0.716 ± 0.0   | -    |
| dili                           | KNeighborsClassifier      |1| AUROC ↑    | 0.7 ± 0.0     | -    |
| ld50_zhu                       | ExtraTreesRegressor       |2| MAE ↓      | 0.636 ± 0.001 | 4    |

---
### <ins>Summary</ins> :

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
