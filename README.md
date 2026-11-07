# Income Data Visualization and Classification

This project uses the UCI Adult dataset to explore how demographic, educational, and employment attributes relate to the recorded income bracket. It also compares classifiers that predict whether annual income exceeds $50,000.

| Notebook | What it covers |
| --- | --- |
| [Univariate Analysis](Univariate_Analysis.ipynb) | Distributions and frequency plots for individual variables and their relationship to the income label |
| [Bivariate Analysis](Bivariate_Analysis.ipynb) | Relationships between variables using correlation, categorical comparisons, parallel coordinates, and exploratory PCA and K-means |
| [Machine Learning Analysis](MachineLearningAnalysis.ipynb) | Baseline classifiers, including logistic regression, random forest, decision tree, and k-nearest neighbors |
| [Model Comparison and Feature Importance](ML%20%26%20Feature%20Importance.ipynb) | Encoding comparisons, grid searches, CatBoost, and feature importance |

## Data and results

The archived input contained 48,842 rows. Of those, 37,155 were labeled `<=50K` and 11,687 were labeled `>50K`. The project examines predictors such as age, education, occupation, and hours worked per week. These patterns describe associations in the dataset.

The project report recorded CatBoost accuracy of **88.83% on training data**, **87.47% on validation data**, and **87.76% on test data**. These figures are from the archived experiment. The majority class makes up about 76% of the combined input, so the class distribution matters when interpreting accuracy.

## Run the notebooks

1. Install the dependencies with `python -m pip install -r requirements.txt`.
2. Download `adult.data` and `adult.test` from the [UCI Adult dataset directory](https://archive.ics.uci.edu/ml/machine-learning-databases/adult/). To recreate the input format, remove the test file's comment line and blank lines, strip whitespace from fields, remove the trailing period from test labels, and combine the files in that order into a headerless `adult-all.csv`.
3. Launch `jupyter notebook` from the repository root. The feature importance notebook includes Google Colab setup and Drive paths. For local Jupyter, skip the mount cell and point the data and performance CSV paths to your working directory.
4. Run the notebooks in order within each file. Some cells use older library APIs and may need a compatible environment.

The notebook source cells were preserved. Saved outputs, older drafts, and the dataset are kept outside this package.
