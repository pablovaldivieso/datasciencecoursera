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
      
      Functions arguments can be partially mathced
        * Check for exact match for a named argument 
        * check for a partial match
        * check for a positional match
        
   
