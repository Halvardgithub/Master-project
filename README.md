# Master-project
The main code is contained in three files, Master project - AGMRF.Rmd, Wakefield reproduction for comparison.Rmd and Application for Norwegian death rates.Rmd. The simulation study uses both Master project - AGMRF.Rmd and Wakefield reproduction for comparison.Rmd while the applied case with Norwegian death rates is contained in Norwegian death rates.Rmd, as well as using some code and fucntions from the first two files. A lot of the code is still a bit messy, but it will reproduce the results presented in my report.

## Master project - AGMRF.Rmd
Firstly, this file looks at first and second order random walks in time and implements them and make figures. Secondly, there are multiple regeneric definitions both for a RW1 and an adaptive RW1. They also both have definitions where the precision matrix $Q$ is defined inside the rgenric or supplied as an argument. Then follows data generation for all the mean trends and some testing and examples with INLA and the different latent models

## Wakefield reprodction for comparison.Rmd
The first half of the file concerns the reproduction of the results in the Wakefield article. Currently, it assumes that the data generation from the file above have been run and is in the global memory, but they can also be saved and loaded. Then the model fitting, evaluation and plotting is done. The `prior_str` is defined at the top, and is either set to `PC`, `Gamma0,00005` or `Gamma0,005` for the respective priors. The second half of the file is similar code for the harmonious mean structures, it uses the function `mod_eval_W` from above, and make sure the file location at the bottom of the function is correct, I had two different folders for the results. The rest is slightly modified to fit this example, and very similar to the above code. Note, that we again assign the `prior_str` for each prior.

## Application for Norwegian death rates.Rmd
This file creates all the plots and figures concerning the applied study in the master project. It can be automated with some nested for loops, but for now you manually choose the observational likelihood, either `poisson` or `nbinomial` and a prior, which is either $Gamma(1, 0.00005), Gamma(1, 0.005)$ or $PC(1, 0.01)$. You must also manually adjust the title to fit the sepcific situation.


