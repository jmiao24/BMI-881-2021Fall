# HW1

![F1](https://github.com/jmiao24/BMI-881-2021Fall/blob/main/HW1/F1.png)
 

## My design choices.
1. I use the log transformation to make sure the mortality rate are on the same scale.
2. I use different color for different age group to show there are difference of mortality rate in differnt group.
3. I put year in the axis because it is a more continous variable.
4. I use different panel to represents the different income group. I ordered the income group into high -> all -> low and middle to make sure the pattern of the line from left to right is monotone. I added "income group: " in the panel title to make sure people understand what each panel represents.

## How to make a comprehensive graph that includes all of the information in the table

I will plot many figures for rate of every responese variable (such as Incidence).

## Codes
```
require(ggplot2)
require(data.table)

setwd("./Academic/UW-Madison/2021-3-Fall/BMI881/HW/")

df <- fread("./feigin2014_table1_mortality.csv")

df$income_group <- paste0("income group: ", df$income_group)
df$income_group <- factor(df$income_group, levels = c("income group: high", "income group: all", "income group: low_and_middle"))


f1 <- ggplot(data = df, aes(x = year, y = log(mortality_rate), color = age_group)) + 
      geom_line() +
      geom_point() +
      scale_color_manual(values=c('#E89BAC', '#8EBDE3','#6CC1AF')) +
      scale_fill_manual(values=c('#E89BAC', '#8EBDE3','#6CC1AF')) +
      geom_ribbon(aes(ymin = log(interval_low), ymax = log(interval_high), fill = age_group), alpha = 0.2) + 
      facet_wrap(facets = vars(income_group)) +
      theme_bw() +
      ggtitle("log(mortality rate) by income group & year & age group")

print(f1)
```
