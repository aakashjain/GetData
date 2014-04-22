Getting and Cleaning Data - Project
===================================


run_analysis.R
--------------


This script performs the following steps:
* Forms a data frame containing features and results for each subject in the training set
* Forms a data frame containing features and results for each subject in the test set
* Combines these two into a single data frame
* Sets column names using the feature names
* Adds a column for activity labels
* Extracts from it a data frame containing mean() and std() columns for each subject
* Cleans up column names to be more readable
* Forms a tidy summary from the new data frame containing averages of each mean() and std() feature for each subject during each activity
