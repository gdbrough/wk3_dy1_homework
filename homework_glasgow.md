# SQL Homework

The Glasgow Film Theatre are having a Marvel Movie Marathon! They have asked you to help maintain their database of movies with times and attendees.

## To access the database:

First, create a database called 'marvel'
```
# terminal
createdb marvel
```

Next, run the provided SQL script to populate your database:
```
# terminal
psql -d marvel -f marvel.sql
```

Use the supplied data as the source of data to answer the questions.  Copy the SQL command you have used to get the answer, and paste it below the question, along with the result they gave.

## Questions

1. Return ALL the data in the 'movies' table.
SELECT * FROM movies;

2. Return ONLY the name column from the 'people' table
SELECT name FROM people;

3. Oops! Someone at CodeClan HQ spelled Jean's name wrong! Change it to reflect the proper spelling ('Gene BaMaung' should be 'Jean BaMaung').
UPDATE people SET name = 'Jean BaMaung' where id = 17;

4. Return ONLY your name from the 'people' table.
SELECT name FROM people where id = 1;
SELECT name FROM people where name = 'Graeme Brough';

5. The cinema is showing 'Batman Begins', but Batman is DC, not Marvel! Delete the entry from the 'movies' table.
DELETE FROM movies where id = 9;

6. Create a new entry in the 'people' table with the name of one of the instructors.
INSERT INTO PEOPLE (name) VALUES ('Allan Russell');

7. Jeff Bridges has decided to hijack our movie evening, Remove him from the table of people.
DELETE FROM people WHERE name = 'Jeff Bridges';

8. The cinema has just heard that they will be holding an exclusive midnight showing of 'Avengers: Infinity War'!! Create a new entry in the 'movies' table to reflect this. (The year should be 2018)
INSERT INTO movies (title, year) VALUES ('Avengers: Infinity War', 2018);

9. The cinema would also like to make the Guardian movies a back to back feature. Update the 'Guardians of the Galaxy' show time from 15:30 to 20:00
UPDATE movies SET show_time = '15:30' where id = 11;

## Extension

1. Research how to delete multiple entries from your table in a single command.
DELETE FROM movies WHERE ID < 10;
DELETE FROM movies WHERE year = 2017;
