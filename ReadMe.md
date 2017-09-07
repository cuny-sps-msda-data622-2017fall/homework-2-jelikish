## DATA622 HW #2
- Assigned on September 13, 2017
- Due on September 27, 2017 11:59 PM EST
- 15 points possible, worth 15% of your final grade


### Data Pipeline using Python (13 points total)

Build a data pipeline in Python that downloads data using the urls given below, trains a random forest model on the training dataset using sklearn and scores the model on the test dataset.

#### Scoring Rubric
The homework will be scored based on code efficiency (hint: use functions, not stream of consciousness coding), code cleaniless, code reproducibility, and critical thinking (hint: commenting lets me know what you are thinking!)  

#### Instructions:
tl;dr: Submit the following 5 items on github.  
- ReadMe.md (see "Critical Thinking")
- requirements.txt
- pull_data.py
- train_model.py
- score_model.py

More details:

- <b> requirements.txt </b> (1 point)

This file documents all dependencies needed on top of the existing packages in the Docker Dataquest image from HW1.  When called upon using <i> pip install -r requirements.txt </i>, this will install all python packages needed to run the .py files.  (hint: use pip freeze to generate the .txt file)

- <b> pull_data.py </b> (5 points)

When this is called using <i> python pull_data.py </i> in the command line, this will go to the 2 Kaggle urls provided below, authenticate using your own Kaggle sign on, pull the two datasets, and save as .csv files in the current local directory.  The authentication login details (aka secrets) need to be in a hidden folder (hint: use .gitignore).  There must be a data check step to ensure the data has been pulled correctly and clear commenting and documentation for each step inside the .py file.

    Training dataset url: https://www.kaggle.com/c/titanic/download/train.csv
    Scoring dataset url: https://www.kaggle.com/c/titanic/download/test.csv

- <b> train_model.py </b> (5 points)

When this is called using <i> python train_model.py </i> in the command line, this will take in the training dataset csv, perform the necessary data cleaning and imputation, and fit a random forest classifier to the dependent Y.  There must be data check steps and clear commenting for each step inside the .py file.  The output for running this file is the random forest model saved as a .pkl file in the local directory

- <b> eda.ipynb </b> (0 points)

[Optional] This supplements the commenting inside train_model.py.  This is the place to provide scratch work and plots to convince me why you did certain data imputations and manipulations inside the train_model.py file.

- <b> score_model.py </b> (2 points)

When this is called using <i> python score_model.py </i> in the command line, this will ingest the .pkl random forest file and apply the model to the locally saved scoring dataset csv.  There must be data check steps and clear commenting for each step inside the .py file.  The output for running this file is a csv file with the predicted score, as well as a png or text file output that contains the model accuracy report.  


### Critical Thinking (2 points total)

Modify this ReadMe file to answer the following questions directly in place.

1. If I had to join another data source with the training and testing/scoring datasets, what additional data validation steps would I need for the join? (0.5 points)

2. What are some things that could go wrong with our current pipeline that we are not able to address?  For your reference, read [this](https://snowplowanalytics.com/blog/2016/01/07/we-need-to-talk-about-bad-data-architecting-data-pipelines-for-data-quality/) for inspiration. (0.5 points)

3. How would you build things differently if this dataset was 1 trillion rows? (0.5 points)

4. How would you build things differently if the testing/scoring dataset was refreshed on a daily frequency? (0.5 points)
