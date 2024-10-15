# BACE1 Inhibitor Analysis for Neurological Disease Research

## Introduction

This project focuses on analyzing BACE1 (β-site amyloid precursor protein cleaving enzyme 1) inhibitors, which are crucial in Alzheimer's disease research. We employ various computational methods to visualize and analyze the properties of known BACE1 inhibitors.

## Data Preparation

### Steps:
1. Retrieved BACE1 inhibitor data from ChEMBL database
2. Preprocessed the data, removing entries with missing values
3. Calculated additional molecular descriptors (Lipinski's rule of five)
4. Converted IC50 values to pIC50 for better comparability

The dataset includes information on compound ChEMBL IDs, SMILES representations, and various molecular properties. Proper data preparation was crucial for accurate analysis, enabling meaningful insights into the properties of these important compounds.

## Exploratory Data Analysis

### Steps:
1. Examined basic statistics of the dataset
2. Created visualizations to explore the relationships between different molecular properties
3. Compared active BACE1 inhibitors

Key visualizations included:
- Scatter plot of Molecular Weight vs LogP
- Bar plot of pIC50 values
- Pairplot of numerical features
- Radar plot for compound comparison

These visualizations offer a comprehensive view of the data, allowing for the identification of patterns and trends in BACE1 inhibitors.

## Statistical Analysis

Due to the limited size of our dataset (only two active compounds), we focused on descriptive statistics rather than inferential statistics. We calculated and compared various properties including molecular weight, LogP, number of hydrogen bond donors/acceptors, and pIC50 values.

## Key Findings

Despite the small sample size, our analysis revealed some interesting characteristics of the active BACE1 inhibitors:

- The compounds have similar molecular weights (424.77 and 513.80)
- They show a range of lipophilicity (LogP values of 2.59 and 4.46)
- Both compounds have 2 hydrogen bond donors, but differ in the number of acceptors (6 and 7)
- The compound with higher molecular weight and LogP showed higher potency (higher pIC50 value)

## Conclusion

This analysis provides initial insights into the physicochemical properties of active BACE1 inhibitors. While the small sample size limits the generalizability of our findings, it sets a foundation for future, more comprehensive studies.

## Future Directions

- Expand the dataset to include more BACE1 inhibitors, including inactive compounds for comparison
- Incorporate more diverse molecular descriptors and fingerprints
- Apply machine learning models to predict BACE1 inhibition based on molecular properties
- Investigate the 3D structures of BACE1 inhibitors to understand their binding mechanisms

By leveraging these computational methods and expanding our dataset, we can potentially accelerate the discovery of new treatments for Alzheimer's disease and other neurological conditions.
