# Multilevel Analyses
Entrepreneurship and regional development – OLS and Multilevel Analysis of Sweden 

## Table of Contents
- [OPENING AND SAVING FILES](#opening-and-saving-files)
- [DATA MANIPULATION](#data-manipulation)
- [REGRESSION MODELS](#regression-models)
- [PPOOLED OLS](#pooled-oLS)
- [YEAR/WAVE-SPECIFIC OLS](#year/wave-specific-oLS)
- [MULTILEVEL MODELING](#multilevel-modeling)
- [EXAMPLES OF ADDITIONAL COMMANDS](#examples-of-additional-commands)
- [TESTS FOR RESIDUALS AND MULTICOLLINEARITY](#tests-for-residuals-and-multicollinearity)


# OPENING AND SAVING FILES
// Open a data file
use "S:\Kingsley Osunkwo Files\Linear regression_And_Multilevel_models-DataExerciseV1.dta", clear

// Save the dataset
save "S:\Kingsley Osunkwo Files\Linear regression_And_Multilevel_models-DataExerciseV1.dta", replace

# DATA MANIPULATION
Calculating Household Income at the Individual Level
Refer to the OECD Note on Equivalence Scales for guidance.

Removing Missing Data

drop if ep005_ < 0

# Install Tidyverse package
<install.packages("tidyverse")

# Load Tidyverse package and all Required Libraries
<library(tidyverse)

# The Tidyverse package encompasses neumerous packages, for the sake of this particular line, we need `ggplot2` and `gridExtra`,
 if you load the `tidyverse` package in R, it will automatically load ggplot2 and other related packages, making them available for use,
but it would not automatically load `gridExtra`, so I have to load it.
library(gridExtra)

# Install and load the plotly package
<install.packages("plotly")
library(plotly)
layout_options(theme = "plotly_white")
