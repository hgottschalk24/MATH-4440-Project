# MATH-4440-Project

Final project repository for MATH 4440 focused on exploring and modeling a bank marketing dataset in R.

## Project Overview

This project analyzes client-level bank campaign data containing demographic, financial, and prior-contact variables.
The central outcome of interest is whether a client subscribed to a term deposit (`y`).

## Current Analysis Scope

The R Markdown workflow currently includes:

- Data loading from a CSV file
- Data preprocessing (including `pdays` recoding)
- Categorical variable conversion to factors
- Summary statistics for numeric and categorical variables
- Outlier inspection via boxplots
- Visualizations (histogram, boxplots, bar charts, heatmap)
- Relationship exploration between campaign behavior and subscription outcome

## Repository Contents

- `report.Rmd`: Main analysis notebook-style report
- `README.md`: Project summary and usage instructions
- `MATH-4440-Project.Rproj`: RStudio project file

## Required R Packages

The report currently loads these packages:

- `ggplot2`
- `caret`
- `MASS`
- `pscl`
- `rpart`
- `pROC`
- `readr`

Install any missing packages with:

```r
install.packages(c("ggplot2", "caret", "MASS", "pscl", "rpart", "pROC", "readr"))
```

## How To Run

1. Open `MATH-4440-Project.Rproj` in RStudio.
2. Ensure the dataset file (currently referenced as `bank-1.csv`) is in the project root.
3. Open `report.Rmd`.
4. Knit the document to HTML.

## Notes

- The analysis currently keeps outliers instead of removing them, with rationale documented in the report.
- `pdays == -1` is recoded to `0` in a derived variable (`pdays_recode`) for interpretability.

## Next Improvements

- Add a reproducible train/test split and model evaluation section.
- Include confusion matrix, ROC/AUC, and model comparison table.
- Add a brief conclusion with business interpretation and limitations.