# Pandas Challenge - PyCitySchools  
`Module 4`  
`EdX(2U) & UT Data Analytics and Visualization Bootcamp`  
`Cohort UTA-VIRT-DATA-PT-11-2024-U-LOLC`  
`By Neel Kumar Agarwal`  

## Table of Contents  
1. [Introduction](#introduction)  
2. [Challenge Overview](#challenge-overview)  
3. [Variables/Breakdowns](#variablesbreakdowns)  
    - [Relevant Variants](#relevant-variants)  
    - [Summary Breakdowns](#summary-breakdowns)  
4. [Setup and Usage](#setup-and-usage)  
5. [Expected Results](#expected-results)  
6. [Files and Directory Structure](#files-and-directory-structure)  
7. [Final Analysis](#final-analysis)  

## Introduction  
You are the new Chief Data Scientist for your city's school district. In this  
capacity, you'll be helping the school board and mayor make strategic decisions  
regarding future school budgets and priorities.  

As a first task, you've been asked to analyze the district-wide standardized test  
results. You'll be given access to every student's math and reading scores, as  
well as various information on the schools they attend. Your task is to aggregate  
the data to showcase obvious trends in school performance.  

## Challenge Overview  
The PyCitySchools .ipynb is a Python-interactive Jupyter notebook that aims to  
find global and local trends of district, school, and student standardized testing  
scores. My job was to take data presented in cleaned CSV file format and extract  
relevant information from it to produce snapshots of different variants and their  
relationally aggregated data.  

PyCitySchools runs using a conda based local python environment. Python version  
used is `3.12.7` running with dependencies of Pandas and pathlib. Two clean CSV  
files, one containing school data and the other student data, were imported and  
read into 2 Pandas DataFrame objects. Minor data validation was performed but not  
needed. The two DataFrames (DFs) were then merged on their shared factor which was  
the school name they contained. A complete DF of both CSV files was then usable  
after tidying. This complete DF was used in the entirety of the Jupyter Notebook to  
create new DFs that held concise summary information of each comparison. After each  
comparison is made an image of it is saved to `PyCitySchools/snapshots/<image-name>`.  

The task at hand is to compare how successful students and schools are, dependently  
and independently, at standardized tests for reading and mathematics. Instances in  
which both tests are passed are also found taken into account.  

> [!NOTE]
> No citations are needed for this project save for the code, data, and assigned  
> conditions given by edX (2U) given for use of learning in this bootcamp.  

## Variables/Breakdowns  
### Relevant Variants:  
```
- School_Name  
    - Type (District/Charter)
    - Size
    - Budget
- Student_Name  
    - Gender (M/F)
    - Grade (9-12)
    - Reading Score
    - Math Score
```
### Summary Breakdowns:  
```
|- District Summary
|- School Summary
|- Highest-Performing School (by % Overall Passing)
|- Bottom-Performing Schools (by % Overall Passing)
|- Math Scores by Grade
|- Reading Scores by Grade
|- Scores by School Spending
|- Scores by School Size
|- Scores by School Type
```

## Setup and Usage  
### Prerequisites  
- Python 3.x  
- Standard libraries: `pandas` and `pathlib` (included with Python)
- Non-standard libarary: `dataframe_image`
- IDE that supports Jupyter Notebooks with Python  

### Instructions  
1. Clone this repository.  
2. Ensure IDE is up to date and running.  
3. Please run the following code if the library references aren't found:
    ```
    pip install pandas
    pip install pathlib
    pip install dataframe-image
    ```
4. Ensure the input CSV files are in the `Resources` folder.  
5. Open `main.ipynb` in your IDE and run all cells.  
6. Results will print throughout the Jupyter Interactive Notebook 
7. Results are then exported in .png format in new `snapshots` directory
> [!TIP]  
> Collapsing of various regions or use of `OUTLINE` in  
> VSCode can speed up exploration.  

### Limitations  
- [ ]Results are qualitative not quantitative  
- [x] Qualitative information is not the most accessable in such a large notebook  
    - Exportation of images created  


## Files and Directory Structure  
```
pandas-challenge/
|
|— PyCitySchools/
|   |— Resources/
|   |   — schools_complete.csv
|   |   - students_complete.csv
|   |— main.ipynb
```
This structure ensures all inputs are organized within their respective folders.  
Outputs will be created without additional directory structuring  


## Expected Results  
1. Updated Jupyter Notebook DataFrames and printed DataFrames
2. New directory structure for `pandas-challenge/`:
```
pandas-challenge/
|
|— PyCitySchools/
|   |— Resources/
|   |   — schools_complete.csv
|   |   - students_complete.csv
|   |- snapshots/
|   |   - bottomPerforming_byOverallPassing.png
|   |   - district_snapshot.png
|   |   - mathScores_byGrade.png
|   |   - perSchool_summary.png
|   |   - readScores_byGrade.png
|   |   - scores_bySchoolType.png
|   |   - scores_bySize.png
|   |   - scores_bySpending.png
|   |   - topPerforming_byOverallPassing.png
|   |— main.ipynb (updated)
```
New directory paths indicate proper running and exporting of DataFrames.

---
## Final Analysis:  
```
Using Pandas and Jupyter Notebook, create a report that includes the following data.
Your report must include a written description of at least two observable trends based on the data.
Summarizes the analysis (5 points)
Draws two correct conclusions or comparisons from the calculations (10 points)
```
1. per_spending_summary --> Shows how groups of bins of $585-630 and $630-645 spending amounts had lower overall success in all categories. However, $630-645 did the worst. Additionally, while reading scores normally aren't impacted the reading scores here are impacted highly as well as math.
2. mathScores_by_grade --> Math scores are typically lower than reading scores and therefore have the highest variability, lending to the most drastic changes in % Overall Passing
3. District v. charter also seems to draw a trend in mathematical success

