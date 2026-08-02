# DSjobtracker_survey

## Summary
This repository contains the data and documentation collected as part of a multi-group survey of job advertisements in the fields of data science and statistics. The dataset was created by systematically extracting information from job postings and transforming it into a structured, study-ready format to provide insights into the qualifications, technical skills, programming languages, software tools, and experience commonly requested by employers.

## Project scope
- Data were collected by 10 student groups. Each group's raw extraction is saved as Group_1.xlsx through Group_10.xlsx in the repository root.
- Our group's contribution is Group_1.xlsx; our group included 12 members (including me).
- The final dataset combining all groups' contributions and cleaned by our group is DSjobtraker.xlsx.

## Key notes
- See `pre_procrssinng.pdf` for the exact preprocessing pipeline, filtering criteria, and decisions made during cleaning (e.g., duplicate removal, normalization of technology names, handling of missing values).
- See `variable_description.pdf` for a complete list of variables and to understand how each field was extracted or derived.

## Using the dataset

R

```r
# install.packages("readxl") # run if not already installed
library(readxl)

# read the Excel file
df <- read_excel("DSjobtraker.xlsx")

# basic structure and summary
str(df)
summary(df)

# quick look at the first rows
head(df)
```

Python

```python
import pandas as pd

# read the Excel file
df = pd.read_excel("DSjobtraker.xlsx")

# basic info and summary
df.info()
df.describe(include='all')

# quick look at the first rows
df.head()
```
## Acknowledgements
Thank you to all student groups who contributed data (10 groups in total) and to the 12 members of our group who carried out collection, extraction, and cleaning.

