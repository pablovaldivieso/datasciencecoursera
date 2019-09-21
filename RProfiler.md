# Profiler 

## Optimizing your code 

Profiler examines how much time is spend in different parts of a program
Useful when trying to optimize your code
Getting biggest impact depends on knowing where the code spends most of the time

## General Principles of Optiization 

Desig first, the optimize 
Measure (collect data), don't guess

## system.time Function 

* system.time Takes an R expression and it tells you the amount of time taken to evaluate the expression
* If there's an error, it will tell you the time to discover the error
* user time (time CPU takes) and elapsed time (the amount of time user experiences)
* this function is useful when you know where the issue is 

## Rprof R profiler function 

* Rprof() starts the profiler in R 
* summaryRprof() summarizes the output from Rprof()
* never use with system.time
* Rprof() keeps track of the function call stack at regularly sampled intervals and tabulates how much time is spend in each function 


### summaryRprof() 
* Two methods of noralizing the data 
* "by.total" divides the time spent in each function by the total run time 
* "by.self" does the same but first substracts out time spent in functions above in the call stack 

