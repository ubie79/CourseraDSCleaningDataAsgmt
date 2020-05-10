# CourseraDSCleaningDataAsgmt
## Peer-graded Assignment: Getting and Cleaning Data Course Project

### How the script works?

*Please refer to the code (run_analysis.R) in parallel with this explanation.*

#### Line 9 to 14 (The data extraction process)

At first calling the *data.table* and *reshape2* packages. This will ensure later when the script is running it will called the package easily. The *data.table* will prepare the data and insert in the table, while *reshape2* illustrate the graph  of the cleaning data. This code will be put inside *packages* object.

Then, *sapply* will be implemented to limit the packages object.

Put the path as working directory and then called the URL specified by the assignment requirement. Then, the file that we put in path are being downloaded and unzipping. From this point, the data are ready to be manipulated (cleaning),

#### Line 17 to 23 (The data (activities) reading process)

In this part, all needed data will be read and lablled inside respective object. The list are :

Labels         | Activity   | Location
---------------|------------|------------------------------------
activityLabels | fread      | UCI HAR Dataset/activity_labels.txt
features       | fread      | UCI HAR Dataset/features.txt
featuresWanted | grep       | mean, std of features
measurements   | col naming | features

#### Line 26 to 32 (The data (training) reading process)

Similar to previous code section, in this part we will red the training data from Samsung.

Labels          | Activity   | Location
----------------|------------|------------------------------------
train           | fread      | UCI HAR Dataset/train/X_train.txt
train           | combine    | combine data with measurements table
trainActivities | fread      | UCI HAR Dataset/train/Y_train.txt
trainSubjects   | fread      | UCI HAR Dataset/train/subject_train.txt
train           | cbind      | combining trainSubjects, trainActivities & train

#### Line 35 to 41 (The data (testing) reading process)

In this section, testing data will be load and store in local machine.

Labels          | Activity   | Location
----------------|------------|------------------------------------
test            | fread      | UCI HAR Dataset/test/X_test.txt
tesy            | combine    | combine data with measurements table
testActivities  | fread      | UCI HAR Dataset/test/Y_test.txt
testSubjects    | fread      | UCI HAR Dataset/test/subject_test.txt
test            | cbind      | combining testSubjects, testActivities & test
