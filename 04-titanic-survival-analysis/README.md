# Titanic Survival Analysis

Which passenger characteristics were associated with survival, and how well can a simple model predict it?

> This project started as a weekly assignment in an Introduction to Machine Learning course (KBTU). It was then restructured as a standalone case study and extended with additional analysis.

## Questions

- How did sex, class, age and family size relate to survival?
- How well does a baseline logistic regression predict survival?

## Approach

- Documented data-quality decisions: no passenger ID exists, so look-alike rows are kept, not dropped
- Age imputed by median per class and sex; fare log-transformed instead of clipped
- Feature engineering: family size, age groups
- Cross-validated logistic regression baseline with odds ratios

## Results

See the **Key findings** section at the end of [the notebook](04_titanic_survival_analysis.ipynb). The notebook is saved with all outputs, so it can be read directly on GitHub.

## Tools

Python, pandas, seaborn, matplotlib, scikit-learn

## Data

`titanic` dataset from seaborn's public example datasets (loaded automatically, no files needed).

## How to run

From the repository root:

```
pip install -r requirements.txt
jupyter lab
```

Then open `04_titanic_survival_analysis.ipynb` and run all cells.
