# Simulation 

## Generating Random Numbers
* rnorm: generate radom normal variables with a given mean and std deviation
* dnorm 
* pnorm
* rpois
* d -> density 
* r -> random numbers
* p -> cumulative distribution 
* q -> quantile function

All functions need to specify the mean and std deviation 
Setting the random number seed with set.seed ensures reproducibility (that means, generate the same set of random numbers again)

  1. set.seed
  2. rnorm 

## Simulating a Linear Model

Need a linear model (equation) and the use the functions above

## Random Sampling 

Sample functions draws randomly from a specified set of (scalar) objects allwoing you to sample from arbitrary distributions.

Example: 

set.seed(1)
sample(1:10, 4)
[1] 3 4 5 7

