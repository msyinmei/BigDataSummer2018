# BigDataSummer2018
Big Data CS-GY 6513 Professor Raman Kannan
A big thank you to [IBM Academic Initiatives](https://developer.ibm.com/academic/) for sponsoring all computers, software and cloud computing infrastructure utilized in this course.


## Environment Setup:
### Windows
Run the following two commands to install putty and xming:
```sh
install putty
```

```sh
install xming
```
your login: your netid
your password: welcome<letters in your netid>!
Set up to use ssh with <your netid>@12.42.205.8

### Mac:
Download & install xquartz 
https://www.xquartz.org/  
Open and run xquartz (search and open xquartz)
Open your terminal and type in 
```sh
ssh -Y <your netid>@12.42.205.8
```
When prompted for a password:
```sh
welcome<letters in your netid>!
```
Once logged in, change your password with the following command:
```sh
passwd
```
type in current password 
type in new password
type to confirm new password

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

#Commands to use your database:
```sh 
use <your netid>
```
#Commands to create a table in your database: 
```sh
create table XYZ (x int, y varchar(32), z varchar(32));
```
Challenge: create a relational table to store students and courses, populate with 10 records.
SQL Syntax: 
https://www.w3schools.com/sql/sql_syntax.asp

## Run R: 
Type command:
```sh 
R
```
```sh
ls()
```
```sh
lsl<-ls()
```
```sh
length(lsl)
```
```sh
history()
```
```sh
tail(history())
```
```sh
rm(list=ls())
```

## Run Java: 
```sh
java -version
```


All available tools can be viewed in the following directory: 
```sh
cd /home/tools/
```
```sh
ls
```


--- 
## Other Notes
What is Big Data? 
https://en.wikipedia.org/wiki/Big_data

# Structured vs. Unstructured Databases
## Structured: 
has a schema. 
R & MySQL: Persistent Store. Fixed Columns. Structured Databases 

## Unstructured:
No schema. Aka Schemaless. 
MongoDB: Structured Databases are not useful for storing, so they came up with MongoDB to deal with data varied in structure.
