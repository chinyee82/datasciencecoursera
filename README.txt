The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. 

After loading the dataset into the working directory, the run_analysis.R script performs the following steps:

1. The train and test sets are loaded as x/y_train, and x/y_test. The subjects in train/test sets were loaded as train/test_subjects. Files containing descriptors of activities and features measured were loaded as features and act_labels. Column variables were named for the train and test sets. Finally, the training and test datasets are formed by merging the merged_train and merged test using the rbind function. 

2. Values of measurements of mean and std were extracted from the dataset with the grepl function.

3. Activities were relabeled with description labels.

4. A new tidy set was formed by using the aggregate function, grouping by subject Id and respective activity. This new set is saved to a file called tidydataset.text using the write.table function.


