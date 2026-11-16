# Data Science Portfolio

Data analysis and machine learning projects in Python by a 3rd-year Information Systems student (KBTU).

The four projects below started as coursework in an Introduction to Machine Learning course. I restructured each one as a standalone case study and extended it with additional analysis: statistical tests, proper validation, leakage-free pipelines and clearly stated limitations.

## Projects

| # | Project | Question | Tools |
|---|---------|----------|-------|
| 1 | [Restaurant Tipping Behavior Analysis](01-tipping-behavior-analysis/) | What drives tips in a restaurant: weekends, gender, smoking status and bill size? | Python, pandas, seaborn, matplotlib, SciPy, scikit-learn |
| 2 | [GDP per Capita vs Life Satisfaction](02-gdp-vs-life-satisfaction/) | Is higher GDP per capita associated with higher life satisfaction, and how well can a simple model predict it? | Python, pandas, matplotlib, SciPy, scikit-learn |
| 3 | [Penguin Species Classification](03-penguin-species-classification/) | Predicting a penguin's species from body measurements, island and sex. | Python, pandas, seaborn, matplotlib, scikit-learn |
| 4 | [Titanic Survival Analysis](04-titanic-survival-analysis/) | Which passenger characteristics were associated with survival, and how well can a simple model predict it? | Python, pandas, seaborn, matplotlib, scikit-learn |

## Run locally

```
python -m venv .venv
.venv\Scripts\activate        # Windows (macOS/Linux: source .venv/bin/activate)
pip install -r requirements.txt
jupyter lab
```

Each project folder contains its own README and a notebook saved with outputs.
