# Data Wrangling of an Auto Insurance Dataset

A complete data-wrangling workflow on a vehicle-insurance policy dataset — **13,336 policies × 43 features** — taking raw, messy data to a clean, model-ready table with the claim flag (`is_claim`) as the target.

## What the notebook does

1. **Load & inspect** — first/last records, schema, dtypes and descriptive statistics
2. **Missing values** — null audit across all columns, then rows with nulls dropped
3. **Duplicates** — duplicate-record check and removal
4. **Exploratory checks** — claim counts by group (`groupby` on `is_claim`), count plots with Seaborn
5. **Identifier removal** — `policy_id` dropped (an ID carries no signal)
6. **Outlier analysis** — box plots of car age by claim status, plus an automated box-plot loop across numeric features
7. **Correlation analysis** — full correlation matrix with visualization (including safety features such as `ncap_rating`)
8. **Encoding** — automated count plots for categorical features, then label encoding of all categoricals
9. **Model-ready split** — features/target separated into `X` (13,336 × 43) and `y` (`is_claim`)

## Dataset

Auto-insurance policy records: policyholder and vehicle attributes (car age, NCAP safety rating, vehicle/segment features), policy characteristics, and the binary claim outcome `is_claim`.

## Tools

Python · pandas · NumPy · Matplotlib · Seaborn · scikit-learn (label encoding)

## Run it

```bash
jupyter notebook project_of_insurance_dataset.ipynb
```

## Author

**Muhammad Hamza** — Data Scientist · [GitHub @mhamza6051](https://github.com/mhamza6051)
