```
  # install.packages('dplyr')
  # install.packages('readxl')
  library(dplyr)
  library(readxl)
  # get data

  dataname = readxl::read_excel('C:/Users/my documents/Dropbox/data.xls', sheet = 'helb')
  # names(dataname)
  # select the columns 
  dataname = subset(dataname, select = c("SerialNo","ID","Name","No"))

  # dataname = as.data.frame(cbind(
  #   house = c(1:5),
  #   p1 = c(200, 105, NA, 80, NA),
  #   p2 = c(230, NA, 90, 200, NA),
  #   p3 = c(NA, 70, NA, 300, NA),
  #   p4 = c(120, 380, NA, 180, 190),
  #   p5 = c(60, NA, 140, NA, NA)
  # )) %>%
  # #   subset(., select = c())

  d = melt(data = dataname, id = 'house') %>%
    aggregate(value ~ house, data= ., function(x) sum(x, na.rm = TRUE)) %>%
    plyr::rename(data= ., c(value = ' TOTAL Production'))
 ```
