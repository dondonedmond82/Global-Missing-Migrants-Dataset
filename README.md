# Global Missing Migrants Dataset --- Data Analysis Project

A Python-based exploratory data analysis project using the **Global
Missing Migrants Dataset**. The project introduces foundational data
manipulation and statistical analysis concepts, creates visualizations
of documented incidents, and produces a PDF decision brief to support
evidence-informed discussion and humanitarian coordination.

> **Important:** This dataset represents documented incidents, not
> necessarily every migration-related death or disappearance. Findings
> should be interpreted as patterns in recorded data, not as a complete
> count or a population-adjusted measure of risk.

## Project Objectives

-   Load and inspect a real-world CSV dataset using Python and Pandas.
-   Understand core data structures, including lists, dictionaries,
    Series, and DataFrames.
-   Assess data quality, including missing values, duplicate rows, data
    types, and date fields.
-   Apply descriptive statistics such as mean, median, standard
    deviation, percentiles, and grouped summaries.
-   Explore recorded incidents by year, region, migration route, cause,
    and other available dimensions.
-   Create charts that help communicate patterns and data limitations.
-   Prepare a PDF decision brief with findings and practical
    recommendations.

## Project Files

  -----------------------------------------------------------------------------------------------
  File                                                        Description
  ----------------------------------------------------------- -----------------------------------
  `Global Missing Migrants Dataset.csv`                       Source dataset used for the
                                                              analysis.

  `foundations_data_analysis_global_missing_migrants.ipynb`   Jupyter Notebook with data
                                                              inspection, cleaning, statistical
                                                              analysis, visualizations, and
                                                              practice exercises.

  `global_missing_migrants_decision_brief.pdf`                PDF report containing charts, key
                                                              findings, limitations, and decision
                                                              recommendations.

  `README.md`                                                 Project documentation and
                                                              instructions.
  -----------------------------------------------------------------------------------------------

The notebook may create an `analysis_outputs/` directory containing
exported data-quality summaries and a cleaned CSV when the export
section is run.

## Dataset Overview

The supplied CSV contains **13,020 records and 19 columns**. The
available fields include:

-   Incident type and incident year
-   Reported month
-   Region of origin and region of incident
-   Country of origin
-   Number of dead
-   Minimum estimated number of missing
-   Total number of dead and missing
-   Number of survivors
-   Number of females, males, and children
-   Cause of death or incident description
-   Migration route
-   Location of death
-   Information source
-   Coordinates
-   UNSD geographical grouping

The supplied data includes incident-year values from **2014 to 2023**.
Always verify the dataset version and its documentation before comparing
results with other releases.

## Tools and Technologies

-   **Python 3**
-   **Jupyter Notebook / JupyterLab / VS Code**
-   **Pandas** --- data loading, cleaning, transformation, and grouping
-   **NumPy** --- numerical operations
-   **Matplotlib** --- chart creation
-   **Seaborn** --- statistical visualizations
-   **OpenPyXL** --- optional Excel support for related workflows

## Getting Started

### 1. Prepare the project folder

Place these files in the same directory:

``` text
global-missing-migrants-analysis/
├── Global Missing Migrants Dataset.csv
├── foundations_data_analysis_global_missing_migrants.ipynb
├── global_missing_migrants_decision_brief.pdf
└── README.md
```

The PDF is an already-generated report. It is not required to run the
notebook.

### 2. Create and activate a virtual environment (recommended)

**Windows --- Command Prompt**

``` bat
python -m venv .venv
.venv\Scripts\activate
```

**macOS / Linux**

``` bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

``` bash
python -m pip install --upgrade pip
pip install pandas numpy matplotlib seaborn jupyter
```

### 4. Launch Jupyter

``` bash
jupyter notebook
```

Open `foundations_data_analysis_global_missing_migrants.ipynb`, then run
the cells from top to bottom.

Alternatively, open the notebook directly in Visual Studio Code and
select a Python kernel.

### 5. Confirm the dataset path

The notebook expects `Global Missing Migrants Dataset.csv` to be in the
same folder. If it is stored elsewhere, update the `FILE_PATH` variable
in the notebook.

## Analysis Workflow

The notebook follows this general workflow:

1.  **Load data** --- read the CSV and inspect its dimensions and sample
    rows.
2.  **Understand structures** --- review DataFrames, Series, lists,
    dictionaries, and column data types.
3.  **Inspect quality** --- measure missing values, identify duplicate
    rows, and review unique values.
4.  **Prepare data** --- standardize column names and parse suitable
    date and numeric fields.
5.  **Summarize data** --- calculate descriptive statistics and category
    frequencies.
6.  **Explore patterns** --- group records by available dimensions such
    as region, route, cause, and country.
7.  **Visualize results** --- create bar charts, histograms, box plots,
    time-series charts, scatter plots, and correlation heatmaps where
    appropriate.
8.  **Review geography** --- plot latitude and longitude if separate
    usable coordinate columns are available.
9.  **Export outputs** --- save a cleaned CSV and data-quality summary
    tables.
10. **Interpret responsibly** --- document assumptions, limitations, and
    potential implications for decisions.

## Decision Brief

The PDF report, `global_missing_migrants_decision_brief.pdf`, presents
descriptive findings and visualizations, including:

-   Recorded incidents over time
-   Regions with the most recorded incidents
-   Migration routes with the most recorded incidents
-   Frequently recorded causes or incident descriptions
-   Distribution of reported deaths and missing persons per record
-   Data-quality considerations
-   Recommended actions for data validation, operational review,
    analysis, and safeguarding

Initial results from this dataset identify **North America** as the most
frequently recorded incident region, **US--Mexico border crossing** as
the most frequently recorded migration route, and **drowning** as the
most frequently recorded cause/incident description. These are record
counts and must not be interpreted on their own as comparative risk
rates.

## Data Quality and Interpretation

Please keep the following considerations in mind:

-   **Missing values are not zero.** A blank may mean information was
    unavailable or not reported.
-   **Duplicates require review.** Identical rows may be duplicate
    records, but should not be removed without checking the dataset's
    documentation and context.
-   **Recorded counts are not risk rates.** Comparisons between regions
    or routes need relevant denominators, such as estimated travel
    volume, as well as information about reporting coverage.
-   **Trends may reflect reporting changes.** An increase or decrease in
    documented records can be affected by access, source coverage,
    classification, and reporting practices.
-   **Reported totals may be estimates.** Totals across records may not
    equal a verified count of unique individuals.
-   **Correlations do not prove causation.** Interpret associations
    carefully, especially when variables have different meanings or are
    related by definition.
-   **Geographic information may be imprecise or sensitive.** Avoid
    publishing unnecessary location precision or details that could put
    vulnerable people, survivors, or families at risk.
-   **Verify before making decisions.** Triangulate findings with
    official documentation, current operational assessments, and
    relevant subject-matter expertise.

## Potential Decision Uses

This analysis can help teams:

-   Identify where recorded incidents and reporting activity are
    concentrated.
-   Review whether reporting coverage and data completeness differ
    across regions or routes.
-   Improve data validation rules and standardize incident
    classifications.
-   Distinguish incident frequency from the reported severity of
    incidents.
-   Identify where additional investigation or coordination may be
    useful.
-   Develop a repeatable data-quality and descriptive-analysis workflow.

The dataset alone should not be used to make claims about an
individual's risk or to rank routes by safety without additional
evidence and suitable denominators.

## Reproducibility

For reproducible results:

-   Keep an unchanged copy of the original dataset.
-   Record the dataset release/version and date of download.
-   Run the notebook from top to bottom.
-   Document any manual changes to column selection, filters, or
    cleaning rules.
-   Review exported data before sharing it.
-   Do not treat automated column detection as a substitute for checking
    the data dictionary.

## License and Attribution

Use the source dataset in accordance with the terms, attribution
requirements, and usage guidance supplied by the dataset publisher. This
project README does not assign a new license to the source data.

## Disclaimer

This is a descriptive educational and decision-support analysis, not a
substitute for official humanitarian assessments, verified incident
investigations, or expert operational judgement. The results reflect the
supplied file and have not been independently verified against external
sources.
