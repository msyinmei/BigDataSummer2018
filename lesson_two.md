##SQL Challenge

## Run MySQL:
Run the following commands:  
```sh
which mysql
```
```sh
/usr/bin/mysql -u <your netid> -p
```
When prompted for a password, your password for mysql is:  
<your netid> + 123  

#Command to show your databases: 
```sh
SHOW DATABASES;
```

Example:

```sh
MariaDB [(none)]> SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| test               |
| ym####             |
+--------------------+
3 rows in set (0.00 sec)    
```

#Commands to use your database:  
```sh 
use <your netid>
```

#Commands to create a table in your database:   
```sh
CREATE TABLE XYZ(x int, y varchar(32), z varchar(32));
```

To rename a table: 
```sh
ALTER TABLE <table name> RENAME TO <new table name>;
```

Challenge: create a relational table to store students and courses, populate with 10 records.  
SQL Syntax: https://www.w3schools.com/sql/sql_syntax.asp

```sh
CREATE TABLE XYZ(student_id int, first_name varchar(32), last_name varchar(32), course_id int);

ALTER TABLE XYZ RENAME TO student_enrollment

INSERT INTO student_enrollment(student_id, first_name, last_name, course_id) VALUES (1, 'Alice', 'One', 3);
INSERT INTO student_enrollment(student_id, first_name, last_name, course_id) VALUES (2, 'Bob', 'Two', 2);
INSERT INTO student_enrollment(student_id, first_name, last_name, course_id) VALUES (3, 'Eve', 'Three', 1);
INSERT INTO student_enrollment(student_id, first_name, last_name, course_id) VALUES (4, 'Mal', 'Four', 3);
INSERT INTO student_enrollment(student_id, first_name, last_name, course_id) VALUES (5, 'Bill', 'Five', 2);
INSERT INTO student_enrollment(student_id, first_name, last_name, course_id) VALUES (6, 'Evelyn', 'Six', 1);
INSERT INTO student_enrollment(student_id, first_name, last_name, course_id) VALUES (7, 'Batman', 'Seven', 3);
INSERT INTO student_enrollment(student_id, first_name, last_name, course_id) VALUES (8, 'Superman', 'Eight', 2);
INSERT INTO student_enrollment(student_id, first_name, last_name, course_id) VALUES (9, 'Brute', 'Nine', 1);
INSERT INTO student_enrollment(student_id, first_name, last_name, course_id) VALUES (10, 'Force', 'Ten', 3);
```

#Display table

```sh
SELECT * FROM student_enrollment; 
```
example: 
```sh
MariaDB [ym1524]> SELECT * FROM student_enrollment
    -> ;
+------------+------------+-----------+-----------+
| student_id | first_name | last_name | course_id |
+------------+------------+-----------+-----------+
|          1 | Alice      | One       |         3 |
|          2 | Bob        | Two       |         2 |
|          3 | Eve        | Three     |         1 |
|          4 | Mal        | Four      |         3 |
|          5 | Bill       | Five      |         2 |
|          6 | Evelyn     | Six       |         1 |
|          7 | Batman     | Seven     |         3 |
|          8 | Superman   | Eight     |         2 |
|          9 | Brute      | Nine      |         1 |
|         10 | Force      | Ten       |         3 |
+------------+------------+-----------+-----------+
10 rows in set (0.00 sec)
```