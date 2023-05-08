# NOSQL-Challenge1

# Project Overview
The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating.

The ask is to evaluate some of the rating data in order to help identify where to focus future articles

# There are three parts of the project:

Database and Jupyter Notebook Set Up
Update the Database
Exploratory Analysis

# Part One Database and Jupyter Notebook Set Up

From the terminal import the data provided in the establishments.json file
Copy the text used to import the file and display in a markdown file within the notebook
Import both the PyMongo and Pretty Print libraries and create an instance of Mongo Client (mongo)
Confirm that the database is created and data loaded properly
List the databases in mongoDB. Confirm "uk_food" exists
List the collection(s) in the database, confirm that "establishments" exists
Find and display one document in the establishments collection. Display with pprint
Assign the database and collection to variables


# Part Two Update the Database

Before running any queries we need to make changes to the database per the requests below

Requested Changes
Add a new halal restaurant to the database, which just opened (the code to add has been copied to the jupyter notebook)
Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields
Update the new restaurant with the BusinessTypeID you found associated with #2
Query the database to determine how many documents contain "Dover" as the Local Authority. Remove all documents with Dover Local Authority from the database
Update the datatype from string to decimal for latitude and longitude. Update using the update_many syntax


# Part Three Exploratory Analysis

The last aspect of the project was to conduct analysis on specific questions

Items to note before conducting the analyis

RatingValue refers to the overall rating decided by the Food Authority and ranges from 1-5. The higher the value, the better the rating
This field also includes non-numeric values such as 'Pass', where 'Pass' means that the establishment passed their inspection but isn't given a number rating.
The scores for Hygiene, Structural, and ConfidenceInManagement work in reverse. This means, the higher the value, the worse the establishment is in these areas.
Unless otherwise stated, for each question:
display number of documents using count_documents
Display the first document in the results using pprint
Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows

# Analysis to Conduct

Determine establishments with a hygiene score equal to 20
Determine which establishments in London have a RatingValue greater than or equal to 4
Determine the top 5 establishments with a RatingValue of '5', sorted by hygiene score (lowest to highest) that are closet to the new restaurant. Search within 0.01 degree of the new restaurant added in Part 2
Determine how many establishments in each Local Authority area have a hygiene score of 0. Sort from highest to lowest based on count of documents, and print the top 10 areas.
