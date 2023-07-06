# SQLite Database Population from JSON

## This Python code establishes a connection to an SQLite database named 'rosterdb.sqlite' and creates three tables: 'User', 'Course', and 'Member'. It then prompts the user to enter a file name or uses a default file name 'roster_data_sample.json'. The code assumes that the file contains JSON data in a specific format.

- The JSON data represents user, course, and their respective roles. Each entry in the JSON data is inserted into the corresponding tables of the SQLite database. If a user or course already exists in the database, it is ignored and not duplicated. The 'Member' table maintains a relationship between users and courses, along with the role assigned to each user in a course.

- The code reads the JSON file, parses the data, and iterates over each entry. It extracts the user's name, course title, and role from each entry and inserts them into the 'User', 'Course', and 'Member' tables, respectively. If a user or course already exists, their corresponding IDs are retrieved. The 'Member' table's primary key ensures that a user cannot be assigned multiple roles in the same course.

- Once all the entries have been processed, the changes are committed to the database.

This code can be used as a starting point for creating and populating an SQLite database with user and course information. By modifying the JSON file or integrating this code into a larger application, you can customize it to suit your specific requirements.
