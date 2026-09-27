# Child Nutrition & Household Empowerment — Data Analysis

Statistical analysis of a household-level maternal and child health intervention study in rural Uganda.

## Overview

This project analyzes household survey data from a randomized nutrition and empowerment intervention involving rural Ugandan families.

Households were assigned to one of four study groups:

* **Control** — no intervention
* **WHN** — women's nutrition training
* **MHN** — men's nutrition training
* **WEMP** — women's empowerment and nutrition training

The analysis examines child health and nutrition outcomes alongside household characteristics, maternal and paternal demographics, decision-making, water and sanitation access, and dietary practices.

## Objectives

* Audit the source datasets for duplicates, missing values, and data-entry anomalies.
* Describe the study population and distribution of study groups.
* Explore key categorical and numerical variables.
* Assess the distribution of major numerical outcomes.
* Select appropriate statistical tests based on distributional characteristics.
* Compare changes in child health and nutrition outcomes across intervention groups.
* Examine relationships between child weight and illness burden.

## Analysis Workflow

1. **Data Loading**
2. **Data Quality Audit**

   * Duplicate detection
   * Missing-value analysis
   * Disguised missing-value codes
   * Empty-column detection
   * Study-group validation
3. **Study Population Overview**
4. **Exploratory Data Analysis**

   * Categorical variables
   * Numerical variables
5. **Normality Testing**
6. **Statistical Group Comparisons**
7. **Correlation Analysis**
8. **Key Findings & Limitations**

## Statistical Methods

The analysis uses:

* Shapiro-Wilk normality testing
* Kruskal-Wallis test
* Mann-Whitney U test
* Wilcoxon signed-rank test
* Spearman correlation

Non-parametric methods are used for the primary group comparisons because the normality checks indicate that several key variables do not follow a normal distribution.

## Key Findings

The analysis investigates several notable patterns in the study population:

* Child weight increased between baseline and endline across the study groups.
* The analysis did not find a statistically significant difference in weight gain across the four study groups.
* Changes in household decision-making patterns were observed between baseline and endline.
* Dietary diversity indicators showed differences between intervention groups.
* Water and sanitation access varied considerably across households.
* The relationship between child weight and illness-day variables was weak.

See the notebook for the complete analysis, statistical results, visualizations, and detailed interpretation.

## Limitations

Several limitations should be considered when interpreting the results:

* Some implausible values were identified and were not automatically corrected.
* Anthropometric variables contain missing observations.
* Complete-case comparisons may be affected by loss to follow-up.
* Children from the same household are not statistically independent.
* The analysis does not account for clustering at the household, village, or district level.
* Statistical significance should be interpreted alongside effect size and practical significance.

## Technologies

* Python
* Pandas
* NumPy
* SciPy
* Matplotlib
* Seaborn
* Plotly
* Jupyter Notebook

## Project Structure

```text
child-nutrition-uganda-analysis/
│
├── data/
│   ├── child_level_mcm.tab
│   └── womens_mens_mcm.tab
│
├── notebooks/
│   └── child_nutrition_uganda_analysis.ipynb
│
├── .gitignore
├── README.md
└── requirements.txt
```

## Running the Project

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/child-nutrition-uganda-analysis.git
cd child-nutrition-uganda-analysis
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Launch Jupyter:

```bash
jupyter notebook
```

Open:

```text
notebooks/child_nutrition_uganda_analysis.ipynb
```

## Data

The project uses two tab-separated datasets:

* `child_level_mcm.tab`
* `womens_mens_mcm.tab`

Please refer to the dataset's original source and data-use terms before redistributing or reusing the data.
