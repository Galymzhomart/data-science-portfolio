# GDP per Capita vs Life Satisfaction

Is higher GDP per capita associated with higher life satisfaction, and how well can a simple model predict it?

> This project started as a weekly assignment in an Introduction to Machine Learning course (KBTU). It was then restructured as a standalone case study and extended with additional analysis.

## Questions

- How strong is the relationship between GDP per capita and life satisfaction?
- Does a simple linear model beat KNN and a naive baseline?
- How much does life satisfaction change per additional 10,000 USD of GDP?

## Approach

- Pearson and Spearman correlation with significance
- Leave-one-out cross-validation, because 27 countries are too few for a stable train/test split
- Linear regression vs KNN (k = 1, 3, 5, 10) vs a mean baseline, compared by RMSE, MAE and R2
- Explicit limitations: sample size, extrapolation, correlation vs causation

## Results

- Strong positive association between GDP per capita and life satisfaction: Pearson r = 0.85 (p = 1.6e-08), Spearman 0.84.
- About +0.68 points of life satisfaction per additional 10,000 USD of GDP per capita.
- Leave-one-out cross-validation: KNN (k=10) has the lowest error (RMSE 0.37), linear regression follows (0.43), and the mean baseline is far behind (0.78). Because k was chosen on the same cross-validation, the KNN result is slightly optimistic; linear regression is close and interpretable.
- Limitation: only 27 countries between about 26,000 and 60,000 USD GDP per capita, so predictions outside that range are extrapolation.

Full details and charts are in [the notebook](02_gdp_vs_life_satisfaction.ipynb), which is saved with all outputs and can be read directly on GitHub.

## Tools

Python, pandas, matplotlib, SciPy, scikit-learn

## Data

`lifesat.csv` (27 countries: GDP per capita and life satisfaction) was provided with the course materials and is not included in this repository. The notebook is saved with all outputs, so every result and chart can be read without re-running it.

## How to run

To re-run the notebook you need the course file `lifesat.csv` in this folder. From the repository root:

```
pip install -r requirements.txt
jupyter lab
```

Then open `02_gdp_vs_life_satisfaction.ipynb` and run all cells.
