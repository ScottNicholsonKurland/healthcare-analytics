# Healthcare Encounter Analytics

## At a Glance

| Area | Detail |
|---|---|
| Dataset | 55,500 healthcare encounter records |
| Tools | MySQL, Python, Power BI |
| Skills shown | SQL cleaning, EDA, validation, baseline modeling, interpretation |
| Final cleaned rows and columns | 54,966 and 21 |
| Key result | Descriptive analytics useful; predictive signal weak |
| Best use case | Healthcare operations reporting, not clinical prediction |

## Project objective

Analyze a healthcare encounter dataset to identify billing, utilization, admission, and test-result patterns. The project includes data cleaning, exploratory analysis, supervised modeling, and interpretation.

## Dataset

Source: Kaggle Healthcare Dataset by prasad22: https://www.kaggle.com/datasets/prasad22/healthcare-dataset

This project uses the dataset for educational portfolio purposes. The dataset is synthetic, but this project does not treat it as real clinical evidence.

- Admission date range: **2019-05-08 to 2024-05-07**
- Valid billing records: **54,860**

## Business questions

1. How are encounters distributed by medical condition, admission type, payer, and test result?
2. Which conditions have the highest average billing amounts?
3. How does the length of stay vary across conditions and admission types?
4. Can available encounter fields predict billing amount?
5. Can available encounter fields predict test-result category?

## Methods

- Standardized and cleaned the dataset.
- Removed exact duplicate rows.
- Flagged and excluded invalid negative billing values from billing analysis.
- Created derived fields for admission year, admission month, age group, and length of stay.
- Built regression models for billing amount.
- Built classification models for test-result category.
- Used model feature importance to interpret behavior.

## Key findings

- Average valid billing amount: **$25,594.63**.
- Median valid billing amount: **$25,593.88**.
- Average length of stay: **15.5 days**.
- Best billing model R²: **-0.0000**.
- Best test-result model macro F1: **0.3153**.

The models did not find a strong predictive signal in the available fields. This is useful: the dataset supports data cleaning, EDA, KPI reporting, and modeling workflow demonstration, but it should not be presented as clinically predictive.

## Limitations

- The dataset appears synthetic or highly regularized.
- No stable patient identifier is available.
- Billing values are not strongly explained by available clinical/admin fields.
- The model should not be interpreted as a clinical decision tool.

## Portfolio value

This project demonstrates practical data-analysis workflow discipline: cleaning, profiling, feature engineering, baseline modeling, model comparison, and responsible interpretation.

# Healthcare MySQL Analytics Subproject

This subproject cleans, explores, models, and interprets a healthcare encounter dataset using MySQL-oriented SQL.

## Contents

```text
data/healthcare_cleaned_mysql.csv
sql/01_create_and_load.sql
sql/02_clean_transform.sql
sql/03_eda_queries.sql
sql/04_sql_models.sql
sql/05_validation_and_export_queries.sql
results/model_metrics.csv
results/*.csv
charts/*.png
docs/mysql_analysis_report.md
docs/data_dictionary.md
docs/mysql_workbench_load_guide.md
```

## Workflow

1. Open MySQL Workbench.
2. Run `sql/01_create_and_load.sql` after replacing the CSV path.
3. Run `sql/02_clean_transform.sql` to create `healthcare_clean`.
4. Run `sql/03_eda_queries.sql` for exploration.
5. Run `sql/04_sql_models.sql` for SQL-only baseline models.
6. Run `sql/05_validation_and_export_queries.sql` for QA and export queries.

## Summary

- Raw rows: 55,500
- Cleaned rows: 54,966
- Duplicate rows removed: 534
- Negative billing values handled: 106
- Average billing amount: $25,594.63
- Average length of stay: 15.5 days

## Modeling conclusion

The SQL-only models did not find a strong predictive signal. This is a useful conclusion: the project demonstrates baseline modeling and interpretation rather than inflated claims.

## How to Reproduce

1. Download the original dataset from Kaggle.
2. Open MySQL Workbench.
3. Run `sql/01_create_and_load.sql`.
4. Run `sql/02_clean_transform.sql`.
5. Run `sql/03_eda_queries.sql`.
6. Run `sql/04_sql_models.sql`.
7. Run `sql/05_validation_and_export_queries.sql`.
8. Open the Python notebook in `python/`.
9. Open the Power BI dashboard in `powerbi/`.









