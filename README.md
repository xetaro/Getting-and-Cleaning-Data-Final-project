# Getting-and-Cleaning-Data-Final-project
For creating a tidy data set of wearable computing data originally from http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

### Files in this repo:

README.md 
CodeBook.md -- codebook describing variables, the data and transformations
run_analysis.R -- R code
run_analysis.R /explanation

## run_analysis.R
You should create one R script called run_analysis.R that does the following: 
1. Merges the training and the test sets to create one data set. 
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set. 
4. Appropriately labels the data set with descriptive activity names. 
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

It should run in a folder of the Samsung data (the zip had this folder: UCI HAR Dataset) The script assumes it has in it's working directory the following files and folders:

activity_labels.txt
features.txt
test/
train/
The output is created in working directory with the name of tidy2.txt

Note: the R script is built to run without including any libraries for the purpose of this course.

## run_analysis.R/ explanation

1. Set working directory
2. Download the file and put the file in the data folder
3. Unzip the file
4. Unzipped files are in the folderUCI HAR Dataset and get the list of the files
5. Read the Activity, Subject and Fearures files
6. Merges the training and the test sets
7. Extracts only the measurements on the mean and standard deviation for each measurement
8. Create a new data frame by finding the mean for each combination of subject and label. It's done by       
aggregate() function
9. Write the new tidy set into a text file called tidy2.txt


