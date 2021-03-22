This the first project for Udacity Data Engineer Nanodegree.

The star schema consists of fact tables referring number of dimension tables These tables can help Sparkify solve simplified common business logic. This logic includes:

What song should play next for the Sparkify user, based on past behavior.
Which song an user would be interested in listening to at that particular point of time.
Sparkify would use the STAR schema like this:

FACT Table: songplays: attributes referencing to the dimension tables.
DIMENSION Tables: users, songs, artists and time table.