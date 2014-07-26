CodeBook for the tidy dataset
=============================

## Data source
- http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 
- https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

## The data

The dataset includes the following files:

- 'README.txt'
- 'features_info.txt': Shows information about the variables used on the feature vector.
- 'features.txt': Lists features.
- 'activity_labels.txt': Links the class labels with their activity name.
- 'train/X_train.txt': Training set.
- 'train/y_train.txt': Training labels.
- 'test/X_test.txt': Test set.
- 'test/y_test.txt': Test labels.

## Steps
- Merges the training and the test sets to create one data set.
- Extracts only the measurements on the mean and standard deviation for each measurement. 
- Uses descriptive activity names to name the activities in the data set
- Appropriately labels the data set with descriptive variable names. 
- Creates a second, independent tidy data set with the average of each variable for each activity and each subject. 

## Variables
- X: contains combined x_train.txt and x_test.txt
- Y: contains combined y_train.txt and y_test.txt
- S: contains combined subject_train.txt and subject_test.txt
- combined: column bind for X, Y, S
- tidy : aggregate by activity and subject with averages

The result is saved as tidy_data.txt, a 180x69 data frame.  The three columns contains keys: activity id, activity_name, subject.  Remaining columns show the averages for each of the 66 attributes.