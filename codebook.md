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
 Body = related to body movement.
 Gravity = acceleration of gravity
 Acc = accelerometer measurement
 Gyro = gyroscopic measurements
 Jerk = sudden movement acceleration
 Mag = magnitude of movement
 
 After replacing code to variable we get
 
 #Before 	                   # After
 subject                    	 subject                                       
 activityName               	 activityName                                  
 activityNum                	 activityNum                                   
 tBodyAcc-mean()-X          	 timeBodyAccelerometer-MEAN()-X                
 tBodyAcc-mean()-Y          	 timeBodyAccelerometer-MEAN()-Y                
 tBodyAcc-mean()-Z          	 timeBodyAccelerometer-MEAN()-Z                
 tBodyAcc-std()-X           	 timeBodyAccelerometer-SD()-X                  
 tBodyAcc-std()-Y           	 timeBodyAccelerometer-SD()-Y                  
 tBodyAcc-std()-Z           	 timeBodyAccelerometer-SD()-Z                  
 tGravityAcc-mean()-X       	 timeGravityAccelerometer-MEAN()-X             
 tGravityAcc-mean()-Y       	 timeGravityAccelerometer-MEAN()-Y             
 tGravityAcc-mean()-Z       	 timeGravityAccelerometer-MEAN()-Z             
 tGravityAcc-std()-X        	 timeGravityAccelerometer-SD()-X               
 tGravityAcc-std()-Y        	 timeGravityAccelerometer-SD()-Y               
 tGravityAcc-std()-Z        	 timeGravityAccelerometer-SD()-Z               
 tBodyAccJerk-mean()-X      	 timeBodyAccelerometerJerk-MEAN()-X            
 tBodyAccJerk-mean()-Y      	 timeBodyAccelerometerJerk-MEAN()-Y            
 tBodyAccJerk-mean()-Z      	 timeBodyAccelerometerJerk-MEAN()-Z            
 tBodyAccJerk-std()-X       	 timeBodyAccelerometerJerk-SD()-X              
 tBodyAccJerk-std()-Y       	 timeBodyAccelerometerJerk-SD()-Y              
 tBodyAccJerk-std()-Z       	 timeBodyAccelerometerJerk-SD()-Z              
 tBodyGyro-mean()-X         	 timeBodyGyroscope-MEAN()-X                    
 tBodyGyro-mean()-Y         	 timeBodyGyroscope-MEAN()-Y                    
 tBodyGyro-mean()-Z         	 timeBodyGyroscope-MEAN()-Z                    
 tBodyGyro-std()-X          	 timeBodyGyroscope-SD()-X                      
 tBodyGyro-std()-Y          	 timeBodyGyroscope-SD()-Y                      
 tBodyGyro-std()-Z          	 timeBodyGyroscope-SD()-Z                      
 tBodyGyroJerk-mean()-X     	 timeBodyGyroscopeJerk-MEAN()-X                
 tBodyGyroJerk-mean()-Y     	 timeBodyGyroscopeJerk-MEAN()-Y                
 tBodyGyroJerk-mean()-Z     	 timeBodyGyroscopeJerk-MEAN()-Z                
 tBodyGyroJerk-std()-X      	 timeBodyGyroscopeJerk-SD()-X                  
 tBodyGyroJerk-std()-Y      	 timeBodyGyroscopeJerk-SD()-Y                  
 tBodyGyroJerk-std()-Z      	 timeBodyGyroscopeJerk-SD()-Z                  
 tBodyAccMag-mean()         	 timeBodyAccelerometerMagnitude-MEAN()         
 tBodyAccMag-std()          	 timeBodyAccelerometerMagnitude-SD()           
 tGravityAccMag-mean()      	 timeGravityAccelerometerMagnitude-MEAN()      
 tGravityAccMag-std()       	 timeGravityAccelerometerMagnitude-SD()        
 tBodyAccJerkMag-mean()     	 timeBodyAccelerometerJerkMagnitude-MEAN()     
 tBodyAccJerkMag-std()      	 timeBodyAccelerometerJerkMagnitude-SD()       
 tBodyGyroMag-mean()        	 timeBodyGyroscopeMagnitude-MEAN()             
 tBodyGyroMag-std()         	 timeBodyGyroscopeMagnitude-SD()               
 tBodyGyroJerkMag-mean()    	 timeBodyGyroscopeJerkMagnitude-MEAN()         
 tBodyGyroJerkMag-std()     	 timeBodyGyroscopeJerkMagnitude-SD()           
 fBodyAcc-mean()-X          	 frequencyBodyAccelerometer-MEAN()-X           
 fBodyAcc-mean()-Y          	 frequencyBodyAccelerometer-MEAN()-Y           
 fBodyAcc-mean()-Z          	 frequencyBodyAccelerometer-MEAN()-Z           
 fBodyAcc-std()-X           	 frequencyBodyAccelerometer-SD()-X             
 fBodyAcc-std()-Y           	 frequencyBodyAccelerometer-SD()-Y             
 fBodyAcc-std()-Z           	 frequencyBodyAccelerometer-SD()-Z             
 fBodyAccJerk-mean()-X      	 frequencyBodyAccelerometerJerk-MEAN()-X       
 fBodyAccJerk-mean()-Y      	 frequencyBodyAccelerometerJerk-MEAN()-Y       
 fBodyAccJerk-mean()-Z      	 frequencyBodyAccelerometerJerk-MEAN()-Z       
 fBodyAccJerk-std()-X       	 frequencyBodyAccelerometerJerk-SD()-X         
 fBodyAccJerk-std()-Y       	 frequencyBodyAccelerometerJerk-SD()-Y         
 fBodyAccJerk-std()-Z       	 frequencyBodyAccelerometerJerk-SD()-Z         
 fBodyGyro-mean()-X         	 frequencyBodyGyroscope-MEAN()-X               
 fBodyGyro-mean()-Y         	 frequencyBodyGyroscope-MEAN()-Y               
 fBodyGyro-mean()-Z         	 frequencyBodyGyroscope-MEAN()-Z               
 fBodyGyro-std()-X          	 frequencyBodyGyroscope-SD()-X                 
 fBodyGyro-std()-Y          	 frequencyBodyGyroscope-SD()-Y                 
 fBodyGyro-std()-Z          	 frequencyBodyGyroscope-SD()-Z                 
 fBodyAccMag-mean()         	 frequencyBodyAccelerometerMagnitude-MEAN()    
 fBodyAccMag-std()          	 frequencyBodyAccelerometerMagnitude-SD()      
 fBodyBodyAccJerkMag-mean() 	 frequencyBodyAccelerometerJerkMagnitude-MEAN()
 fBodyBodyAccJerkMag-std()  	 frequencyBodyAccelerometerJerkMagnitude-SD()  
 fBodyBodyGyroMag-mean()    	 frequencyBodyGyroscopeMagnitude-MEAN()        
 fBodyBodyGyroMag-std()     	 frequencyBodyGyroscopeMagnitude-SD()          
 fBodyBodyGyroJerkMag-mean()	 frequencyBodyGyroscopeJerkMagnitude-MEAN()    
 fBodyBodyGyroJerkMag-std() 	 frequencyBodyGyroscopeJerkMagnitude-SD()      

