# Scoping Rules 
## Symbol Binding  
    A function name can be repeated and R may get confused 
    Need to seacrh which packages are insatlled in R
    search()
    Gobal environment is always the first element of the search list and the base package is always the last 
## Lexical Scoping
    What is an environment?
    Is a collection of (symbol, value) pairs, i.e. x is a symbol and 3.14 might be its value
    Every environment has a parent environment 
    A function + an environemnt = a closure or function closure
    
    A free variale - > a symbol that hasn't been definied in an environment 
    If the value of a symbol is not foun in the environment in which a function was defined, then the search is continued in the parent environment
## R Scoping Rules
    In R, you can have functions inside other functions
    Languages like C don't allow this
    
