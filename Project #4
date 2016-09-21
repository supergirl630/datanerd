# import the csv file
worldbank <- read.csv(file.choose())
worldbank
head(worldbank)
str(worldbank)

# filtering the data from the csv file

data1960 <- worldbank[worldbank$Year == "1960", ]
head(data1960)

data2013 <- worldbank[worldbank$Year == "2013", ]
head(data2013)

# check row count

nrows(data1960) # 187 rows
nrows(data2013) # 187 rows

# creating the 1960 and 2013 dataframes

worldbank1960 <- data.frame(data1960, Life.Expectancy = Life_Expectancy_At_Birth_1960)
head(worldbank1960)

worldbank1960$Year <- NULL

worldbank2013 <- data.frame(data2013, Life.Expectancy = Life_Expectancy_At_Birth_2013)
head(worldbank2013)

worldbank2013 <- NULL


#visualizing the 1960 data

library(ggplot2)

qplot(data=worldbank1960, x= Fertility.Rate, y= Life.Expectancy,
      color=Region, size= I(4), alpha=I(0.6),
      main= "Life Expectancy vs Fertility Rate (1960)")

# High life expectany correlates with low fertility rates, stronger in europe (1960)
# Lower life expectany correlated with high fertility rates (1960)
# Questions did the study include both men and women?
# Poor health facilities and access to healthcare could be bringing
# life expectany numbers down
# In the Middle East the correlation is less strong, ie individuals
# could have higher fertility rates and higher life expectancy

qplot(data=worldbank2013, x= Fertility.Rate, y= Life.Expectancy,
      color=Region, size= I(4), alpha=I(0.6),
      main= "Life Expectancy vs Fertility Rate (2013)")

# In Asia and the Americas people have fewer children regarless of life expectancy (2013)
# In Europe there is a very tight correlation between high life expectancy
# People in the middle east now have fewer children than they did in 1960
# In Africa life expectancy is still lower than that of other regions but, fertility rates
# are on the decline
# and low birth rates

