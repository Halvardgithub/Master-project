# Master-project
The main code is contained in three files, Master project - AGMRF.Rmd, Wakefield reproduction for comparison.Rmd and Application for Norwegian death rates.Rmd. The simulation study uses both Master project - AGMRF.Rmd and Wakefield reproduction for comparison.Rmd while the applied case with Norwegian death rates is contained in Norwegian death rates.Rmd, as well as using some code and fucntions from the first two files. A lot of the code is still a bit messy, but it will reproduce the results presented in my report.

## Application for Norwegian death rates.Rmd
This file creates all the plots and figures concerning the applied study in the master project. It can be automated with some nested for loops, but for now you manually choose the observational likelihood, either `poisson` or `nbinomial` and a prior, which is either $Gamma(1, 0.00005), Gamma(1, 0.005)$ or $PC(1, 0.01)$. You must also manually adjust the title to fit the sepcific situation.
