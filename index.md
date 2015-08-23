---
title       : Coursera Developing Data Products
subtitle    : Course Project
author      : Atlanta Sam
job         : Dog Walker, Data Miner, Jedi Knight
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## People Will Come, Ray.

People will come and play with my App!


For the first part of the project, I developed my first Shiny App using some baseball data.

The App investigates the offensive production (Runs, Hits and Home Runs) of Major League Baseball teams from 1950 to 2014.

Here's a link to that app ---> https://atlantasam.shinyapps.io/baseball

Here's a link to the github repo ---> https://github.com/AtlantaSam/baseball.git 

And, a clip from "Field of Dreams" ... 
https://www.youtube.com/watch?v=QOOLX9R8Ncc


--- .class #id 


## Lahman

I'm a certified Sabermetrician - that's a funny way of saying I'm a Data Scientist that works with baseball data.

If you haven't seen "Moneyball" you might check it out - it's a movie about Sabermetrics.
Here are some scenes: https://www.youtube.com/watch?v=Bj20TKaRgN8

By the way, I got my baseball data by installing the "Lahman" package ... it's basically got all Major League Baseball Data through last season.

--- .class #id 

## Using the Lahman Package

The All-Time Top 10 Teams regarding Runs Per Game (RPG)

```r
library("Lahman"); data(Teams); Teams_sub$RPG <- Teams_sub$R/Teams_sub$G
top10_RPG <- Teams_sub[c("name", "yearID", "RPG")]
top10_RPG <- top10_RPG[order(-top10_RPG$RPG),]; head(top10_RPG, n=10)
```

```
##                        name yearID      RPG
## 866        New York Yankees   1930 6.896104
## 881        New York Yankees   1931 6.883871
## 960        New York Yankees   1936 6.870968
## 1186         Boston Red Sox   1950 6.668831
## 872     St. Louis Cardinals   1930 6.519481
## 896        New York Yankees   1932 6.423077
## 873            Chicago Cubs   1930 6.397436
## 897  Philadelphia Athletics   1932 6.370130
## 1008       New York Yankees   1939 6.361842
## 856            Chicago Cubs   1929 6.294872
```

--- .class #id 

## Summary

1. An App has been presented that investigates the Offensive Production of Baseball Teams since 1950 to 2014.
2. An example has been given concerning the package that I used
3. I hope you found it interesting and (in some regard) useful
