# esp106-sally_lee
## This is the lab for week 2 
## Add working R code in between the questions
## The chapters refer to the sections in https://rspatial.org/intr/

## Chapter 8  (Functions)

## 1) Write a function 'f' that behaves like this:
## > f('Jim')
## [1] "hello Jim, how are you?"
##HINT: you will need to use the paste() function within your new function
f <- function(name)
  {greeting <- paste("hello", name,", how are you?")
  return(greeting)}
result <- f('Jim')
print(result)

## 2) Write a function 'sumOfSquares' that behaves like this:
sumOfsquares <- function(data){
  result <- sum(data^2)/length(data)
  return(result)
}

d<- c(1,5,2,4,6,2,4,5)
result <- sumOfsquares
print(result)


## > d <- c(1,5,2,4,6,2,4,5)
## > sumOfSquares(d)
## [1] 21.875

# To compute the "sum of squares", subtract the mean value of all numbers from each number. 
# Square these numbers and sum them
# (bonus: make a variant that can handle NAs)
sumOfsquares <- function(data){
  if(any(is.na(data))){
    data <- na.omit(data)
}
  meanvalue <- mean(data)
  result <-sum((data - meanvalue)^2)/length(data)
  return(result)}

d<-c(1,5,2,4,6,2,4,5)
result <-sumOfsquares(d)
print(result)
## Chapter 10  (Flow control)

## 4) Write a for loop that adds the numbers 1 to 10
##HINT: you will need one variable that loops through the numbers 1 to 10 and one that keeps count through each loop
total_sum <- 0
for(i in 1:10){
  total_sum <- total_sum +i
}
print(total_sum)
## 5) Write a for loop that adds the odd numbers between 1 and 10 
odd_sum<-0 
for(i in 1:10){
  if(i %% 2!=0){
    odd_sum <-odd_sum+i
  }
}
print(odd_sum)
