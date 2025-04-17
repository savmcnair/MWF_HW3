# MWF_HW3
Homework 3 Modern Workflows in Data Science


**Project Summary**

This project will be an exploration of the change in covid cases by country over time using Spark in R. We will pull data directly from a GitHub repository online using a spark. This repository contains Johns Hopkins database of daily logs of COVID-19 cases internationally. It also has some metadata on each country including population. We will explore how country, population, and case #/case rate are interrelated through graphs and ML regression models to evaluate the predictive power of each of these components. 

**There are a few sections of this project:**
1. Setting up a local spark server in R and connecting it. 
 
2. Pulling data from online (at https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/UID_ISO_FIPS_LookUp_Table.csv and https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_global.csv) into the spark server and downloading it to our repository. These files are named "lookup.csv" and "confirmed_global.csv".

3. Manipulating the data to be usable in long form so we can do timeseries analyses. 

4. Plotting the data as case rate over time by country and case number over time by country. This section has graphs and interpretations for the user.

5. Running a ML linear regression to explain the log number of cases using country, population size, and days since the start of the pandemic. This section has graphs and interpretations for the user.


**Repository organization**

data folder: has the data downloaded via spark for this project: cases by country daily and metadata by country.
output: has the rmarkdown pdf output report.
script: has the master script for creating the spark server and developing the report on COVID cases internationally over time. 

**Below are details for the session info for reproducibility:**

Below is the session info for this R Markdown script, the packages needed, dependencies, and Rversion, platform, and OS so one can reproduce the use of this script exactly:

R version 4.3.1 (2023-06-16 ucrt) Platform: x86_64-w64-mingw32/x64 (64-bit) Running under: Windows 11 x64 (build 26100)

Matrix products: default

locale: [1] LC_COLLATE=English_United States.utf8 LC_CTYPE=English_United States.utf8 LC_MONETARY=English_United States.utf8 [4] LC_NUMERIC=C LC_TIME=English_United States.utf8

time zone: America/New_York tzcode source: internal

attached base packages: [1] stats graphics grDevices utils datasets methods base

other attached packages: [1] lubridate_1.9.3 ggplot2_3.4.4 tidyr_1.3.0 dplyr_1.1.4