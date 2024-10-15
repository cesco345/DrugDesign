# BACE1 Inhibitor Prediction Model for Neurological Disease Research

## Introduction

This project aims to develop a machine learning model to predict potential BACE1 (β-site amyloid precursor protein cleaving enzyme 1) inhibitors. BACE1 is a key enzyme in the pathogenesis of Alzheimer's disease, making it a critical target for drug development in neurological disease research.

## Data Preparation

### Steps:
1. Fetched BACE1 inhibitor data from ChEMBL database
2. Cleaned and preprocessed the data
3. Converted IC50 values to pIC50

- ChEMBL provides a large, curated database of bioactive molecules with drug-like properties.
- pIC50 values (negative log of IC50) are used because they provide a more normally distributed range of values, which is beneficial for many machine learning algorithms.

High-quality, relevant data is crucial for developing accurate predictive models in drug discovery. BACE1 inhibitors are particularly important in Alzheimer's disease research.

## Molecular Representation

### Steps:
1. Generated molecular fingerprints (MACCS keys) from SMILES strings
2. Converted fingerprints to numerical arrays

- Molecular fingerprints capture important structural information about compounds in a format suitable for machine learning.
- MACCS keys are a well-established method for representing molecular structure and have been successful in many QSAR studies.

Effective molecular representation allows the model to learn important structure-activity relationships, which is crucial for predicting potential new drug candidates for neurological diseases.

## Model Development

### Steps:
1. Split data into training and test sets
2. Developed a neural network model
3. Trained the model on the training data

- Neural networks can capture complex, non-linear relationships between molecular structure and biological activity.
- The split into training and test sets allows for unbiased evaluation of the model's performance.

A well-developed predictive model can significantly speed up the drug discovery process by prioritizing compounds for experimental testing, saving time and resources in neurological disease research.

## Model Evaluation

### Steps:
1. Evaluated model performance on test set
2. Calculated Mean Absolute Error (MAE)

- MAE provides a clear, interpretable measure of the model's predictive accuracy.
- Test set evaluation gives an unbiased estimate of the model's performance on new, unseen data.

Understanding the model's predictive power is crucial for determining its utility in real-world drug discovery applications for neurological diseases.

## Virtual Screening

### Steps:
1. Developed a function for virtual screening of compound libraries
2. Demonstrated screening on a small set of example compounds

- Virtual screening allows for the rapid evaluation of large numbers of compounds in silico.
- This approach can identify promising candidates for further experimental testing.

Virtual screening can significantly accelerate the drug discovery process for neurological diseases by prioritizing the most promising compounds for resource-intensive experimental validation.

## Conclusion

This project demonstrates the development of a machine learning-based approach for predicting BACE1 inhibitors, which has potential applications in Alzheimer's disease drug discovery. The model, with its MAE of 0.6044, provides a valuable tool for screening and prioritizing potential drug candidates. 

Future work could involve:
- Refining the model with additional data or advanced architectures
- Integrating other types of data (e.g., 3D structure information)
- Expanding to other targets relevant to neurological diseases

By leveraging computational methods in this way, we can potentially accelerate the discovery of new treatments for devastating neurological conditions.
