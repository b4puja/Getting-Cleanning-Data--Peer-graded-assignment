###Getting & Cleaning Data###

Source of the original data: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Original description: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

The attached R script (run_analysis.R) performs the following to clean up the data:
Merging all data in one set, variable like y_train, subject_train, x_train are merged to form mrg_train and y_test, subject_test, x_test to form mrg_test. we select all to form setAllInOne.

Read the columns names and create vector for defining ID, mean and standard deviation. The variables used are:

activityId
subjectId
mean
std

Then we made necessary subset from setAllInOne then descriptive activity names were used to name the activity in the data set.

Finally 2nd tidy data set was made using subjectId, activityId , setWithActivityNames & mean and we wrote tidy data set using write.table.