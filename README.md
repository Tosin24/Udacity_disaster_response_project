# Disaster Response Pipeline Project

## Table of Contents
1. Project Overview
2. Installations
3. File Descriptions
4. Author, and Acknowledgement
5. Instructions

## Project Overview
This project is part of the requirement for Udacity Data Scientist Nanodegree Program. The data sets for this project was provided by Udacity in conjunction with FigureEight. In this project, i applied data engineering skills, natural language processing, and machine learning tools to analyze disaster data from FigureEight to build a model for an API that classifies disaster messages.

## Installations
* Machine Learning Packages: Pandas, NumPy, SciPy,  Scikit-Learn.
* Natural Language Process Packages: Punkt, Wordnet, Stopwords.
* SQLite Database Library: SQLAlchemy Engine.
* Web App and Data Visualization: Flask, Plotly.

## File Descriptions
This project contains three folders:
1. Data
    * messages.csv - A csv file that holds the messages data set.
    * categories.csv - A csv file that holds the categories data set.
    * process_data.py - An ETL pipeline that loads the messages and categories datasets, merges the two datasets, cleans the data, and stores it in a SQLite database.
    * DisasterResponse.db - A database that contains the output of the ETL pipeline.


2. Model
    * train_classifier.py - A machine learning pipeline that loads data from the SQLite database, splits the dataset into training and test sets, builds a text processing and machine learning pipeline, trains and tunes a model using GridSearchCV, outputs results on the test set, and exports the final model as a pickle file.
    * mlpipeline.pkl - A pickle file that contains the output of the machine learning pipeline.


3. App
    * template:
      - master.html - The main page of web app.
      - go.html - The classification result page of web app.
    * run.py - A flask file that runs app.

## Author, Acknowledgement
* Oluwatosin (Tosin) Obisan
* All credits to Udacity, and FigureEight for providing the data set for this project.

## Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/mlpipeline.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
