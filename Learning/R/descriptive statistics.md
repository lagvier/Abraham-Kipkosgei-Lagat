# Basic statistics
Let x be a vector of numeric values. Basic statistics can be easily obatined using the R base functions. 
- Single statistics:
```
  mean(x) # Mean
  sd(x) # standard deviation
  min(x) # Minimum value
```
_Mode_ statistic is not available in the R base and you either define your own function or use third party packages. Example is _modeest_ package
```
require(modeest)
mfv(x)
```
- Combined statistics:
```
fivenum(x) # Values for Tukey min,lower quartile, median,upper quartile,max

```
