# financial-aid-outcomes

This project estimates the causal effect of the Tennessee Promise, a no-cost financial aid program, on 
higher education first-time, full-time (FTFT) enrollment at public, two-year institutions from 2010 to 2015 
using data from the IPEDS database in a differences-in-differences (DiD) regression model.

While the regression model provides inconclusive results (statistically insignificant coefficient of interest), 
this project includes discussion on the model's shortcomings and potential alternative models to parse the casual effect,
and other potential routes of analysis.

Files include:

- `data/schools`: (raw data) folder of .csv files including US higher education institution data from 2010-2015
- `data/students`: (raw data) folder of .csv file including US higher education student enrollment data from 2010-2015
- `data/xwalk`: (raw data) folder of .csv file converting zip codes to state abbreviations
- `codebooks`: codebooks for `schools` and `students` folders, providing code rules and variable descriptions
- `clean.csv`: cleaned raw data, including data on schools in TN containing the institution ID, BA-offered indicator,
public institution indicator, FTFT enrollment numbers, FTFT state/local grant amounts, and FTFT federal grant amounts.
- `cleaning.Rmd`: code cleaning the raw data and answering Part A of the data task questions, outputting `clean.csv`
- `analysis.Rmd`: code analyzing `clean.csv` and estimating the DiD model
- `analysis.pdf`: knitted from `analysis.Rmd`; answering Part B of the data task questions; includes code output
and discussion of DiD model effectiveness, validation, areas for improvement, and alternative models
