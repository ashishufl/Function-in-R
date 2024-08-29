# Function-in-R
All you need to know to starting writing functions in R

##Function in R
Why?
- to understand what the code does 
- for repeated use

Example: 
sum(c(1,2,3))
6

But what does sum function? Algorithm?

###Syntax:

Function_name <- function(inputs) {
output_value <- calculation(inputs)
return(output_value)
}

==> {}. ==group the expression or calculation together

{
a=2
b=3
a+b
}

function_name(2, 3, 4, 5, 6,8)

## store value in an object

Sum_of <- function_name(2, 3, 4, 5, 6,8)


##setting default in the function 

Input/variable = a value 

##when to use named and unnamed arguments

Vol<- function(len, wid, ht) {
Area<- len*wid
volumn <- area*ht

return(volume)
}

==> can b useful to do when we do not remember the oder of input variables

==> or change the default value of an argument or input variable

## Combining multiple functions

- for larger task, we may have to combine multiple functions

- like function in dyplr package

==> est_shrub_mass <- function(volume) {
Mass <- 2.65 *colume^0.9
return(Mass)
}


== one option is creating intermediate variable

$ shrub_vol <- Vol(1, 2, 3)
$shrub_mass <- est_shrub_mass(shrub_vol)


## we can also use pipe 

shrub_mass <- Vol(1,2,3) %>%
est_shrub_mass()


## we can also next function

shrub_mass<- est_shrub_mass(calc_Vol(1,2,3))

#the nexting of functions can be hard to read, may be do not want to next more than one function

##Calling function inside of other function

Est_shrub_mass_dim <- function(len, wid, ht =1) {

 Volume <- calc_Vol(len, wid, ht)
Mass <- est_shrub_mass(Volume)
return(mass)
}


est_shrub_mass_dim(0.8, 1.6, 2)


## RStudio Tips and Tricks when working with Functions

Once we have more functions , it can be difficult to recall them


==(Top Level)
== use side number to see the details steps

==We can highlight the functions vs variable by using global environment

 tools> global options> code> display> highlight R function calls


## How function execute

How we should treat function as black box?

Function should only rely on inputs.
Function should only know inputs and program only knows what comes out of functions and what goes into it. Not knowing what happens inside the function.

 









