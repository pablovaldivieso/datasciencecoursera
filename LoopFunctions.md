# Loop Functions 

* lapply: loop over a list and evaluate a function on each element 
* sapply: same as lapply but simplifies the result 
* apply: apply a function over the margins of an array 
* tapply: apply a function over subsets of a vector (table apply)
* mapply: multivariate version of lapply 
* split: use with lapply


## lapply 
  Takes 3 arguments:
  1) list
  2) a function
  3) other argument
  
  ### Example
    x <- list(a = 1:5, b = rnorm(10))
    lapply(x, mean) #apply the mean to all the elements in x 
    $a
    [1] 3
    $b 
    [1] 0.0296
    
    Outcome will always be a list 

Anonymous functions can be used 

## sapply 
  Simplify the result of lapply 
  
  * List where every element is lenght 1 -> a vector is returned 
  * List where every element is a vector greater than length -> matrix is returned 
  * if can't figure it out -> a list is returned
  
## apply 
  Evaluate a function (often an anonymous one) over the margins of an array
  
  ### Syntax 
    str(apply) 
    function (X, MARGIN, FUN, ...)
    - X is an array
    - MARGIN is an integer indicating which margins should be "retained"
    - FUN is a function to be applied 
    - ... is for other arguments to be passed to FUN
  
  ### Example 
    x <- matrix(rnorm(200), 20, 10)  #20 rows, 10 columns
    apply(x,2,mean)  #caclulate the mean of all the columns (that's why the # 2)
    apply(x,1,sum)   #calculate the sum of all the row (#1)
    

## mapply 
Is a multivariable apply of sort which applies a function in parallel over a set of arguments

  ### Sytanx 
  str(mapply)
  function (FUN, ..., MoreArgs = NULL, SIMPLIFY = TRUE, USE.NAMES = TRUE)
  - FUN is a function to apply 
  - ... contains arguments to apply over 
  - MoreArgs is a list of other arguments to FUN 
  - SIMPLIFY indicates whether the result should be simplified
  
Useful when you have more than one list. For instance, you only want to apply a function to 1 list and the appy something else to the second list 

The arguments needs to be equal to the number of lists

  ### Example 
    instead of doing: list(rep(1:4), rep(2,3), rep(3,2), rep(4,1))
    
    you can do:
    
    mapply(rep, 1:4, 4:1)

Vectorize function that doesn't allow for vector arguments.

## tapply
  
  
