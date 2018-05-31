# BigDataSummer2018
Big Data CS-GY 6513 Professor Raman Kannan

## Environment Setup:
### Windows
Run the following two commands to install putty and xming:
`$install putty`
`$install xming`

### Mac:
Download & install xquartz 
https://www.xquartz.org/  
Open and run xquartz (search and open xquartz)
Open your terminal and type in 
ssh -Y <your netid>@12.42.205.8
When prompted for a password:
welcome + letters in your netid + !
Once logged in, change your password with the following command:
$passwd
type in current password 
type in new password
type to confirm new password

## Run MySQL:
Run the following commands: 
`$which mysql`
`$/usr/bin/mysql -u <your netid> -p`
When prompted for a password, your password for mysql is:
<your netid> + 123

#Commands to use your database:
`$use <your netid>`
#Commands to create a table in your database: 
`$create table XYZ (x int, y varchar(32), z varchar(32));`
Challenge: create a relational table to store students and courses, populate with 10 records. Got it. 
create table StudentsInCourses 
SQL Syntax: 
https://www.w3schools.com/sql/sql_syntax.asp

## Run R: 
Type command:
$R
$ls() to list all objects
$lsl<-ls()
$length(lsl)
$history()
tail(history())
rm(list=ls()) clears objects. 

## Run Java: 
java -version


All available tools can be viewed in the following directory: 
/home/tools/
