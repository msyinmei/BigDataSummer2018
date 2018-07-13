##How to Load Large Files into a Database
https://www.slideshare.net/rk2153/joy-ofunix
(2>&1 in unix combines error and stdout)

Sample Code Instructions
```
tips<-read.csv("https://vincentarelbundock.github.io/Rdatasets/csv/reshape2/tips.csv")
 head(tips)
sp <- ggplot(data=tips, aes(x=total_bill, y=tip)) + geom_point()
sp + facet_grid(sex ~ .)
```

How to update a really large file and import into a database? 
1) Use python or php to take care of batching within the script by committing every 1000 records, provided project is not at risk. 
2) numpy is present but scipy is not there.
https://www.slideshare.net/rk2153/ 