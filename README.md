# Getting and Cleaning Data Course Project
## Readme from run_analysis.R
- The script carries out the following steps to get the tidy dataset called **Avg_ByActSub**
  1. Load packages plyr and dplyr for further usage.
  2. The following dataframes/vectors are created in sequential order:
     - **activity_labels** (dataframe) holds the activity labels and the activity names.
     - **features** (dataframe) holds the names of the 561 features variables and the corresponding numbers.
     - **features_names** (vector) is the vector representation of **features** dataframe above, which holds the variable names only.
     - **Y_test** (dataframe) contains the activity labels (from 1 to 6) of the testing data.
     - **X_test** (dataframe) contains the testing dataset.
     - **subject_test** (dataframe) contains the subjects/volunteers selected for generating the testing data.
     - **Y_train** (dataframe) contains the activity labels (from 1 to 6) of the training data.
     - **X_train** (dataframe) contains the training dataset.
     - **subject_train** (dataframe) contains the subjects/volunteers selected for generating the training data.
     - **X_test** (dataframe) is the finalised testing dataset by combining the **subject_test**, **Y_test** and **X_test**.
     - **X_train** (dataframe) is the finalised training dataset by combining the *subject_train**, **Y_train** and **X_train**.
     - **Test_And_Train_Data** (dataframe) is created by 2 steps.  Firstly, merge **X_test** and **X_train**.  Secondly, get the activity names by joining **activity_labels**.  The key is actlabels (i.e. the activity labels).
     - **All_Cols** (vector) contains the column names of the Test_And_Train_Data.
     - **Selected_Cols** is the subset of All_Cols.  Only columns which names contains mean (not meanFreq) and std are in this subset.
     - **Test_And_Train_Data_Trim** (dataframe) is a subset of **Test_And_Train_Data** which contains the subject, actlabels, actnames, the std deviation and mean measurements.
  3. The final output is the tidy dataset **Avg_ByActSub**, which contains the average of each measurements in **Test_And_Train_Data_Trim** by subject and actnames.  It is further ordered by subject and actlabels in ascending order.


      
     





