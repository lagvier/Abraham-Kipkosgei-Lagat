# Basic statistics
Let x be a vector of numeric values. Basic statistics can be easily obatined using the R base functions. Some pf the common basic statistics to summarize numeric data include: mean, standard deviation, variance, minimun and maximum values, mode, median, range, and quantile ranges. 

- Single statistics: Provide a single statistical value specified by the user
```
  mean(x) # Mean
  sd(x) # standard deviation
  min(x) # Minimum value
  max(x)
  length(x) # number of non-missing observations
  range(x)
  quantile(x) #  0%  25%  50%  75% 100%  quartile values of the vector
  sum(x)
  mad(x) # median absolute deviation
```
_Mode_ statistic is not available in the R base and you either define your own function or use third party packages. Example is _modeest_ package
```
require(modeest)
mfv(x)
```
- Combined statistics: Provide a combination of more than one statistical value based on the function specified.
```
fivenum(x) # provide values for min,lower quartile, median,upper quartile,max
summary(x) # mean,median,25th and 75th quartiles,min,max
```
