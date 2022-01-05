# Sparkify ETL PIPELINE Project "Udacity Nano Degree"
## 1) Database Purpose
Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to.
The current dataset is a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

## 2) Files in the repository
### In the Repo you will find the following : 
1. Data : A directory that contains the JSON files for the Logs/Metadata
2. sql_queries.py : Python script containts Create/Insert/Select Queries format for each table we will create
3. create_tables.py : Python script to Drop all created tables and recreate them with the sql_queries formats
4. etl.ipynb : Jupyter notebook to test the ETL pipeline schema and process
5. etl.py : Python Script containts the whole ETL Process ready to run 
6. test.ipynb : Jupyter notebook to test the content of each table 
    
## 3) How to run the Python scripts
1. Run create_tables.py with the CMD command:
``` 
     python create_tables.py 
```
2. Run etl.py with the CMD command:
```
    python etl.py    
```
3. Check Table content and do you analysis on test.ipynb 


## 4) Database Schema Design 
In this Database we are using **Star Schema** 
### Fact Table : 
1. **songplays** : records in log data associated with song plays i.e. records with page NextSong
Attributes :
+ songplay_id
+ start_time
+  user_id
+  level
+  song_id 
+  artist_id 
+  session_id 
+  location 
+  user_agent
### Dimension Tables
1. **users** - users in the app
Attributes : 
+ user_id 
+ first_name 
+ last_name 
+ gender 
+ level
2. **songs** - songs in music database
Attributes : 
+ song_id 
+ title 
+ artist_id 
+ year 
+ duration
3. **artists** - artists in music database
Attributes : 
+ artist_id 
+ name 
+ location 
+ latitude 
+ longitude
4. **time** - timestamps of records in songplays broken down into specific units
Attributes : 
+ start_time 
+ hour 
+ day 
+ week 
+ month 
+ year 
+ weekday

## 5) ETL pipeline
1. Create Database tables
2. Load JSON Files and Create Pandas Dataframe to store the Data
3. Extract the needed Data from pandas dataframe 
4. Transform the needed columns to the target form (Ex : Transform ts column to datetime Type)
5. Load\Insert data into the target tables
