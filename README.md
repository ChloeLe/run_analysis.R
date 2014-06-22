run_analysis.R
==============

Getting and Cleaning Data Course Project

This Repo contains :

run_analysis.R - The R code for the programming assignment
Codebook.md - description of the data, transformation & variables
README.md - description of how the code works

The code follows the assignment in a step by step format

Prior to any steps we begin by setting our working directory

Step 1:

Read all the test and training files: y_test.txt, subject_test.txt and X_test.txt.
We then combine the files to a data frame in the form of subjects, labels etc.
The featuresis read from features.txt and filter it to only leave features that are either means ("mean()") or standard deviations ("std()").

Step 2:

The reason for leaving out meanFreq() is that the goal for this step is to only include means and standard deviations of measurements, of which meanFreq() is neither.
A new data frame is then created that includes subjects, labels and the described features.

Step 3:

Read the activity labels from activity_labels.txt and replace the numbers with the text.

Step 4:

Make a column list (includig "subjects" and "label" at the start)
Tidy the list by removing all non-alphanumeric characters and converting the result to lowercase
Apply the now-good-columnnames to the data frame
Step 5:

Create a new data frame by finding the mean for each combination of subject and label. It's done by aggregate() function
Final step:

Write the new tidy set into a text file called tidy.txt, formatted similarly to the original files.
