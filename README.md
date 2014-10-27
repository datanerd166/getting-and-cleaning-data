### Introduction

This repository is for Getting and Cleaning Data Course Project, which is 
an important component of the course. The purpose of this project is to demonstrate 
the ability to collect, work with, and clean a data set. The goal is to prepare tidy
data that can be used for later analysis.

### Instructions
Create one R script called run_analysis.R that performs the following tasks:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set.
4. Appropriately labels the data set with descriptive variable names.
5. From the data set in step 4, create a second, independent tidy data set with the average
of each variable for each activity and each subject.

### Data Set
Human Activity Recognition Using Smartphones Data Set is used for this project. The data set 
is in a folder called UCI HAR Dataset. It contains test and train data set sub-folders, 
activity_labels, features, features_info and README files.
The data set can be downloaded from:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

### run_analysis.R Features
run_analysis.R verifies the runtime environment and handles package dependencies automatically.
It also verifies data set path to ensure that the correct path information is provided; otherwise,
the execution is stopped with an error message. When the execution is completed, a tidy_data.txt 
file is generated and stored in the data set folder.

### Run run_analysis.R
Please follow the steps described below to run run_analysis.R script:

1. Download the data set, unzip the .zip file to a folder on your local drive. Record the path
leading to the data set folder.
2. Download the run-analysis.R and place it in a folder on your local drive, or your RStudio working 
directory.
3. In RStudio, first run source("run_analysis.R) command, followed by run_analysis(data_set_path)
4. A tidy data set created by the script, called tidy_data.txt file will be created in the 
UCI HAR Dataset folder.


