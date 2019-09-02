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
