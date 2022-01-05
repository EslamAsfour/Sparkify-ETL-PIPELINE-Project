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
5. elt.py : Python Script containts the whole ETL Process ready to run 
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




State and justify your database schema design and ETL pipeline.
[Optional] Provide example queries and results for song play analysis.