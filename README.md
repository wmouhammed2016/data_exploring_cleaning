# 🐼 Python-S3 — Exploring & Cleaning Data with Pandas

Welcome to Session 3! This repo is a hands-on lecture kit for turning a messy, real-world CSV into a trustworthy dataset — the workflow every data analyst leans on before building a single chart or model.

## 🎯 What this session is about

The star of the show is **[`exploring_cleaning_data.ipynb`](exploring_cleaning_data.ipynb)** — a full walkthrough (with a matching blank practice version, **[`exploring_cleaning_data_empty.ipynb`](exploring_cleaning_data_empty.ipynb)**) that takes a CSV from *"just downloaded"* to *"ready for analysis"* using nothing but Pandas.

Each topic follows the same rhythm: **explanation → demo → exercise 🧪**

| #  | Topic                        | What you'll do                                                        |
| -- | ---------------------------- | --------------------------------------------------------------------- |
| 0  | Setup                        | Load`pandas`, `numpy`, `matplotlib`                             |
| 1  | Getting Oriented             | `.shape`, `.head()`, `.info()` — first look at the data        |
| 2  | Descriptive Exploration      | `.describe()`, `.value_counts()` — what does "normal" look like? |
| 3  | Data Types & Conversions     | Fix dates and categories so operations actually work                  |
| 4  | Missing Data                 | Find gaps with`.isnull().sum()`, then drop vs. fill                 |
| 5  | Duplicate Detection          | `.duplicated()` on full rows and meaningful subsets                 |
| 6  | Inconsistent / Dirty Values  | Normalize casing, whitespace, and typos in text columns               |
| 7  | Outliers & Sanity Checks     | Range checks, IQR, boxplots — is it an error or just reality?        |
| 8  | Filtering & Boolean Indexing | `.loc`, `.iloc`, and combined conditions                          |
| 9  | Reshaping & Aggregating      | `.groupby()` and `.pivot_table()` turn clean rows into answers    |
| 10 | Wrap-Up                      | A repeatable cleaning checklist + capstone exercise                   |

## 📊 The dataset

**[`Sample-Superstore2019.csv`](Sample-Superstore2019.csv)** — 9,994 orders from a fictional retail superstore (2016–2019), covering customers, products, shipping, and sales/profit figures.

### 🤓 Fun facts hiding in the data

- The CSV ships with a sneaky `Unnamed: 0` column — a classic sign of a file exported *with* its row index baked in. Spotting it is your first mini cleaning win.
- `Postal Code` has exactly **11** missing values. Small enough to actually go find them by hand.
- Negative `Profit` isn't a bug — it just means an order sold at a loss. Not every "weird" number is a data error!
- The dataset is refreshingly clean on typos/casing... but you only know that *because* you checked with `.unique()`, not because you assumed it.

## 📚 Bonus material

- **[`jupyter_notebook_vscode.ipynb`](jupyter_notebook_vscode.ipynb)** — a primer on Jupyter Notebooks in VS Code: running cells, kernels, Markdown + images, command vs. edit mode, and keyboard shortcuts.
- **[`GitHub_Repo_From_Terminal_Guide.docx`](GitHub_Repo_From_Terminal_Guide.docx)** — a guide for setting up a GitHub repo from the terminal.
- **[`Python-S3.md`](Python-S3.md)** — the lecture agenda.
- **[`images/`](images)** — screenshots and diagrams used across the notebooks.

## 🚀 Getting started

```bash
# 1. Create and activate a virtual environment
python -3.14 -m venv .venv
.venv/Scripts/activate

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch the notebook (VS Code or Jupyter)
# Open exploring_cleaning_data_empty.ipynb and start cleaning! 🧹
```

## ✅ The cleaning checklist (TL;DR)

1. **Shape & types** — what am I working with?
2. **Descriptive stats** — what does "normal" look like?
3. **Fix types** — dates, numbers, categories
4. **Missing data** — find it, then decide drop vs. fill *per column*
5. **Duplicates** — full-row and meaningful subsets
6. **Consistency** — normalize text values
7. **Outliers** — range checks + IQR/boxplots
8. **Filter & select** — `.loc` / `.iloc` / boolean indexing
9. **Aggregate** — `.groupby()` / `.pivot_table()` for real answers

Happy cleaning! 🧼🐼
