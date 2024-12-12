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
```
// Open a data file
use "S:\Kingsley Osunkwo Files\Linear regression_And_Multilevel_models-DataExerciseV1.dta", clear

// Save the dataset
save "S:\Kingsley Osunkwo Files\Linear regression_And_Multilevel_models-DataExerciseV1.dta", replace
```

# DATA MANIPULATION
Calculating Household Income at the Individual Level
Refer to the OECD Note on Equivalence Scales for guidance.

Removing Missing Data
```
drop if ep005_ < 0
```

Keeping Specific Countries
```
keep if country == 20 | country == 11
```

Generating New Variables
```
gen self_perceived_health = sphus
replace self_perceived_health = . if sphus < 0

gen phy_health = self_perceived_health
replace phy_health = 1 if self_perceived_health == 5
replace phy_health = 5 if self_perceived_health == 1
```


