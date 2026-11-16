# Restaurant Tipping Behavior Analysis

What drives tips in a restaurant: weekends, gender, smoking status and bill size?

> This project started as a weekly assignment in an Introduction to Machine Learning course (KBTU). It was then restructured as a standalone case study and extended with additional analysis.

## Questions

- Do customers tip more on weekends?
- Do gender or smoking status influence tipping?
- How does the size of the bill affect the tip?

## Approach

- Tip **percentage** as a size-independent metric (dollar tips mostly follow the bill)
- Welch t-tests for weekend, gender and smoking effects instead of comparing means by eye
- Linear regression evaluated on a held-out test set and compared with a mean-tip baseline
- Findings generated from the data, so the text always matches the numbers

## Results

See the **Key findings** section at the end of [the notebook](01_tipping_behavior_analysis.ipynb). The notebook is saved with all outputs, so it can be read directly on GitHub.

## Tools

Python, pandas, seaborn, matplotlib, SciPy, scikit-learn

## Data

`tips` dataset from seaborn's public example datasets (loaded automatically, no files needed).

## How to run

From the repository root:

```
pip install -r requirements.txt
jupyter lab
```

Then open `01_tipping_behavior_analysis.ipynb` and run all cells.
