# Ti6Al4V-NiTi-LDED-MachineLearning
This repository provides the source code, model parameter settings, data description, and reproducibility files for machine-learning-assisted optimization of process parameters for laser directed energy deposition of Ti6Al4V-NiTi mixed powders.

## Research topic
This work focuses on the intelligent prediction and optimization of process parameters for Ti6Al4V-NiTi composite tracks fabricated by laser directed energy deposition, abbreviated as L-DED.
The machine learning models are used for two main tasks:
1. **Forming morphology prediction**
2. **Defect type classification**

The purpose of this repository is to improve the transparency, reproducibility, and traceability of the model training procedures, parameter settings, and data labeling strategy used in my research.

## Dataset overview
The dataset contains 120 single-track L-DED samples fabricated using Ti6Al4V-NiTi mixed powders.

### Task 1: Forming morphology prediction
- Number of samples: 120
- Number of input features: 5
- Number of output labels: 6
- Data splitting ratio: 4:1
- Evaluation metric: RMSE
  
Input features:

1. NiTi powder mass ratio
2. Laser power
3. Laser scanning speed
4. Normalized line mass
5. Laser energy density

Output labels:

1. Heat-affected zone width
2. Heat-affected zone depth
3. Molten pool width
4. Deposited height
5. Left wetting angle
6. Right wetting angle

### Task 2: Defect type classification
The defect type prediction task is a three-class classification problem.
- Number of samples: 120
- Number of input features: 11
- Number of output classes: 3
- Data splitting ratio: 11:1 with stratified sampling
- Evaluation metrics: Accuracy, F1-score, and ROC-AUC

Input features:

1. NiTi powder mass ratio
2. Laser power
3. Laser scanning speed
4. Normalized line mass
5. Laser energy density
6. Heat-affected zone width
7. Heat-affected zone depth
8. Molten pool width
9. Deposited height
10. Left wetting angle
11. Right wetting angle

Class labels:

| Label | Description |
|---|---|
| 0 | Pores, unmelted particles, and lack of fusion |
| 1 | Desirable process parameters |
| 2 | Cracks |

## Machine learning models
### Regression models
1. Linear Regression
2. Lasso Regression
3. Ridge Regression
4. Random Forest Regression
5. Support Vector Regression
6. K-Nearest Neighbors Regression
7. Artificial Neural Network Regression
8. XGBoost with gblinear booster
9. XGBoost with gbtree booster
10. XGBoost with dart booster
11. TabPFN Regressor
12. TabPFN with Post Hoc Ensembling
### Classification models
1. Logistic Regression
2. Random Forest Classifier
3. Support Vector Classifier
4. K-Nearest Neighbors Classifier
5. Artificial Neural Network Classifier
6. XGBoost with gblinear booster
7. XGBoost with gbtree booster
8. XGBoost with dart booster
9. TabPFN Classifier
10. TabPFN with Post Hoc Ensembling

## Reproducibility
The Python environment can be reproduced using `requirements.txt`.

Install dependencies using pip:

```bash
pip install -r requirements.txt
