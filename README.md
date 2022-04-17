# ANA_Assignement_5_R_16
Assignment_5_Barchart and histogram.
---
title: "ANA 515 Assignment_5"
author: Ritesh Tikhade
date: 4/16/2022
output: word_document
---
```{r ,echo=FALSE} 
 Alcohol.data1 <- data.frame(
  country = c("Afghanistan","Albania","Algeria","Andorra","Angola"),
  beer_servings = c(0,89,25,245,217),
  spirit_servings = c(0,132,0,138,57),
  wine_servings =  c(0,54,14,312,45),
  Description = c("Total_Beer&wine&sprit serve in Afganistan=0","Total_Beer&wine&sprit serve in Albania=275","Total_Beer&wine&sprit servein Algeria=39","Total_Beer&wine&sprit serve in Andorra=695","Total_Beer&wine&sprit serve in Angola=319"), 
  stringsAsFactors = FALSE
)
```

# Histogram: Beer served in the 5 countries.
 Beer served in first five countries which include   "Afghanistan","Albania","Algeria","Andorra","Angola". From chart we can see that from range (0 to 50) two country and 50-100 one country and 200-250 2 two country has beer servings.

```{r ,echo=FALSE}
hist(Alcohol.data1$beer_servings, main="Beer served in 5 country", xlab= "Beer_servings", col= "blue")

```


# Barchar of 5 conuntry which serve spirit. From graph we can see that,Afghanistan and Algeria has zero spirit serving and Andorra has highest spirit servings.


```{r ,echo=FALSE}
library(ggplot2)
 ggplot(Alcohol.data1,aes(x = country, y = spirit_servings, fill = country )) +
  geom_bar(stat = "identity") + scale_fill_manual(values= c("Andorra"="cyan")) + geom_text (aes(label = spirit_servings)) 
```
