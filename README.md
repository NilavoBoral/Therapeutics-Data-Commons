# Therapeutics-Data-Commons
Predicting Absorption, Distribution, Metabolism, Excretion and Toxicity (ADMET) Properties of Drug Molecule.

---

**Run ADMET_Properties_Prediction_Using_Descriptors.ipynb for feature extraction, model selection and predict for in set.**

---
Results for test set, after 5 independent runs:


{'ames': [0.716, 0.0],

 'bbb_martins': [0.811, 0.013],
 
 'bioavailability_ma': [0.523, 0.011],
 
 'caco2_wang': [0.321, 0.005],
 
 'clearance_hepatocyte_az': [0.44, 0.003],
 
 'clearance_microsome_az': [0.518, 0.005],
 
 'cyp2c9_substrate_carbonmangels': [0.281, 0.0],
 
 'cyp2c9_veith': [0.556, 0.0],
 
 'cyp2d6_substrate_carbonmangels': [0.478, 0.018],
 
 'cyp2d6_veith': [0.358, 0.0],
 
 'cyp3a4_substrate_carbonmangels': [0.605, 0.0],
 
 'cyp3a4_veith': [0.654, 0.0],
 
 'dili': [0.7, 0.0],
 
 'half_life_obach': [0.438, 0.011],
 
 'herg': [0.715, 0.011],
 
 'hia_hou': [0.818, 0.01],
 
 'ld50_zhu': [0.636, 0.001],
 
 'lipophilicity_astrazeneca': [0.617, 0.003],
 
 'pgp_broccatelli': [0.818, 0.0],
 
 'ppbr_az': [9.185, 0.0],
 
 'solubility_aqsoldb': [0.828, 0.002],
 
 'vdss_lombardo': [0.627, 0.01]}
 
---
Using 31 Descriptors & different ML models with Parameter tuning.

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
