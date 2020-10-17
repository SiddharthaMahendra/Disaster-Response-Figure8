# Disaster-Response-Figure8

## Motivation
Having watched people stuck in disasters. I realised swift Disaster Response can minimise the damage and help save lives. For this project I used a dataset from Figure 8 that
contained labeled disaster messages received by an aid organization. So to that end I designed a multi-output Random Forrest classifier that could classify a disaster message into 36 different categories and trained it using supervised learning with (NLP).

For this project the following steps were executed:<br/>
1.An ETL pipeline was created, extracting data from csv files, cleaning and loading into an SQL database.<br/>
2.A machine learning pipeline was created to extract the NLP features and then optimize the algorithm using grid search.<br/>
3.A web app was then developed that extracts the initial data from the database and provides some interactive visual summaries.

## Files

1. app
 -> template<br/>
   -> master.html: Main page of web app<br/>
   -> go.html: Classification result page of web app<br/>
 -> run.py: Flask file that runs app<br/>


The data  files for this project are in the following link: https://drive.google.com/drive/folders/117XSJzD8STe7OKEFd7pOI3TOXLKec-tE?usp=sharing<br/>
2. data<br/>
-> disaster_categories.csv:Data to process <br/>
-> disaster_messages.csv: Data to process<br/>
-> process_data.py<br/>
-> DisasterResponse.db: Database to save clean data to<br/>

The model  files for this project are in the following link: https://drive.google.com/drive/folders/1EIBQ1sTdHbDxoWvv9YGXMx4lK8_19SU-?usp=sharing<br/>
3. models<br/>
-> train_classifier.py<br/>
-> classifier.pkl: Saved model Pickle File<br/>

## Instructions

1. Run the following commands in the project's root directory to set up your database and model.<br/>
    - To run ETL pipeline that cleans data and stores in database<br/>
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`<br/>
    - To run ML pipeline that trains classifier and saves<br/>
         'python train_classifier.py ../data/DisasterResponse.db classifier.pkl'<br/>
2. Run the following command in the app's directory to run your web app.<br/>
    `python run.py`<br/>
3. Go to http://0.0.0.0:3001/

## Acknowledgments

1. https://towardsdatascience.com/natural-language-processing-classification-using-deep-learning-and-word2vec-50cbadd3bd6a<br/>
2. http://pandas.pydata.org/Pandas_Cheat_Sheet.pdf<br/>
3. http://scikit-learn.org/stable/modules/classes.html#module-sklearn.ensemble<br/>
