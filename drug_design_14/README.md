# QSAR Modeling of BACE1 Inhibitors for Alzheimer's Disease Research

## Introduction

This project focuses on developing a Quantitative Structure-Activity Relationship (QSAR) model for BACE1 (β-site amyloid precursor protein cleaving enzyme 1) inhibitors, which are crucial in Alzheimer's disease research. We employ various computational methods to analyze and predict the activity of BACE1 inhibitors based on their molecular properties.

## Data Preparation

### Steps:
1. Loaded BACE1 inhibitor data from a CSV file
2. Examined the dataset structure and contents
3. Calculated additional molecular descriptors

Proper data preparation is crucial for accurate QSAR modeling. The dataset includes information on compound SMILES representations, pIC50 values, and various molecular properties. Additional descriptors provide a more comprehensive representation of molecular features that may influence BACE1 inhibition.

## Feature Engineering

### Steps:
1. Calculated topological descriptors (e.g., TPSA, NumRotatableBonds, NumRings)
2. Computed Lipinski descriptors (e.g., Molecular Weight, LogP, H-bond donors/acceptors)
3. Generated additional features like QED (Quantitative Estimate of Drug-likeness)

These molecular descriptors capture different aspects of compound structure and properties. Topological descriptors represent the 2D structure, Lipinski descriptors relate to drug-likeness, and QED provides an overall estimate of how drug-like a molecule is. These features are chosen based on their potential relevance to BACE1 inhibition and general principles of medicinal chemistry.

## QSAR Model Development

### Steps:
1. Split the data into training and testing sets
2. Scaled the features using StandardScaler
3. Trained a Random Forest Regressor model
4. Performed cross-validation to assess model stability
5. Conducted hyperparameter tuning using RandomizedSearchCV

Random Forest is chosen for its ability to capture non-linear relationships and handle high-dimensional data. Cross-validation provides a robust estimate of model performance, while hyperparameter tuning optimizes the model's predictive power. These steps ensure we develop a reliable and generalizable QSAR model.

## Model Evaluation

### Steps:
1. Calculated Mean Squared Error (MSE) and R-squared score on the test set
2. Performed 5-fold cross-validation
3. Computed Mean RMSE across folds

### Results: 

Cross-Validation Results:
RMSE scores: [0.90632646 0.94634427 0.90206009 0.89229157 0.91308379]
Mean RMSE: 0.9120 (+/- 0.0369)

These metrics provide a comprehensive evaluation of model performance. RMSE indicates the average prediction error in pIC50 units, while cross-validation ensures the model's stability across different subsets of the data.

## Feature Importance Analysis

### Steps:
1. Conducted permutation importance analysis
2. Visualized feature importances

### Key Findings:
1. QED (Quantitative Estimate of Drug-likeness) is the most important feature
2. Number of Hydrogen Bond Acceptors (n_hba) is the second most important feature
3. Several features show minimal or negative importance

Permutation importance provides insight into which molecular properties are most crucial for predicting BACE1 inhibition. This information is valuable for understanding structure-activity relationships and can guide future drug design efforts.

## Conclusions and Insights

1. The model shows moderate predictive power with a mean RMSE of 0.9120 pIC50 units.
2. Drug-likeness (QED) is a strong predictor of BACE1 inhibition potency.
3. The number of hydrogen bond acceptors plays a significant role, aligning with known BACE1 binding site characteristics.
4. Traditional descriptors like molecular weight and TPSA show surprisingly low importance, warranting further investigation.

## Future Directions

1. Explore more advanced machine learning algorithms (e.g., Gradient Boosting, Deep Learning)
2. Incorporate more diverse molecular descriptors and fingerprints
3. Investigate the high importance of QED and its components
4. Collect more data to improve model robustness and generalizability
5. Collaborate with medicinal chemists to validate and interpret model findings
