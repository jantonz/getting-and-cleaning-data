# getting-and-cleaning-data
Repository for the course project of Getting and Cleaning Data

run_analysis.R is written as an R function with no arguments. It's called by sourcing the "run_analysis.R" file and calling it by "run_analysis()". 

It first loads the required packages ("dplyr" and "tidyr"). Then it follows the steps provided in the Coursera course project description:

Firs it reads all data sets and loads them into R variables.
Then it merges the training and the test sets with r_bind.
After that, it labels the columns with "subject", "activity", and the names provided in the features.txt file.
Then it extracts only the measurements on the mean and standard deviation (that is, the columns with "mean" or "std" in their name).
Then it names the activities (1 to 6) as walking", "walking_upstairs", "walking_downstairs", "sitting", "standing", "laying", as provided in the "activity_labels.txt" file.
After that, it groups the data set by activity and subject and extracts the mean for each activity and subject combination (180 combinations = 180 rows) with summarise_each function.
Finally, it creates a text file called "data_avg.txt" with write.table using row.names=FALSE.
