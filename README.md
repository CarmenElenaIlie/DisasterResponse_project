# DisasterResponse_project


Repository for the course project Disaster Respose as part of the Nanodegree Data Science from Udacity.

Project Components

This repository has 3 components:

1. ETL Pipeline (process_data.py)
   
  Loads the messages and categories datasets
  Merges the two datasets
  Cleans the data
  Stores it in a SQLite database
  
2. ML Pipeline (train_classifier.py)
   
  Loads data from the SQLite database
  Splits the dataset into training and test sets
  Builds a text processing and machine learning pipeline
  Trains and tunes a model using GridSearchCV
  Outputs results on the test set
  Exports the final model as a pickle file
  
3. Flask Web App (app folder)
   
  Provides basic descriptives of the training data
  Has a form to classifify new messages using the best ML model

**Usage:**

In the project's root directory:

  To run ETL pipeline that cleans data and stores in database:
python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db

  To run ML pipeline that trains classifier and saves:
python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl

  To run the web app locally:
python app/run.py then go to http://0.0.0.0:3001/ or localhost:3001

Alternatevely, in unix system type: gunicorn app.run:app -b 0.0.0.0:3001 to run a local gunicorn server

**Output:**

![image](https://github.com/CarmenElenaIlie/DisasterResponse_project/assets/144029233/47370b66-cc48-45e9-8ba4-9a7a26b9fa17)


![image](https://github.com/CarmenElenaIlie/DisasterResponse_project/assets/144029233/0f9b56b7-8f79-484e-aeaf-1027959314df)


