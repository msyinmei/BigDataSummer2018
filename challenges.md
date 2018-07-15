#R 

1. generate a list (x1) containing 1 through 50

2. randomly select 13 numbers of that list and assign to a second list (x2)

3. use lapply to square the 13 numbers in the second list and assign it to 3rd list

4. create a data.frame with these two lists x1, and x2

5. create a matrix with this data.frame, m1

6. transpose this matrix, m2

7. multiply m1 and m2 and create a m3

8. create a data.frame with m3

9. create a random list of 13 characters from a through z

10. make a word containing anywhere from 3 to 7 characters from these 13 characters

11. make a list of 23 such words

12. subset this list containing only words that have 4 letters

13. subset this list containing only words that have 3 to 6 letters

14. subset this list containing only words with first character 'a'

15. Find all txt files that has url in its name and process them. Commit each line you read into a relational table --with three columns: source, url, about. source is the file path, url is the line you read, about is for later use. 


16. Find the return posted by GSPC each month and for each month find top 10 stocks that performed better than gspc and 10 stocks that performed worse.

```
# one way to calculate monthly returns using quantmod package

require(quantmod)
getSymbols("SPY")


head(SPY)
dim(SPY)
spymx<-as.matrix(SPY)
grep ("2007-01-",rownames(spymx))
spyxm_jan<-spymx[ grep ("2007-01-",rownames(spymx)),]

dim(spyxm_jan)

initial<-spyxm_jan[1,6]
finalv<-spyxm_jan[20,6]
spy_jan_return<-finalv/initial -1
spy_jan_return
```





#SQL
1. how to run linear regression using SQL.
2. Loading and extracting data from dataStores
3. How to load data into mysql
4. preconditions: you have created a relational table with the same column layout as the csv file on disk, you know the csv file has header or no header
```
load data local infile "/home/rkannan/test.csv" into table test09252017 fields terminated by ',' ;
```


```
and here is the test.csv
cat > test.csv
a,v,3,4.0
z,x,2,3.2
r,t,7,6.3
```
5. create new tables from existing tables
```
create table test0925201702 select * from test09252017;
 
insert into test0925201702 select * from test09252017;
```

