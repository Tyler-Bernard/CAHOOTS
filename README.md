# CAHOOTS
Data analysis for class working with CAHOOTS data

---------------------------------------------------------------------------

This project is broken up into 3 parts:

Data Cleaning

Temporal Data Analysis 

Location Data Analysis

The following README will be in that order.

-----------------------------------------------------------------------

Prerequisites- Python 3.X !!!!!!!!!!!!!!!!!!!!!!!!!!!!

Ensure you have the following Python libraries installed:

pandas,
numpy,
seaborn,
matplotlib,
scipy,
scikit-learn

!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

-----------------------------------------------------------------------

Data Cleaning:

Overview:
This script involves cleaning and analyzing call data from the Computer-Aided Dispatch (CAD) system. The data is sourced from two files: a CSV file (call_data_from_CAD.csv) and an Excel file (call_data_from_CAD_2022.xlsx). The cleaning focuses on identifying unique unit call signs containing specific patterns, filtering data based on certain criteria, and comparing call counts across different years.

Files

"insert data here".csv: Contains call data from previous years.

"insert data here".xlsx: Contains call data specifically from the year 2022.

output.csv: The output CSV file containing cleaned and filtered call data.

Steps

-Loading Data

  Read the CSV and Excel files into pandas DataFrames.
  
-Pre-cleaning

  Removal of unnessesary characters and locating associated call signs
  
-Checking usefulness of small CAD dataset (2022-2023)

  Ratio analysis of the total call count between datasets
  
-Final Cleaning

  Removal of years not used in analysis and formatting data of relevant dataset

  -----------------------------------------------------------------------

Temporal Data Analysis:

Overview
This script involves analyzing call time distribution data across hour, month and year. The data is sourced from the output of the data cleaning file: (output.csv). The analysis focuses on a data visualization of distributions and a Spearman's correlation analysis with bootstrapping. 

Files

output.csv: The main CSV file containing the call data.

Steps

-Loading Data

  Read the CSV file into pandas DataFrame.
  
-Plotting of Distributions for Hour, Year and Month

  Seaborn countplots are made for the call time distribution for months, hours, and years in the data
  
-Plotting of Hour and Month by Each Year

  Seaborn lineplots are made to show more detail between distributions as they change over years
  
-Plotting of Distribution of Hours in July

  Seaborn lineplot for a more detailed look at a time of interest according to previous graphs
  
-Calculation of Percent Change in Calls Day to Day

  Scatterplot is shown to represent the percent change in call volume day to day across whole dataset.
  
-Test for Normality

  Several checks, histogram, Q-Q plot and Shapiro-Wilk test, are used to see if data is normally distributed
  
-Spearman's Correlation Analysis

  Bootstrapping and confidence interval for correlation analysis, results are shown on subplots

  -----------------------------------------------------------------------

Location Data Analysis:

Overview
This script performs a detailed analysis of call data from a CAD (Computer-Aided Dispatch) system, focusing on various metrics such as call distribution by zip code, hourly and monthly trends, and the correlation of call percentage changes across different years and zip codes.

Files

output.csv: The main CSV file containing the call data.

Steps

-Loading Data

  Read the CSV file into pandas DataFrame.
  
-Plot Distribution of Zip Codes Across Years (Cleaning)

  Filter zip codes that do not contain relevant years for analysis
  
-Plotting of Hour and Month by Each Zip Code

  Seaborn lineplots are made to show more detail between distributions as they change over zip codes
  
-Spearman's Correlation Analysis

  Bootstrapping and confidence interval for correlation analysis, results are shown on subplots
  
  


