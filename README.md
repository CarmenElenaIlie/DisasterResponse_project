# DisasterResponse_project


Repository for the course project Disaster Respose as part of the Nanodegree Data Science from Udacity.

https://github.com/CarmenElenaIlie/DisasterResponse_project

The motivation behind this machine learning project is to build a web application that classifies text messages received in the event of a disaster such as during storms or earthquakes. The web application can be used by emergency workers to classify messages, and this could be essential for effective allocation of resources. The output of the ML model is a classification of the message into several categories such as water, shelter, food and clothing. Such a classification would give the app user a better awareness on what kind of help/aid is needed in case of emergency.

**File Description**

        disaster_response_pipeline
          |-- app
                |-- templates
                        |-- go.html
                        |-- master.html
                |-- run.py
          |-- data
                |-- disaster_message.csv
                |-- disaster_categories.csv
                |-- DisasterResponse.db
                |-- process_data.py
          |-- models
                |-- classifier.pkl
                |-- train_classifier.py
          |-- Screenshots
                |-- img1.jpg
                |-- img2.jpg
          |-- README

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


