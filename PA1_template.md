# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data
First we have to read the data.

```r
setwd('D:/ScJavier/Coursera/Data Sciencie Specialization/05_Reproducible_Research/Course_Project_1/RepData_PeerAssessment1/')
if (!file.exists("activity.csv"))
  {
    unzip("activity.zip")
  }
data <- read.csv("activity.csv")
summary(data)
```

```
##      steps                date          interval     
##  Min.   :  0.00   2012-10-01:  288   Min.   :   0.0  
##  1st Qu.:  0.00   2012-10-02:  288   1st Qu.: 588.8  
##  Median :  0.00   2012-10-03:  288   Median :1177.5  
##  Mean   : 37.38   2012-10-04:  288   Mean   :1177.5  
##  3rd Qu.: 12.00   2012-10-05:  288   3rd Qu.:1766.2  
##  Max.   :806.00   2012-10-06:  288   Max.   :2355.0  
##  NA's   :2304     (Other)   :15840
```
To process the data we'll use the `dplyr` package, to manage dates we'll use the `lubridate`, and to make the plot we'll use the `ggplot2` package.

```r
library(dplyr); library(lubridate); library(ggplot2)
```

```
## 
## Attaching package: 'dplyr'
## 
## The following object is masked from 'package:stats':
## 
##     filter
## 
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
```

```r
data<-tbl_df(data)
data<-mutate(data,date=ymd(date))
```

## What is mean total number of steps taken per day?


## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
