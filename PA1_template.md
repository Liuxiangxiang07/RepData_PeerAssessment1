---
title: "PeerOne"
author: "liuxiangxiang"
date: "November 16, 2015"
output: html_document
---

##Loading and preprocessing the data

1.load the data

```r
datas<- read.csv(".\\Desktop\\activity.csv")
```

```
## Warning in file(file, "rt"): 无法打开文件'.\Desktop\activity.csv': No such
## file or directory
```

```
## Error in file(file, "rt"): 无法打开链结
```

```r
head(datas)
```

```
##   steps       date interval
## 1    NA 2012-10-01        0
## 2    NA 2012-10-01        5
## 3    NA 2012-10-01       10
## 4    NA 2012-10-01       15
## 5    NA 2012-10-01       20
## 6    NA 2012-10-01       25
```

2.Process the data
It dosn't need be processed.

##What is mean total number of steps taken per day?

1.Histogram figure saved as hist.png

```r
dates<-unique(data$date)
```

```
## Error in data$date: 类别为'closure'的对象不可以取子集
```

```r
hist_data<- data.frame(data=dates, step=0)
```

```
## Error in data.frame(data = dates, step = 0): 找不到对象'dates'
```

```r
for (d in dates){
    hist_data[which(hist_data$date==d),]$steps=sum(subset(data,date==d)$steps,na.rm=T)
}
```

```
## Error in eval(expr, envir, enclos): 找不到对象'dates'
```
