### Code Book

This is a code book for the Getting and Cleaning Data Course project. It describes the variables, the data set, and any transformation or work that have been performed to clean up the Human Activity Recognition Using Smartphones Data Set.

### Data Set
Human Activity Recognition Using Smartphones Data Set:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

A full description is available at the site where the data was obtained:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 

### Data Set Description
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

### Data Set Structure

The data set is in a folder called UCI HAR Dataset. It includes:
- README.txt: Description of the data set

- features_info.txt: Information about the variables used on the feature vector.

- features.txt: List of all features.

- activity_labels.txt: Links the class labels with their activity name.

- train/X_train.txt: Training set.

- train/y_train.txt: Training labels.

- test/X_test.txt: Test set.

- test/y_test.txt: Test labels.

The following files are available for the train and test data. Their descriptions are equivalent. 

- train/subject_train.txt: Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 

- train/Inertial Signals/total_acc_x_train.txt: The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis. 

- train/Inertial Signals/body_acc_x_train.txt: The body acceleration signal obtained by subtracting the gravity from the total acceleration. 

- train/Inertial Signals/body_gyro_x_train.txt: The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second. 

### Transformation

1. Read in  test/X_test.txt, train/X_train.txt, test/y_test.txt, train/y_train.txt, test/subject_test.txt and train/subject_train.txt 
2. Merge test and train data set by performing rbind operation on X_test and X_train, y_test and y_train, and subject_test and subjext_train to create three data objects: X, y and subject.
3. Transform y to test label factor by specifying activity labels.
4. Merge three data objects by performing cbind operation on X, y factor and subject to create one data frame object.
4. Assign descriptive column names to the data object using features.
5. Extract the measurements on the mean and standard deviation for each measurement from the data frame object.
6. Create an independent tidy data set with the average of each variable for each activity and each subject.
