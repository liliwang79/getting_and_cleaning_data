# getting_and_cleaning_data
collect, work with, and clean Human Activity Recognition Using Smartphones Data Set 
The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 1) a tidy data set as described below, 2) a link to a Github repository with your script for performing the analysis, and 3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.

One of the most exciting areas in all of data science right now is wearable computing - see for example this article . Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Here are the data for the project:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

You should create one R script called run_analysis.R that does the following.

Merges the training and the test sets to create one data set.
Extracts only the measurements on the mean and standard deviation for each measurement. 
Uses descriptive activity names to name the activities in the data set
Appropriately labels the data set with descriptive variable names. 
Creates a second, independent tidy data set with the average of each variable for each activity and each subject. 
Good luck!

run_analysis.R: downloads all the required files to complete this assignment and creates a big file mean_and_std.csv and a small file tidy_dataset.csv (both are stored in /results)

Codebook
downloads required data from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
unzips the file if it has not been uncompressed
creates results folder if it does not exist (all files are stored in this folder)
loads features.txt used for columns
loads X_train.txt, y_train.txt, subject_train.txt
X_train contains the data using the feature data set as columns
y_train contains the activity labels
subject_train contains the ids
loads and appends test dataset using X_test.txt, y_test.txt, subject_test.txt
X_test contains the data using the feature data set as columns
y_test contains the activity labels
subject_test contains the ids
appends train and test data
rearrange the data using id
loads activity_labels.txt
changes the data activity row to use the activity labels
saves the mean and std into mean_and_std.csv
saves the tidy dataset into tidy_dataset.csv

mean_and_std.csv
contains 1 0300 (including header) rows and 82 columns (including enumeration column) in a default csv format
variables:

id
activity
tBodyAcc.std...X
tBodyAcc.std...Y
tBodyAcc.std...Z
tGravityAcc.std...X
tGravityAcc.std...Y
tGravityAcc.std...Z
tBodyAccJerk.std...X
tBodyAccJerk.std...Y
tBodyAccJerk.std...Z
tBodyGyro.std...X
tBodyGyro.std...Y
tBodyGyro.std...Z
tBodyGyroJerk.std...X
tBodyGyroJerk.std...Y
tBodyGyroJerk.std...Z
tBodyAccMag.std..
tGravityAccMag.std..
tBodyAccJerkMag.std..
tBodyGyroMag.std..
tBodyGyroJerkMag.std..
fBodyAcc.std...X
fBodyAcc.std...Y
fBodyAcc.std...Z
fBodyAccJerk.std...X
fBodyAccJerk.std...Y
fBodyAccJerk.std...Z
fBodyGyro.std...X
fBodyGyro.std...Y
fBodyGyro.std...Z
fBodyAccMag.std..
fBodyBodyAccJerkMag.std..
fBodyBodyGyroMag.std..
fBodyBodyGyroJerkMag.std..
tBodyAcc.mean...X
tBodyAcc.mean...Y
tBodyAcc.mean...Z
tGravityAcc.mean...X
tGravityAcc.mean...Y
tGravityAcc.mean...Z
tBodyAccJerk.mean...X
tBodyAccJerk.mean...Y
tBodyAccJerk.mean...Z
tBodyGyro.mean...X
tBodyGyro.mean...Y
tBodyGyro.mean...Z
tBodyGyroJerk.mean...X
tBodyGyroJerk.mean...Y
tBodyGyroJerk.mean...Z
tBodyAccMag.mean..
tGravityAccMag.mean..
tBodyAccJerkMag.mean..
tBodyGyroMag.mean..
tBodyGyroJerkMag.mean..
fBodyAcc.mean...X
fBodyAcc.mean...Y
fBodyAcc.mean...Z
fBodyAcc.meanFreq...X
fBodyAcc.meanFreq...Y
fBodyAcc.meanFreq...Z
fBodyAccJerk.mean...X
fBodyAccJerk.mean...Y
fBodyAccJerk.mean...Z
fBodyAccJerk.meanFreq...X
fBodyAccJerk.meanFreq...Y
fBodyAccJerk.meanFreq...Z
fBodyGyro.mean...X
fBodyGyro.mean...Y
fBodyGyro.mean...Z
fBodyGyro.meanFreq...X
fBodyGyro.meanFreq...Y
fBodyGyro.meanFreq...Z
fBodyAccMag.mean..
fBodyAccMag.meanFreq..
fBodyBodyAccJerkMag.mean..
fBodyBodyAccJerkMag.meanFreq..
fBodyBodyGyroMag.mean..
fBodyBodyGyroMag.meanFreq..
fBodyBodyGyroJerkMag.mean..
fBodyBodyGyroJerkMag.meanFreq..
tidy_dataset.csv.csv
contains 181 rows (including header) and 82 columns (including enumeration column) in a default csv format

