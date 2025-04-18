# african-american-firsts
Data on African American achievements; from tidyverse #TidyTuesday exploration by A. Jayaraman.

```{r, include=F}
library(tidyverse)
library(ggplot2)
library(magrittr) # needs to be run every time you start R and want to use %>%
library(dplyr)    # alternatively, this also loads %>%
install.packages("dplyr")    # alternative installation of the %>%
install.packages("magrittr") # package installations are only needed the first time you use it
install.packages("tidytuesdayR")

choose_how <- 1  # Set this to either 0 or 1

if(choose_how == 0){
  # Either read with Github csv urls ------------------------------------------
  firsts_url <- "https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2020/2020-06-09/firsts.csv"
  science_url <- "https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2020/2020-06-09/science.csv"
  
  firsts <- readr::read_csv(firsts_url)
  science <- readr::read_csv(science_url)
} else {
  # Or read in with tidytuesdayR package --------------------------------------
  # (https://github.com/thebioengineer/tidytuesdayR)
  
  choose_again <- 1  # Set this to either 0 or 1
  
  if(choose_again == 0){
    tuesdata <- tidytuesdayR::tt_load('2020-06-09')
  } else {
    tuesdata <- tidytuesdayR::tt_load(2020, week = 24)
  }
  
  firsts <- tuesdata$firsts
  science <- tuesdata$science
}
```

```{r, echo=F}
firsts
```


```{r, echo=F}
science
```

