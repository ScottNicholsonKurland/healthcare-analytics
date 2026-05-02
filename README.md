# Healthcare MySQL Analytics Project

This project cleans, explores, models, and interprets a healthcare encounter dataset using MySQL-oriented SQL.

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

The SQL-only models did not find strong predictive signal. This is a useful conclusion: the project demonstrates baseline modeling and interpretation rather than inflated claims.
