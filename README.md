# PyCitySchools School & Student Analysis
> Neel Agarwal

## Given Task:
You are the new Chief Data Scientist for your city's 
school district. In this capacity, you'll be helping
the school board and mayor make strategic decisions 
regarding future school budgets and priorities.

As a first task, you've been asked to analyze the 
district-wide standardized test results. You'll be 
given access to every student's math and reading 
scores, as well as various information on the schools 
they attend. Your task is to aggregate the data to 
showcase obvious trends in school performance.


## Description:
The PyCitySchools .ipynb is a Python-interactive 
Jupyter notebook that aims to find global and local 
trends of district, school, and student standardized 
testing scores. My job was to take data presented to 
me in cleaned CSV file format and extract relevant 
information from it to produce snapshots of different 
variants and their relationally aggregated data.

PyCitySchools runs using a conda based local python 
environment. Python version used is 3.12.7 running 
with dependencies of Pandas and pathlib. Two clean CSV 
files, one containing school data and the other student 
data, were imported and read into 2 Pandas DataFrame 
objects. Minor data validation was performed but not 
needed. The two DataFrames (DFs) were then merged on their 
shared factor which was the school name they contained. 
A complete DF of both CSV files was then usable after 
tidying. This complete DF was used in the entirety of 
the Jupyter Notebook to create new DFs that held concise
summary information of each comparison.

The task at hand is to compare how successful students 
and schools are, dependently and independently, at 
standardized tests for reading and mathematics. Instances
in which both tests are passed are also found taken into
account.

## Relevant variants include:
```
- School
    - Type (District/Charter)
    - Size
    - Budget
- Student
    - Gender (M/F)
    - Grade (9-12)
    - Reading Score
    - Math Score
```

## The breakdowns included are:
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

Limitations:
- Qualitative not quantitative
- Qualitative information is not easily accessable in such a large notebook
- Exportation of snapshots should be implemented for quick access


Analysis:
---------
