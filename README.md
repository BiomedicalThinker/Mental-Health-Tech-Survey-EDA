# Mental Health in the Tech Industry: Exploratory Data Analysis

Statistical exploration of the OSMI *Mental Health in Tech Survey*, answering two research questions with sampling distributions, summary statistics and two-sample t-tests.

## Project overview

This project explores survey data collected by [Open Sourcing Mental Illness (OSMI)](https://osmhelp.org/) through its *Mental Health in Tech Survey*, run in 2014, 2016, 2017, 2018 and 2019. The raw data contains 236,898 individual answers given by 4,218 respondents across 105 unique questions.

The notebook [`mental_health_tech_industry_EDA.ipynb`](mental_health_tech_industry_EDA.ipynb) cleans and reshapes this data, then focuses on a subset of seven questions to answer two research questions:

1. What is the probability that a person working in tech has been diagnosed with a mental illness, and does it differ by country (USA vs. rest of world), gender, or employment type (self-employed vs. employee)?
2. What proportion of tech workers feel comfortable discussing a mental health issue with their coworkers, and does it differ by gender?

Each question is explored with kernel density estimates (KDE) of the sampling distribution of the mean, summary statistics tables, and independent two-sample t-tests (alpha = 0.05). See the notebook's own Table of Contents and Conclusions section for the full write-up and results.

## Data source

- Kaggle dataset: [anth7310/mental-health-in-the-tech-industry](https://www.kaggle.com/datasets/anth7310/mental-health-in-the-tech-industry)
- Originally collected by [Open Sourcing Mental Illness (OSMI)](https://osmhelp.org/)

The dataset is downloaded automatically by the notebook via the `kagglehub` package the first time it runs, and cached locally afterwards.

## How to run

1. Install the dependencies listed below (a virtual environment is recommended).
2. Open `mental_health_tech_industry_EDA.ipynb` in Jupyter Lab/Notebook, VS Code, or any other Jupyter-compatible environment.
3. Run all cells from top to bottom. The first code cell that calls `kagglehub.dataset_download(...)` downloads the dataset the first time it is executed (a free Kaggle account / API token may be required depending on your `kagglehub` configuration).

## Environment

Python 3.13.3, with the following package versions:

| Package | Version |
|---|---|
| pandas | 2.2.3 |
| numpy | 2.2.6 |
| scipy | 1.16.0 |
| seaborn | 0.13.2 |
| matplotlib | 3.10.3 |
| kagglehub | 1.0.2 |
| ipykernel | 6.29.5 |

`sqlite3` and `os` come from the Python standard library. A recent version of Jupyter Lab, Jupyter Notebook, or the VS Code Jupyter extension is also required to run the notebook interactively.

## Repository structure

```
├── mental_health_tech_industry_EDA.ipynb   # Main analysis notebook
└── README.md
```

## Tech stack

Python · pandas · NumPy · SciPy · seaborn · Matplotlib · kagglehub · Jupyter
