# ITMO DL and NLP Course - Homework Solutions

Homework solutions for the "Deep Learning and NLP" course at ITMO AI Talent Hub (Spring 2026).

## Repository Structure

```
.
├── course/
│   └── itmo_dl_nlp_course/          # Course materials (submodule)
├── data/
│   ├── raw/
│   │   └── hw_1/                     # lenta-ru-news.csv.gz
│   ├── interim/
│   │   └── hw_1/                     # Preprocessed dataframe
│   └── processed/
│       └── hw_1/                     # Train/val/test parquet splits
├── weights/
│   └── hw_1/                         # Best sklearn pipeline (joblib)
├── notebooks/
│   └── hw_1_classic_ml.ipynb         # HW1: Classic ML text classification
├── pyproject.toml                    # Dependencies (managed by uv)
└── README.md
```

## Setup

1. Install [uv](https://docs.astral.sh/uv/getting-started/installation/)
2. Clone and init submodules:
   ```bash
   git clone <repo-url>
   cd itmo-ai-talent-hub-dl-and-nlp-course
   git submodule update --init --recursive
   ```
3. Install deps and launch:
   ```bash
   uv sync
   uv run jupyter notebook
   ```

## HW1: Classic ML Text Classification

**Notebook:** `notebooks/hw_1_classic_ml.ipynb`

Topic classification on lenta-ru-news (100k texts) with CountVectorizer, TfidfVectorizer, and LogisticRegression. Includes preprocessing (razdel + pymorphy3), hyperparameter tuning, and error analysis.

## Data

Data and weights are not tracked in git. Notebooks download everything automatically on first run. Run HW1 before HW2 (HW2 reuses HW1 splits).
