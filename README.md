# Student Database Project

This repository contains the files I created for my student database project using SQL and Bash.

## About the Project

The project covers a variety of topics including:

- Creating tables and columns
- Inserting data into tables
- Querying data from tables
- Updating and deleting data
- Using primary and foreign keys
- Joining tables
- Using aggregate functions
- Running SQL scripts from shell scripts

## Shell Scripts Overview

### 1. `insert_data.sh`

This script inserts data from `courses.csv` and `students.csv` into the PostgreSQL database named "students." It performs the following tasks:

- Truncates tables `students`, `majors`, `courses`, and `majors_courses`.
- Reads data from `courses.csv` and `students.csv`.
- Inserts majors into the `majors` table, courses into the `courses` table, and establishes relationships between majors and courses in the `majors_courses` table.

### 2. `student_info.sh`

This script provides information about computer science students from the "students" database. It includes queries for:

- Students with a 4.0 GPA
- Courses whose first letter is before 'D' in the alphabet
- Students whose last name begins with an 'R' and have a GPA greater than 3.8 or less than 2.0
- Students whose last name contains 'sa' in a case-insensitive manner or have an 'r' as the second to last letter
- Students who have not selected a major and either have a first name beginning with 'D' or a GPA greater than 3.0
- The first five courses, in reverse alphabetical order, that have an 'e' as the second letter or end with an 's'
- The average GPA of all students rounded to two decimal places
- Major-wise statistics including Major ID, the total number of students, and average GPA for each major with more than one student
- List of majors in alphabetical order with no students or students whose first name contains a case-insensitive 'ma'
- Unique courses, in reverse alphabetical order, that no student or 'Obie Hilpert' is taking
- Courses, in alphabetical order, with only one student enrolled
