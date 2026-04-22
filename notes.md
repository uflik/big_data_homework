# Big Data HF Notes

## Current Direction

Planned prediction target:

- `Diploma_osszes`

Planned core features:

- `GDP`
- `egy főre jutó jövedelem / fogyasztás`
- `Erettsegi_osszes`
- `Felsookt_hallgato_osszes`

This is a regression task, because the target is a numeric value.

## Planned Workflow

1. Fix the exact prediction goal.
2. Reorganize the notebook into the CRISP-DM structure.
3. Keep what is already useful and remove what is confusing or unnecessary.
4. Do a short data understanding step.
5. Clean the selected datasets.
6. Build one merged analysis table.
7. Move the relevant plots and relationship checks into data exploration.
8. Do feature engineering if needed.
9. Do preprocessing for modeling.
10. Train and evaluate the model.
11. Write short conclusions.

## CRISP-DM Mapping

### 1. Business Understanding

Here we define:

- what we want to predict
- why this is interesting
- which KSH variables may explain it

Current candidate:

- predict the number of graduates from economic and education-related indicators

### 2. Data Understanding

Here we check:

- which datasets we have
- what columns they contain
- what years are available
- where values are missing
- whether the tables can be merged

This part is already partially done in the notebook.

### 3. Data Preparation

Here we do the actual preparation work:

- clean year columns
- replace KSH missing-value symbols
- convert text-like numbers to numeric values
- keep only the needed columns
- align the common year range
- merge the selected datasets into one final table

### 4. Modeling

Here we:

- choose `X` and `y`
- split train and test data
- train a regression model

### 5. Evaluation

Here we check:

- how well the model works
- whether the predictions are meaningful
- whether the selected features make sense

### 6. Deployment

For this homework this can mean:

- final notebook structure
- final plots
- final conclusion
- short presentation-ready explanation

## Important Distinctions

### Data Cleaning

Data cleaning means fixing raw-data problems.

Examples:

- wrong year format
- missing-value symbols like `..`
- numbers stored as text
- broken or unnecessary rows

### Feature Engineering

Feature engineering means creating better explanatory variables from existing ones.

Examples:

- growth rate from two yearly values
- ratio of one indicator to another
- lagged variables
- selecting a more informative transformed variable

### Data Preprocessing

Data preprocessing is the model-ready preparation step after cleaning and feature selection.

Examples:

- selecting final input columns
- handling remaining missing values
- scaling
- encoding, if categorical variables exist
- building `X` and `y`

## What Is Already Done

- topic exists
- KSH files are selected
- files are loaded
- some early checks and plots exist
- some cleaning attempts exist
- one early merge attempt exists
- one early model attempt exists

## What Needs To Come Next

- fix the exact target
- reduce the number of datasets
- choose only the useful columns
- create one clear merged dataframe
- then continue with proper exploration and modeling
