# Project Title
Music Stream Data Modeling with PostgresSQL

## Introduction
The database is about building database for a music stream data companies with PostgresSQL

### Purpose of this database
A music stream database which includes function such as storing user inforamtion, song information, artist information, the records of the songs that played by the user and the corresponding time in different format 

### Datasets available
There are five datasets in total. Songs and Artists table are from song_data. Users and Time tables are from log_data. Songplays data is from a combination of song_data and log_data.
1. Songs table: 'song_id', 'title', 'artist_id', 'year', 'duration'
2. Artists table: 'artist_id', 'artist_name', 'artist_location', 'artist_latitude', 'artist_longitude'
3. Time table: 'start_time', 'hour', 'day', 'week', 'month', 'year', 'weekday'
4. Users table: 'userId', 'firstName', 'lastName', 'gender', 'level'
5. Songplays table: 'ts', 'userId', 'level', 'sessionId', 'location', 'userAgent', 'song', 'artist', 'length'

### Prerequisites
### Setup Instructions and Steps followed
1. Run create_tables.py connects to the database server
```
python create_tables.py
```
2. Finish test on etl.ipynb and sql_quesries.py so that etl.py will run correctly
3. Run each step in test.ipynb to see if every table is correctly loaded

## Program execution
1. Run create_tables.py
```
python create_tables.py
```
2. Run etl.py
```
python test.py
```
3. Test results with test.ipynb

## Schema Design
The database is implement by STAR schema with song_play as fact table. Each tables contains:
1. All id numbers are set to PRIMARY KEY
2. Important columns are set to NOT NULL
3. Set up CONFLICT function if duplicate id are set