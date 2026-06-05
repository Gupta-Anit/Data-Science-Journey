# Data Science Journey

A curated personal collection of data-science learning materials: reusable code snippets, interview-preparation examples (Python, SQL, and notebooks), and an end-to-end salary-prediction project framework. It is meant as a working reference and study log rather than a single self-contained application.

## Overview

This repository gathers practical artifacts collected while building data-science and analytics skills:

- Reusable **pandas** snippets for common data-wrangling tasks.
- A reference write-up on Python **list comprehensions**.
- A set of real **interview / take-home examples** worked in Python, SQL, and Jupyter, organized by company.
- A flagship **salary-prediction project** structured as a full DEFINE → DISCOVER → DEVELOP → DEPLOY workflow.

Because it spans several independent topics, treat each folder as a standalone resource.

## What's inside

| Path | Contents |
| --- | --- |
| `Salary Predictions Project.ipynb` | Flagship project notebook — structured ML workflow for predicting salaries from job descriptions (see Highlight below). |
| `Salary Prediction Interview Assignment.docx` | The original assignment brief for the salary-prediction project. |
| `Code_Snippets/Data_Wrangling.py` | Reusable pandas snippets: forward-filling null columns by pattern and reshaping wide data with `pd.melt`. |
| `Code_Snippets/List_Comprehensions.txt` | Reference notes and examples on Python list comprehensions (simple, nested, and filtered forms). |
| `Interviews/Examples/Company1/` | Worked take-home: a classification challenge notebook plus an ROC-curve plot. |
| `Interviews/Examples/Company2/` | Worked take-home: a product-analytics exercise in Python plus a set of Mode SQL queries (percentiles, check-in frequency, sign-up composition). |
| `img/` | Image assets used by the repository. |
| `pdfs/` | Placeholder folder for exported PDF copies of notebooks. |

## Highlight: Salary Prediction Project

**Goal:** predict salaries from job-description features.

**Approach:** the notebook (`Salary Predictions Project.ipynb`) is organized as a complete, reproducible ML workflow in four phases:

1. **Define** — frame the problem and success metric.
2. **Discover** — load, clean, and explore the data (EDA), then establish a simple baseline (e.g. average salary per industry) and hypothesize candidate models.
3. **Develop** — engineer features, train and tune models, and validate them with 5-fold cross-validation.
4. **Deploy** — automate the training pipeline, score the test set, and persist predictions plus feature-importance visualizations.

**Metric & target:** the project uses Mean Squared Error (MSE), with the stated goals of **MSE < 360** for entry-level roles and **MSE < 320** for senior roles, evaluated under 5-fold cross-validation.

> Note: the notebook captures the full project structure and methodology as a working framework; it is intended to be run against the accompanying job-description dataset to produce the final fitted models and scores.

## Tech stack

- **Python 3** — pandas, NumPy, scikit-learn
- **Visualization** — matplotlib, seaborn
- **SQL** — analytical queries (window functions, `NTILE` percentiles) authored for Mode
- **Jupyter Notebook** for exploratory and project work

## Setup & usage

```bash
# Clone
git clone https://github.com/Gupta-Anit/Data-Science-Journey.git
cd Data-Science-Journey

# (Recommended) create a virtual environment
python3 -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch the flagship project
jupyter notebook "Salary Predictions Project.ipynb"
```

The standalone snippets in `Code_Snippets/` and the SQL files under `Interviews/` can be read or copied directly; they do not require installation.

## License & attribution

This repository aggregates personal notes alongside **third-party educational content** (notably a Salary Prediction project framework and interview materials from **Mikiko Bazeley / Springboard**). Because of that, **no blanket open-source license is asserted**; see [`ATTRIBUTION.md`](ATTRIBUTION.md). Rights to third-party material remain with their original authors.
