Getting and Cleaning Data - Project
===================================

run_analysis.R
--------------
Forms and stores a tidy summary of the given data. 
This script performs the following steps:
* Forms a data frame containing features and results for each subject in the training set
* Forms a data frame containing features and results for each subject in the test set
* Combines these two into a single data frame
* Sets column names using the feature names
* Adds a column for activity labels
* Extracts from it a data frame containing mean() and std() columns for each subject
* Cleans up column names to be more readable
* Forms a tidy summary from the new data frame containing averages of each mean() and std() feature for each subject during each activity

Results:
* `data` - Contains the combined data of the training and test sets.
* `meansDevs` - Contains only mean and standard deviation columns for each subject.
* `dataSummary` - Contains averages of mean and standard deviation values for each combination of activity and subject. It is written to `data_summary.txt` in the given data folder.

Points of note:
* For `meansDevs` and `dataSummary`, the cryptic feature names are modified into more readable and meaningful [camelCase](http://en.wikipedia.org/wiki/CamelCase) names.
* The activity labels are not of the character class but of the factor class, for easier grouping operations in the future. A side effect of this is that underscores have been left in (eg. `WALKING_UPSTAIRS` instead of `WALKING UPSTAIRS`) because using spaces would cause confusion among factor levels, as follows:

`> head(dataSummary$activity)
[1] LAYING LAYING LAYING LAYING LAYING LAYING
Levels: LAYING SITTING STANDING WALKING WALKING_DOWNSTAIRS WALKING_UPSTAIRS`

