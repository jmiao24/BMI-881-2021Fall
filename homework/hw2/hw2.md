# HW2
 

## 1
Denote $S_n$ as sensitivity, $S_p$ as specificty, $p$ as the prevalence, the precision is 

$Precision = \frac{TP}{TP + FP} = \frac{n p \times S n}{n p \times S n+n(1-p) \times(1-S p)} = \frac{p \times S n}{p \times S n+(1-p) \times(1-S p)} $

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
