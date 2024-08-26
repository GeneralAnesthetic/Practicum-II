# Practicum-II

# This code explores Predictive Modeling with CMS Audit Data.

# I chose the two files that contained the best/most-useful audit columns from https://data.cms.gov/provider-data/topics/dialysis-facilities
# Examining the datasets, these two files are "COMPLETE_QIP_DATA.csv" & "DFC_FACILITY.csv". The others are incomplete portions of "COMPLETE_QIP_DATA", or they do not contain useful information (i.e. "CLINICAL_DEPRESSION")

# The dataset’s range is from October 2022 - September 2023  

# Data Cleaning: naturally, some columns, from the combined dataset, were found to be valuable for displaying graphs, but not for Machine Learning. Also, some values were 'Not Rated', or were given unusable values such '<30'. These were dropped, in the former example, or imputed, in the latter example. 

# Imputation: also, some columns were missing too many values. So, they were dropped. Luckily, most were not the most pertinent columns for ML. However, values within columns that were not missing too many values, but were still missing audit entries, were imputed/estimated with KNN. 

# ML Pipeline: a series of predictive/classification algorithms were used to find the best performing model. In this case, SVC and Random Forrest were tried. 

# EDA: Exploratory Data Analysis. CA had the highest Performance Score. Texas had the second. 

# 'SVC’ and ‘Random Forrest’ received decent accuracies. ‘SVC’ was used to predict ‘Total (Audit) Performance Scores’ and ‘Random Forrest’ classified ‘Mortality Rates’.
# SVC received 73%
# Random Forrest received 93%

# These models can be used within a platform/application (i.e. Salesforce) to predict when a facility will, or will not, be likely to achieve high performance scores or high mortality rates. These predications can be run continuously. 

# Going forward, a facility's internal datasets can be further broken down, or ‘segmented’ into patient types (fistula, calcium ranges, etc.) for more impactful results. And, of course, more algorithms can be explored. 

