##Practice with R

MAC Directions:
1) Run xquartz locally to get the xterm 
2) run the IBM server from xterm 
3) run R code from lesson 3 on xterm by typing R to start R. 

```
GGPLOT Visualization using GGPLOT
------------------------------

require(ggplot2)
require(vcd)

ggplot(data=Arthritis, aes(x=Treatment))+geom_bar(aes(fill=Improved))
```

Helpful links for learning R: 
http://rfunction.com/archives/1441 
https://tutorials.iq.harvard.edu/R/Rgraphics/Rgraphics.html
