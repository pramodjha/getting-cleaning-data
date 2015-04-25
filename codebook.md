Getting and Cleaning Data Project

Description

Additional information about the variables, data and transformations used in the course project for the Johns Hopkins Getting and Cleaning Data course.

Source Data

A full description of the data used in this project can be found at The UCI Machine Learning Repository

Data Set Information

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

# Get the Data in R
 Getting data from given url by using "download.file" function

# download the file and store in directory
 Storing data into working directory for further manipulation
  
# Unzip the file
 unzip the file using "unzip" function in order to extract all the file which are compressed in zip folder
  
Getting list of unziped file from "UCHI HAR dataset"
 Checking list of files in "UCHI HAR dataset folder"
  
# Reading data from files into variable
  Reading following files by storing into variable
    features.txt
    activity_labels.txt
    subject_train.txt
    x_train.txt
    y_train.txt
    subject_test.txt
    x_test.txt
    y_test.txt

# binding row by using rbind 
  By using rbind row of subject_test.txt & subject_train.txt are binded and table created called "data_subject"
  similarly row of y_test.txt & y_train.txt are binded into one table called "data_activity"
  and row of  X_test.txt & X_train.txt are binded and formed tabled called "data_feature"
  
  by binding row three tables are created 1) "data_subject" 2) "data_activity" 3) "data_feature"
  
# set_variable
  Setting header for variables by uisng "names" function
  
# Combine Column by using cbind
  Column for each table created above are combine by using function called "cbind"
  
# Subset Name of Features by measurements on the mean and standard deviation
  As we required only column with mean and stadard deviation so we created subset of data with same specification
  
# Subset the data frame Data by seleted names of Features
  
  
# Read descriptive activity names from “activity_labels.txt
  Assigning  lables from activity labels.txt files
  
# Appropriately labels the data set with descriptive variable names
  As one of the important component of tidydata is to have descriptive variable name of a variable there for proper labels are assinged to it.
