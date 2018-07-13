Steps for (Basic) Project 1.

Perhaps this will be helpful:
https://www.youtube.com/watch?v=U4-RnTW5dfw

TO DO LIST: 
GET DATA: 
1) Create a data-fetch-script -- which will download the data (We need to load 5-10 million rows!?)
2) create a database-schema-creation-script -- which will create the tables if you need them
3) create a data load-script -- which will load the data into the store
4) create a load-verify-validation-script -- which will verify record coutns in the file and the store are same

COMPUTE A NON-GAUSSIAN DISTRIBUTION 
1) create a distribution-function.sql -- this will define the distribution function

2) create compute-sql -- this will select distribution_function you defined above
INTEGRATE R WITH A DATASTORE
1) create an integration-script -- this will do the same select from within R
SUMMARY 
1) create an instruction.txt -- which outlines how to run your scripts...

SUBMISSION
create directory called: P1
Place all files above in this directory
Summary is required 