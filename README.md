This the first project for Udacity Data Engineer Nanodegree.

The star schema consists of fact tables referring number of dimension tables These tables can help Sparkify solve simplified common business logic. This logic includes:

Using the song and log datasets, you'll need to create a star schema optimized for queries on song play analysis. This includes the following tables.

Fact Table
songplays - records in log data associated with song plays i.e. records with page NextSong
songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent
Dimension Tables
users - users in the app
user_id, first_name, last_name, gender, level
songs - songs in music database
song_id, title, artist_id, year, duration
artists - artists in music database
artist_id, name, location, latitude, longitude
time - timestamps of records in songplays broken down into specific units
start_time, hour, day, week, month, year, weekday

What song should play next for the Sparkify user, based on past behavior.
Which song an user would be interested in listening to at that particular point of time.
Sparkify would use the STAR schema like this:

FACT Table: songplays: attributes referencing to the dimension tables.
DIMENSION Tables: users, songs, artists and time table.

The analytic team is particularly interested in understanding what songs users are listening to, but would like a data engineer to create a Postgres database with tables designed to optimize queries on song play analysis. This is where I come in.

The data we receive is in JSON files, which can take time to analysis. Our goal is to import the data into a Postgres database and use modeling techniques to allow fast retrieval of data. In this case, we will use the STAR schema.

Execute the below files in order each time before pipeline.

create_tables.py $ python3 create_tables.py
etl.ipynb/et.py $ python3 etl.py
test.ipynb
