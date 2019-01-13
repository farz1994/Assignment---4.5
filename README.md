library(RcmdrPlugin.IPSUR)
data(RcmdrTestDrive)
Perform the below operations:
1. Compute the measures of central tendency for salary and reduction which variable has highest center?
There are three main measures of central tendency: the mode, the median and the mean. Each of these measures describes a different indication of the typical or central value in the distribution.

x <- RcmdrTestDrive$salary

table(is.na(x))

mean(x)
median(x)

getmode <- function(v) {
  uniqv <- unique(v)
  uniqv[which.max(tabulate(match(v, uniqv)))]
}

mode <- getmode(x)

x <- RcmdrTestDrive$reduction

table(is.na(x))

mean(x)
median(x)

getmode <- function(v) {
  uniqv <- unique(v)
  uniqv[which.max(tabulate(match(v, uniqv)))]
}

mode <- getmode(x)

# taking salary as variable
> mean(x)
[1] 724.5164
> median(x)
[1] 710.15
> mode
[1] 618.65

# taking reduction as variable

> mean(x)
[1] 223.631
> median(x)
[1] 139.5
> mode
[1] 116

>>>> Salary has the highest center


2. Which measure of center is more appropriate for before and after?
# question not clear enough to answer.
Ans : Mean is the most appropriate method for both the variables
