# Disaster Response Web App

## Installation
The codes in this repository was written in Python 3, and requires the following Python packages: json, plotly, pandas, nltk, flask, sklearn, sqlalchemy, sys, numpy, re, etc.

## Project Overview
The project was to create a web app for disaster management to categorize new messages for sending them to their respective authorities.

## File Descriptions
* **process_data.py**: This code takes as its input csv files containing message data. The data undergoes ETL Pipeline and get prepared to run Machine Learning Model. 
* **train_classifier.py**: This code takes the SQLite database produced by process_data.py as an input and uses the data contained within it to train and tune a ML model for categorizing messages. The output is a pickle file containing the fitted model. Test evaluation metrics are also printed as part of the training process.
* **ETL Pipeline Preparation.ipynb**: The code is for ML Pipeline and prediction of messages.
* **ML Pipeline Preparation.ipynb**: ML Pipeline Jupyter notebook was used in train_classifier.py. 
* **data**: This folder contains sample messages and categories datasets in csv format.
* **app**: This folder contains all of the files necessary to run and render the web app.

## Running Instructions
### ***Run process_data.py***
1. Save the data folder in the current working directory and process_data.py in the data folder.
2. From the current working directory, run the following command:
`python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`

### ***Run train_classifier.py***
1. In the current working directory, create a folder called 'models' and save train_classifier.py in this.
2. From the current working directory, run the following command:
`python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

### ***Run the web app***
1. Save the app folder in the current working directory.
2. Run the following command in the app directory:
    `python run.py`
3. Go to http://0.0.0.0:3001/

## Warning
The datasets included in this repository are very unbalanced, with few positive examples for several message categories. 
## Licensing, Authors, Acknowledgements
I want to thank Udacity for encouraging me to do this project.This app was completed as part of the [Udacity Data Scientist Nanodegree](https://www.udacity.com/course/data-scientist-nanodegree--nd025).
