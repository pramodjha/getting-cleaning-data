Getting and Cleaning Data: Course Project
Introduction

This repository contains my work for the course project for the Coursera course "Getting and Cleaning data", part of the Data Science specialization.

Purpose of this project

The purpose of this project is to demonstrate our ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. 

Project Requirement

1) a tidy data set as described below, 
2) a link to a Github repository with your script for performing the analysis, and 
3) a code book that describes the variables, the data, and any transformations or work that we performed to clean up the data called CodeBook.md
4)README.md


About the raw data

The features (561 of them) are unlabeled and can be found in the x_test.txt. 
The activity labels are in the y_test.txt file. 
The test subjects are in the subject_test.txt file.

The same holds for the training set.


About the script and the tidy dataset

I created a script called run_analysis.R which perform following steps to get output
# Setup working directory
# Download the file and store in directory
# Unzip the file
# Get the Data in R : Getting list of unziped file from "UCHI HAR dataset"
# Reading data from files into variable
# Binding row by using rbind 
# set_variable:
# Combine Column by using cbind
# Subset Name of Features by measurements on the mean and standard deviation
# Subset the data frame Data by seleted names of Features
# Read descriptive activity names from activity_labels.txt
# Appropriately labels the data set with descriptive variable names
# In this part,a second, independent tidy data set will be created with the average of each variable for each activity and each subject

so, the code starts from setting up working directory and ending with "tidydata" output

About the Code Book
Above Code step are briefly explained in Code Book
The CodeBook.md file explains the transformations performed and the resulting data and variables.
