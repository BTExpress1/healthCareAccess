# README
![License: MIT](https://img.shields.io/badge/license-MIT-green)
![Python 3.11](https://img.shields.io/badge/python-3.11-blue)
![Last Updated](https://img.shields.io/github/last-commit/BTExpress1/healthCareAccess)
[![View in NBViewer](https://img.shields.io/badge/notebook-nbviewer-orange)](https://nbviewer.org/github/BTExpress1/healthCareAccess/blob/main/notebooks/CapstoneTwoEDA.ipynb)


## Project Overview
This repository presents a data science project focused on Healthcare Access for African Americans. The goal is to identify disparities in access to care and provide actionable insights to improve health equity across communities.

## Repository Structure and Notes
### Cookiecutter Template
This repository was scaffolded using the cookiecutter data science template (https://drivendata.github.io/cookiecutter-data-science/). As a result, some folders (e.g., references, reports/) may appear empty—they are part of the standard structure but were not used in this project.

## Data Exploration
During the exploratory data analysis (EDA) phase, multiple datasets were reviewed. The final dataset was selected because it best aligned with the project's objectives, especially around race and access to healthcare services.

## Final Version vs Original
To ensure clarity and focus, only the relevant components of the analysis are retained in this version. Some preliminary work that did not directly support the project’s goals has been removed. However, the original repository with all earlier work remains intact and can be referenced separately.

## Modeling Approach
Given the complexity of the healthcare access problem and the nature of the data, I recognized early on that traditional models like linear or logistic regression would be insufficient. However, I implemented a basic version of logistic regression to establish a performance baseline before moving on to more sophisticated modeling techniques.
### Baseline Modeling
To establish a performance benchmark, a simple out-of-the-box linear regression model was applied using scaled features. No feature selection or hyperparameter tuning was performed. While earlier versions of this project included multiple linear regression variations (e.g., pipeline integration, SelectKBest, and GridSearchCV), those efforts provided minimal value and were removed in the final version for clarity.

The linear model now serves solely as a baseline against which tree-based models like Random Forest and LightGBM are compared.

## Modeling Refinement
During model development, I identified significant overfitting driven by features strongly correlated with race. To address this, I removed several high-weight, redundant, or racially skewed features to reduce bias and improve generalization. The dataset itself was imbalanced, with 74.3% of observations attributed to individuals identifying as white. The final model emphasizes social, health, and demographic factors in its predictions, supporting a more equitable and interpretable outcome.

## How to Use This Project
This project is designed to explore healthcare access disparities using 2023 data. To run the analysis and replicate the results:

### Requirements
Python 3.10+

pip

Git LFS (for downloading large model + data files)

git lfs install

### Installation
Clone the repo and install dependencies:

git clone https://github.com/BTExpress1/healthCareAccess.git
cd healthCareAccess
pip install -r requirements.txt

### Project Structure
notebooks/                         # Jupyter notebooks (EDA, training, modeling)
data/                              # Processed and raw datasets
models/                            # Trained model artifacts
reports/                           # Final report and presentation
healthcareaccess/                  # Source code (config, data prep, modeling)

### Running the Project
Launch Jupyter Lab or Notebook:
jupyter lab

Open and run these notebooks in order:

notebooks/healthCareAccess_Wrangling.ipynb

notebooks/healthCareAccess_EDA.ipynb

notebooks/healthCareAccess_training.ipynb

notebooks/healthCareAccess_modeling.ipynb

Results, models, and charts will be saved automatically to:

models/

reports/figures/

### Notes
This project is based on the 2023 CDC NHIS dataset.

Some folders (e.g., docs/, reports/figures/) may contain placeholder or empty files due to the project template (Cookiecutter).

Final model outputs are tracked via Git LFS due to file size.

## Dataset Citation
The final analysis is based on the 2023 National Health Interview Survey (NHIS) Adult File. The dataset was obtained from the Centers for Disease Control and Prevention (CDC), National Center for Health Statistics (NCHS):

Dataset: NHIS 2023 Adult Data (CSV): https://ftp.cdc.gov/pub/Health_Statistics/NCHS/Datasets/NHIS/2023/adult23csv.zip

Codebook: NHIS 2023 Adult Codebook (PDF): https://ftp.cdc.gov/pub/Health_Statistics/NCHS/Dataset_Documentation/NHIS/2023/adult-codebook.pdf


