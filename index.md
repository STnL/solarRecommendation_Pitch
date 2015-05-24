---
title       : Residential Solar Panels
subtitle    : Assessing the profitability of residential solar panels in Eastern Australia
author      : H.Thai
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Background

The push for renewable energy has been an increasing issue in Australia. In particular, solar is considered one of the leading sources of renewable energy given Australia's level of solar intensity.

With the increasingly exponential improvement of solar technology, solar is quickly becoming an opportunity for people to not only use cleaner energy but generate money from solar generation on their roofs. The way this works is that power companies pay people for their solar energy generation. 

However, to profit from this as a residential consumer depends on a number of factors. 

The aim of this data product is to provide a recommendation based on information entered by the user.

--- 

## The Facts

Some key facts about solar generation in Australia:

```r
average_usage_per_person <- 5 
average_person_per_household <- 3.5
average_usage_per_household <- average_usage_per_person * average_person_per_household
avg_solar_gen <- 18
```

---

## The Logic

The logic for the current recommendation engine is rudimentary. It accounts for:
* the state in Eastern Australia that the user resides and automatically assumes that the sun-rich states of QLD and NSW have sufficient sunlight hours in the year to have constant solar generation.
* the average electricity usage per user as reported by Australia's Energy Regulator (AER) which is 5 KWh.
* the living space (in square meters) of the user.
* the average generation of the 90th percentile of solar panels in Australia which is 18 KWh.
* the average usage per household in Eastern Australia which is 18 KWh.

--- 

## Next Steps

Enhance the intelligence of the recommendation engine by:
* Provide a chart of payback period for purchasing solar panels so user has an idea they'll first generate a profit
* Include a home insulation index to factor into the recommendation
* Provide the usage options to include household type which will enable more intelligent recommendation based on the type of household. (EG: parents + young child, parents + teenage child, working couple etc.)  
* Take the geo-location of the user (provided user shares such information) to determine the solar intensity index of the user's location and feed this into the recommendation algorithm.
* Factor into the recommendation the amount of money the user is willing to spend on solar panels to ascertain the likely generation capacity of purchased panels
