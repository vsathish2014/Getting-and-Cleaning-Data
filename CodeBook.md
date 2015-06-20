#Overview
The script `run_analysis.R`performs the 5 steps described in the course project's definition.

1 First, train and test data with  similar data (same number of columns and similar attribute) is merged using the `rbind()` 
function. 
2 Identified columns with the mean and standard deviation measures are taken from the whole dataset.  After extracting these columns, they are given the correct names, taken from `features.txt`.
3 Activity names and IDs from `activity_labels.txt` and they are substituted in the dataset.
4 On the whole dataset, those columns with vague column names are replaced with proper names
5 Finally, we generate a new dataset with all the average measures for each subject and activity type

# List of Variables

1 `x_train`, `y_train`, `x_test`, `y_test`, `subject_train` and `subject_test` contain the data from the downloaded files.
2 `x_data`, `y_data` and `subject_data` merge the previous datasets to further analysis.
3 `features` contains the correct names for the `x_data` dataset, which are applied to the column names stored in 
`mean_std_features`, which used to extract the desired data.
4 Similary activity names extracted through the `activities` variable.
5 `x_data`, `y_data` and `subject_data` merged to 'all_data' .
6 `averages_data` contains the relevant averages which will be later stored in a `.txt` file. 
 `ddply()` from the plyr package is used to apply `colMeans()` and ease the development.
