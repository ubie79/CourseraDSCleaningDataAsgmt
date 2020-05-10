# CourseraDSCleaningDataAsgmt
## Peer-graded Assignment: Getting and Cleaning Data Course Project

### How the script works?

*Please refer to the code (run_analysis.R) in parallel with this explanation.*

#### Line 9 to 14 (The data retrieval process)

At first calling the *data.table* and *reshape2* packages. This will ensure later when the script is running it will called the package easily. The *data.table* will prepare the data and insert in the table, while *reshape2* illustrate the graph  of the cleaning data. This code will be put inside *packages* object.

Then, *sapply* will be implemented to limit the packages object.

Put the path as working directory and then called the URL specified by the assignment requirement. Then, the file that we put in path are being downloaded and unzipping. From this point, the data are ready to be manipulated (cleaning)/


