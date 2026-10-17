# Credit EDA

Exploratory data analysis of loan applicants, looking for the factors that relate to credit default risk.

## What the notebook does

- Loads current applications, previous applications and a column-description lookup
- Cleans the data: drops columns with more than 50% missing values, removes duplicates and checks outliers (e.g. `AMT_INCOME_TOTAL`)
- Adds features such as a debt-to-income ratio (`AMT_CREDIT / AMT_INCOME_TOTAL`) and age groups
- Summarises the numeric features, with each column's description attached
- Plots a correlation heatmap of numeric features
- Merges current and previous applications on `SK_ID_CURR` to compare past loan outcomes with current default status (`TARGET`)

## Data

The notebook expects three CSV files: `application_data.csv`, `previous_application.csv` and `columns_description.csv`. They are not included in this repo. Download them, then update the paths in the `pd.read_csv(...)` cell.

## Running it

```bash
pip install -r requirements.txt
jupyter notebook Credit_EDA_Assignment.ipynb
```

## Files

- `Credit_EDA_Assignment.ipynb`: the full analysis
