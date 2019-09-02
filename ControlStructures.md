# CONTROL STRUCTURES

* if,else: testing  condition
* for: execute a loop for a fixed # of times 
* while
* repeat
* break 
* next
* return 


## If - else
	if (<condition>) {
		##					
	}else if   -> another type of condition 
		##
	}else      -> always at the end
		##
	}			Note: else is not always neccesary 


## For Loops
	Used for terating over the elements of an object (list, vector, etc)

	for (i in 10){
		print(i)		Takes i variable and in each iteration of the loop gives its values: 1,2,3...10
	}	
	
	x<- matrix(1:6, 2,4)    			 	by 3 matrix 
		for (i in seq_len(nrow(x))){		 	-> seq_len(nrow) = 1:2 -> 2 rows of matrix 
			for (j in seq_len(ncol(x))){		-> seq_len(ncol) = 1:3 -> 3 columns of matrix 
				print(x[i,j])
		}
	} 																					i   j              Matrix 
	This loops as follows: 		1   1	= 1		1	3	5
					1   2	= 3		2	4	6							
					1   3	= 5																2   1	= 2					
					2   2   = 4
					2   3   = 6

## While Loops

	count <-0                   -> while loops test a condition
		while(count<10){
			print(count)
		count<-count+1        -> update value 
	}
	
## Repeat, Next, Break
	Repeat -> initiates an infinte loop, not commmon 
	break -> used to break the inifnity loop

	x0 <- 1			This conde can be used to estimate a value. You can use to solve a set of equations 
	tol <- 1e-8		Also it can be used to optimize a function
	repeat {
		x1<-computeEstimate 				#function 
			if(abs(x1-x0)<tol){
				break
		} else{	
				x0<-x1
		}
	}
	
