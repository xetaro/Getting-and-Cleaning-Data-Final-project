Description of DATA
======================================
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

For each record it is provided:
======================================

- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

The dataset includes the following files:
=========================================

- 'README.txt'

- 'features_info.txt': Shows information about the variables used on the feature vector.

- 'features.txt': List of all features.

- 'activity_labels.txt': Links the class labels with their activity name.

- 'train/X_train.txt': Training set.

- 'train/y_train.txt': Training labels.

- 'test/X_test.txt': Test set.

- 'test/y_test.txt': Test labels.

The following files are available for the train and test data. Their descriptions are equivalent. 

- 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 

- 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis. 

- 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration. 

- 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second. 

Notes: 

- Features are normalized and bounded within [-1,1].
- Each feature vector is a row on the text file.
- The units used for the accelerations (total and body) are 'g's (gravity of earth -> 9.80665 m/seg2).
- The gyroscope units are rad/seg.
- A video of the experiment including an example of the 6 recorded activities with one of the participants can be seen in the following link: http://www.youtube.com/watch?v=XOEN9W05_4A

For more information about this dataset please contact: activityrecognition '@' smartlab.ws


Transformation:
======
1.Set working directory

2.Download the file and put the file in the data folder

3.Unzip the file

4.Unzipped files are in the folderUCI HAR Dataset and get the list of the files

5.Read the Activity, Subject and Fearures files

6.Merges the training and the test sets

7.Extracts only the measurements on the mean and standard deviation for each measurement

8.Create a new data frame by finding the mean for each combination of subject and label. It's done by
  aggregate() function
  
9.Write the new tidy set into a text file called tidy2.txt




Variables names final Data
======
 [1] "timeimeBodyAccelerometerelerometer-mean()-X"                           
 [2] "timeimeBodyAccelerometerelerometer-mean()-Y"                           
 [3] "timeimeBodyAccelerometerelerometer-mean()-Z"                           
 [4] "timeimeBodyAccelerometerelerometer-std()-X"                            
 [5] "timeimeBodyAccelerometerelerometer-std()-Y"                            
 [6] "timeimeBodyAccelerometerelerometer-std()-Z"                            
 [7] "timeimeGravityAccelerometerelerometer-mean()-X"                        
 [8] "timeimeGravityAccelerometerelerometer-mean()-Y"                        
 [9] "timeimeGravityAccelerometerelerometer-mean()-Z"                        
[10] "timeimeGravityAccelerometerelerometer-std()-X"                         
[11] "timeimeGravityAccelerometerelerometer-std()-Y"                         
[12] "timeimeGravityAccelerometerelerometer-std()-Z"                         
[13] "timeimeBodyAccelerometerelerometerJerk-mean()-X"                       
[14] "timeimeBodyAccelerometerelerometerJerk-mean()-Y"                       
[15] "timeimeBodyAccelerometerelerometerJerk-mean()-Z"                       
[16] "timeimeBodyAccelerometerelerometerJerk-std()-X"                        
[17] "timeimeBodyAccelerometerelerometerJerk-std()-Y"                        
[18] "timeimeBodyAccelerometerelerometerJerk-std()-Z"                        
[19] "timeimeBodyGyroscopescope-mean()-X"                                    
[20] "timeimeBodyGyroscopescope-mean()-Y"                                    
[21] "timeimeBodyGyroscopescope-mean()-Z"                                    
[22] "timeimeBodyGyroscopescope-std()-X"                                     
[23] "timeimeBodyGyroscopescope-std()-Y"                                     
[24] "timeimeBodyGyroscopescope-std()-Z"                                     
[25] "timeimeBodyGyroscopescopeJerk-mean()-X"                                
[26] "timeimeBodyGyroscopescopeJerk-mean()-Y"                                
[27] "timeimeBodyGyroscopescopeJerk-mean()-Z"                                
[28] "timeimeBodyGyroscopescopeJerk-std()-X"                                 
[29] "timeimeBodyGyroscopescopeJerk-std()-Y"                                 
[30] "timeimeBodyGyroscopescopeJerk-std()-Z"                                 
[31] "timeimeBodyAccelerometerelerometerMagnitudenitude-mean()"              
[32] "timeimeBodyAccelerometerelerometerMagnitudenitude-std()"               
[33] "timeimeGravityAccelerometerelerometerMagnitudenitude-mean()"           
[34] "timeimeGravityAccelerometerelerometerMagnitudenitude-std()"            
[35] "timeimeBodyAccelerometerelerometerJerkMagnitudenitude-mean()"          
[36] "timeimeBodyAccelerometerelerometerJerkMagnitudenitude-std()"           
[37] "timeimeBodyGyroscopescopeMagnitudenitude-mean()"                       
[38] "timeimeBodyGyroscopescopeMagnitudenitude-std()"                        
[39] "timeimeBodyGyroscopescopeJerkMagnitudenitude-mean()"                   
[40] "timeimeBodyGyroscopescopeJerkMagnitudenitude-std()"                    
[41] "frequencyrequencyBodyAccelerometerelerometer-mean()-X"                 
[42] "frequencyrequencyBodyAccelerometerelerometer-mean()-Y"                 
[43] "frequencyrequencyBodyAccelerometerelerometer-mean()-Z"                 
[44] "frequencyrequencyBodyAccelerometerelerometer-std()-X"                  
[45] "frequencyrequencyBodyAccelerometerelerometer-std()-Y"                  
[46] "frequencyrequencyBodyAccelerometerelerometer-std()-Z"                  
[47] "frequencyrequencyBodyAccelerometerelerometerJerk-mean()-X"             
[48] "frequencyrequencyBodyAccelerometerelerometerJerk-mean()-Y"             
[49] "frequencyrequencyBodyAccelerometerelerometerJerk-mean()-Z"             
[50] "frequencyrequencyBodyAccelerometerelerometerJerk-std()-X"              
[51] "frequencyrequencyBodyAccelerometerelerometerJerk-std()-Y"              
[52] "frequencyrequencyBodyAccelerometerelerometerJerk-std()-Z"              
[53] "frequencyrequencyBodyGyroscopescope-mean()-X"                          
[54] "frequencyrequencyBodyGyroscopescope-mean()-Y"                          
[55] "frequencyrequencyBodyGyroscopescope-mean()-Z"                          
[56] "frequencyrequencyBodyGyroscopescope-std()-X"                           
[57] "frequencyrequencyBodyGyroscopescope-std()-Y"                           
[58] "frequencyrequencyBodyGyroscopescope-std()-Z"                           
[59] "frequencyrequencyBodyAccelerometerelerometerMagnitudenitude-mean()"    
[60] "frequencyrequencyBodyAccelerometerelerometerMagnitudenitude-std()"     
[61] "frequencyrequencyBodyAccelerometerelerometerJerkMagnitudenitude-mean()"
[62] "frequencyrequencyBodyAccelerometerelerometerJerkMagnitudenitude-std()" 
[63] "frequencyrequencyBodyGyroscopescopeMagnitudenitude-mean()"             
[64] "frequencyrequencyBodyGyroscopescopeMagnitudenitude-std()"              
[65] "frequencyrequencyBodyGyroscopescopeJerkMagnitudenitude-mean()"         
[66] "frequencyrequencyBodyGyroscopescopeJerkMagnitudenitude-std()"          
[67] "subject"                                                               
[68] "activity"                                  






