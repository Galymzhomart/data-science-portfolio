# Penguin Species Classification

Predicting a penguin's species from body measurements, island and sex.

> This project started as a weekly assignment in an Introduction to Machine Learning course (KBTU). It was then restructured as a standalone case study and extended with additional analysis.

## Questions

- Can species be predicted reliably from physical measurements?
- Which model works best, and which features matter most?

## Approach

- Missing values handled **inside** the scikit-learn pipeline to avoid data leakage
- Baseline, KNN, logistic regression and random forest
- 5-fold stratified cross-validation (a single small test set is too noisy to trust)
- Confusion matrix, classification report and permutation feature importance

## Results

- Two rows without any measurements were dropped; 9 missing values in `sex` are imputed inside the pipeline (no leakage).
- KNN, logistic regression and random forest all reach about 99.7% in 5-fold cross-validation, versus 44.2% for always predicting the most common species. They are effectively tied.
- Test accuracy is 100% on only 69 penguins, so the cross-validated figure is the more reliable estimate.
- Bill length is by far the most informative feature (permutation importance), followed by bill ratio and body mass. Gentoo penguins are the heaviest (about 5,076 g on average vs about 3,700 g for Adelie and Chinstrap).

Full details and charts are in [the notebook](03_penguin_species_classification.ipynb), which is saved with all outputs and can be read directly on GitHub.

## Tools

Python, pandas, seaborn, matplotlib, scikit-learn

## Data

`penguins` dataset from seaborn's public example datasets (loaded automatically, no files needed).

## How to run

From the repository root:

```
pip install -r requirements.txt
jupyter lab
```

Then open `03_penguin_species_classification.ipynb` and run all cells.
