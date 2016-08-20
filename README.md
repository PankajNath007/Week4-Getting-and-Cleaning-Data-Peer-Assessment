# Readme for run_analysis.R

## Purpose
This script processes data from the Human Activity Recognition Using Smartphones Dataset to extract the average means and standard deviations of each variable for a given subject and activity, returning a tidy data frame containing these values.
The script was prepared to meet the requirements of an assignment in the Getting and Cleaning Data Course offered on Coursera

## Source Data
credit for the Human Activity Recognition Using Smartphones Dataset to:
Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto. Smartlab - Non Linear Complex Systems Laboratory DITEN - Universit? degli Studi di Genova. Via Opera Pia 11A, I-16145, Genoa, Italy. activityrecognition@smartlab.ws www.smartlab.ws
Data available here: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
With a full description here:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

## Assumptions
The script assumes the data will be found in the directory "./UCI HAR Dataset/" structured as it is in the linked archive. The script requires that the packages "plyr" and "reshape2" are available.

## Use
To use the script at the prompt, call source("~/run_analysis.R") correcting for file location, then run_analysis(). Assigning the ouput of the script to a data frame is recomended, since the resulting table is too large to simply read on screen.

##Functionality
1.	Download the dataset if it does not already exist in the working directory
2.	Load the activity and feature info
3.	Loads both the training and test datasets, keeping only those columns which reflect a mean or standard deviation
4.	Loads the activity and subject data for each dataset, and merges those columns with the dataset
5.	Merges the two datasets
6.	Converts the activity and subject columns into factors
7.	Creates a tidy dataset that consists of the average (mean) value of each variable for each subject and activity pair.

## The end result is shown in the file tidy.txt.

