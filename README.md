# getting-and-cleaning-data-final-project
This repository contains the code and description for the Coursera Getting and Cleaning Data Course final project.

## Process
The process to obtain the tidy data set from the original, raw data soures in run_analysis.R is as follows:
1. The test data set is read into a data frame using the scan() function.
2. The training data set is read into a data frame using the scan() function.
3. The list of activities is read into a data frame using the read.table() function.
4. The activity column is added to the test data set by matching each integer index to the activities data set and using the scan() function.
5. The activity column is added to the training data set by matching each integer index to the activities data set and using the scan() function.
6. The subject column is added to the test data set by using the scan() function.
7. The subject column is added to the training data set by using the scan() function. 
8. The training and test data sets are combined into a single data set using the rbind() function.
9. The column names of interested are renamed using dplyr and the rename() function.
10. A new data set is created from the combined set, selecting only the rows of interest using the select() function.
11. The final tidy data set is created by grouping the new data set by the subject and activity and then taking the average of all of the remaining columns. 

## Code Book
A description of each of the variables in the final, tidy data set is given in this section.

* subject - An integer identifier of the subject being observed (1 - 30)
* activity - The activity being performed while the measurements were taken. Either LAYING, SITTING, STANDING, WALKING, WALKING_DOWNSTAIRS, WALKING_UPSTAIRS
* time_body_accelerometer_mean_(X,Y,Z) - The average of the mean accelerometer body values for the 3-axial directions
* time_body_accelerometer_std_(X,Y,Z) - The average of the standard deviation accelerometer body values for the 3-axial directions
* time_gravity_accelerometer_mean_(X,Y,Z) - The average of the mean accelerometer gravity values for the 3-axial directions
* time_gravity_accelerometer_std_(X,Y,Z) - The average of the standard deviation accelerometer gravity values for the 3-axial directions
* time_body_accelerometer_jerk_mean_(X,Y,Z) - The average of the mean accelerometer jerk signal values for the 3-axial directions
* time_body_accelerometer_jerk_std_(X,Y,Z) - The average of the standard deviation accelerometer jerk signal values for the 3-axial directions
* time_body_gyroscope_mean_(X,Y,Z) - The average of the mean gyroscope values for the 3-axial directions
* time_body_gyroscope_std_(X,Y,Z) - The average of the standard deviation gyroscope values for the 3-axial directions
* time_body_gyroscope_jerk_mean_(X,Y,Z) - The average of the mean gyroscope jerk signal values for the 3-axial directions
* time_body_gyroscope_jerk_std_(X,Y,Z) - The average of the standard deviation gyroscope jerk signal values for the 3-axial directions
* time_body_accelerometer_magnitute_mean - The average of the magnitute of the mean accelerometer body values
* time_body_accelerometer_magnitute_std - The average of the magnitute of the standard deviation accelerometer body values
* time_gravity_accelerometer_magnitute_mean - The average of the magnitute of the mean accelerometer gravity values
* time_gravity_accelerometer_magnitute_std - The average of the magnitute of the standard deviation accelerometer gravity values
* time_body_accelerometer_jerk_magnitute_mean - The average of the magnitute of the mean accelerometer jerk signal values
* time_body_accelerometer_jerk_magnitute_std - The average of the magnitute of the standard deviation accelerometer jerk signal values
* time_body_gyroscope_magnitute_mean - The average of the magnitute of the mean gyroscope body values
* time_body_gyroscope_magnitute_std - The average of the magnitute of the standard deviation gyroscope body values
* time_body_gyroscope_jerk_magnitute_mean - The average of the magnitute of the mean gyroscope jerk signal values
* time_body_gyroscope_jerk_magnitute_std - The average of the magnitute of the standard deviation gyroscope jerk signal values
* frequency_body_accelerometer_mean_(X,Y,Z) - The average of the mean accelerometer frequency domain body values for the 3-axial directions
* frequency_body_accelerometer_std_(X,Y,Z) - The average of the standard deviation accelerometer frequency domain body values for the 3-axial directions
* frequency_body_accelerometer_jerk_mean_(X,Y,Z) - The average of the mean accelerometer frequency domain jerk signal values for the 3-axial directions
* frequency_body_accelerometer_jerk_std_(X,Y,Z) - The average of the standard deviation accelerometer frequency domain jerk signal values for the 3-axial directions
* frequency_body_gyroscope_mean_(X,Y,Z) - The average of the mean gyroscope frequency domain values for the 3-axial directions
* frequency_body_gyroscope_std_(X,Y,Z) - The average of the standard deviation gyroscope frequency domain values for the 3-axial directions
* frequency_body_accelerometer_magnitute_mean - The average of the magnitute of the mean accelerometer frequency domain body values
* frequency_body_accelerometer_magnitute_std - The average of the magnitute of the standard deviation accelerometer frequency domain body values
* frequency_body_accelerometer_jerk_magnitute_mean - The average of the magnitute of the mean accelerometer frequency domain jerk signal values
* frequency_body_accelerometer_jerk_magnitute_std - The average of the magnitute of the standard deviation accelerometer frequency domain jerk signal values
* frequency_body_gyroscope_magnitute_mean - The average of the magnitute of the mean gyroscope frequency domain values
* frequency_body_gyroscope_magnitute_std - The average of the magnitute of the standard deviation gyroscope frequency domain values
* frequency_body_gyroscope_jerk_magnitute_mean - The average of the magnitute of the mean gyroscope frequency domain jerk signal values
* frequency_body_gyroscope_jerk_magnitute_std - The average of the magnitute of the standard deviation gyroscope frequency domain jerk signal values