variables:

id
activity
tBodyAcc.std...X_mean
tBodyAcc.std...Y_mean
tBodyAcc.std...Z_mean
tGravityAcc.std...X_mean
tGravityAcc.std...Y_mean
tGravityAcc.std...Z_mean
tBodyAccJerk.std...X_mean
tBodyAccJerk.std...Y_mean
tBodyAccJerk.std...Z_mean
tBodyGyro.std...X_mean
tBodyGyro.std...Y_mean
tBodyGyro.std...Z_mean
tBodyGyroJerk.std...X_mean
tBodyGyroJerk.std...Y_mean
tBodyGyroJerk.std...Z_mean
tBodyAccMag.std.._mean
tGravityAccMag.std.._mean
tBodyAccJerkMag.std.._mean
tBodyGyroMag.std.._mean
tBodyGyroJerkMag.std.._mean
fBodyAcc.std...X_mean
fBodyAcc.std...Y_mean
fBodyAcc.std...Z_mean
fBodyAccJerk.std...X_mean
fBodyAccJerk.std...Y_mean
fBodyAccJerk.std...Z_mean
fBodyGyro.std...X_mean
fBodyGyro.std...Y_mean
fBodyGyro.std...Z_mean
fBodyAccMag.std.._mean
fBodyBodyAccJerkMag.std.._mean
fBodyBodyGyroMag.std.._mean
fBodyBodyGyroJerkMag.std.._mean
tBodyAcc.mean...X_mean
tBodyAcc.mean...Y_mean
tBodyAcc.mean...Z_mean
tGravityAcc.mean...X_mean
tGravityAcc.mean...Y_mean
tGravityAcc.mean...Z_mean
tBodyAccJerk.mean...X_mean
tBodyAccJerk.mean...Y_mean
tBodyAccJerk.mean...Z_mean
tBodyGyro.mean...X_mean
tBodyGyro.mean...Y_mean
tBodyGyro.mean...Z_mean
tBodyGyroJerk.mean...X_mean
tBodyGyroJerk.mean...Y_mean
tBodyGyroJerk.mean...Z_mean
tBodyAccMag.mean.._mean
tGravityAccMag.mean.._mean
tBodyAccJerkMag.mean.._mean
tBodyGyroMag.mean.._mean
tBodyGyroJerkMag.mean.._mean
fBodyAcc.mean...X_mean
fBodyAcc.mean...Y_mean
fBodyAcc.mean...Z_mean
fBodyAcc.meanFreq...X_mean
fBodyAcc.meanFreq...Y_mean
fBodyAcc.meanFreq...Z_mean
fBodyAccJerk.mean...X_mean
fBodyAccJerk.mean...Y_mean
fBodyAccJerk.mean...Z_mean
fBodyAccJerk.meanFreq...X_mean
fBodyAccJerk.meanFreq...Y_mean
fBodyAccJerk.meanFreq...Z_mean
fBodyGyro.mean...X_mean
fBodyGyro.mean...Y_mean
fBodyGyro.mean...Z_mean
fBodyGyro.meanFreq...X_mean
fBodyGyro.meanFreq...Y_mean
fBodyGyro.meanFreq...Z_mean
fBodyAccMag.mean.._mean
fBodyAccMag.meanFreq.._mean
fBodyBodyAccJerkMag.mean.._mean
fBodyBodyAccJerkMag.meanFreq.._mean
fBodyBodyGyroMag.mean.._mean
fBodyBodyGyroMag.meanFreq.._mean
fBodyBodyGyroJerkMag.mean.._mean
fBodyBodyGyroJerkMag.meanFreq.._mean
