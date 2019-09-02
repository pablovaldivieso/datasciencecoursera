# Functions
  Functions need to define an argument 
## Example 
    columnmean <- function (y) {          - y is the arugument of the function
      nc <- ncol(y)                     - calculates number of columns
      means <- numeric(nc)              - creates a numeric vector equal to the number of columns
      for(i in 1:nc) {
        means[i] <- means(y[,i])        - assign the mean of each column
      }
      means                             - return vector of means
    }
    Always save your file
## Part 1
    Funtions are R objects of class "function"
    Functions are "first class objects"
    Functions can be nested 
   ### Syntax 
      f <- fucntion (<arguments>) {
         % Do something 
      }
   ### Argument Matching 
      Arguments can be matched positionally. The examples below will provide the same outcome 
      
      mydata<- rnorm(100)
      sd(mydata)  sd = standard deviation function
      sd(x = mydata)
      sd(x = mydata, na.rm=FALSE)
      sd(na.rm = FALSE, x = mydata)
      sd(na.rm = FALSA, mydata) 
      
      Functions arguments can be partially matched. The order is as follows:
          1 Check for exact match for a named argument 
          2 check for a partial match
          3 check for a positional match
## Part 2
   ### Defining a function 
    f <- function (a, b=1, c=2, d=NULL){
    }
    b, c, and d have default values 
   ### Lazy Evaluation
    Arguments are only evaluated as they are needed
    
    f <- function(a,b){
      a^2 
    }
    f(2)
    
    [1] 4   This functions never uses the argument b , so calling f(2) will not produce an error because 2 get positionally matched to a
   ### The "..." Argument 
    ... Argument is used to indicate a variable number of arguments that are usually passed on to other functions
    
    Example:
    
    myplot<-function(x,y,type="l",...){
       plot(x,y,type=type,...)                   -> Plot is an existing function
    }
    
    This case personalizes the function "plot" to change the type to "l" but keep the other arguments (...) the same
    
    ... Argument is needed when the number of arguments passed to the function cannot be known in advance
    
    Exampel
    args(paste)     - paste is a function
    function(..., sep =" ", collapse = NULL)
    
    Arguments that come after the "..." must be named explicitely. No partial matching
        
   
