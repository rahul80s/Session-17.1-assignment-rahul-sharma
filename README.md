# Session-17.1-assignment-rahul-sharma
Acagild session 17.1 assignment 

1. Use the below given data set

Data Set

2. Perform the below given activities:

a. Create classification model using logistic regression model

b. verify model goodness of fit

c. Report the accuracy measures

d. Report the variable importance

e. Report the unimportant variables

f. Interpret the results

g. Visualize the results


Ans 2 a ->

logitmod <- glm(Class ~ Cl.thickness + Cell.size + Cell.shape, family = "binomial", data=down_train)

summary(logitmod)

Ans 2 b ->

In order to verify the model goodness of fit, we will use the following hypothesis

H0 = The data is consistent with a specified reference distribution.
H1 = The data is NOT consistent with a specified reference distribution

Ans 2 c ->

We will use the following coding for accuracy measures:

accuracy(f, x, test = NULL, d = NULL, D = NULL, ...)

Ans 2 d - >

We will use the following coding for variable importance:

importance(x, type=NULL, class=NULL, scale=TRUE, ...)

Ans 2 f ->


logitmod <- glm(Class ~ Cl.thickness + Cell.size + Cell.shape, family = "binomial", data=down_train)

summary(logitmod)
#> Call:
#> glm(formula = Class ~ Cl.thickness + Cell.size + Cell.shape, 
#>     family = "binomial", data = down_train)
#> 
#> Deviance Residuals: 
#>     Min       1Q   Median       3Q      Max  
#> -2.1136  -0.0781  -0.0116   0.0000   3.9883  

#> Coefficients:
#>                 Estimate Std. Error z value Pr(>|z|)
#> (Intercept)       21.942   3949.431   0.006    0.996
#> Cl.thickness.L    24.279   5428.207   0.004    0.996
#> Cl.thickness.Q    14.068   3609.486   0.004    0.997
#> Cl.thickness.C     5.551   3133.912   0.002    0.999
#> Cl.thickness^4    -2.409   5323.267   0.000    1.000
#> Cl.thickness^5    -4.647   6183.074  -0.001    0.999
#> Cl.thickness^6    -8.684   5221.229  -0.002    0.999
#> Cl.thickness^7    -7.059   3342.140  -0.002    0.998
#> Cl.thickness^8    -2.295   1586.973  -0.001    0.999
#> Cl.thickness^9    -2.356    494.442  -0.005    0.996
#> Cell.size.L       28.330   9300.873   0.003    0.998
#> Cell.size.Q       -9.921   6943.858  -0.001    0.999
#> Cell.size.C       -6.925   6697.755  -0.001    0.999
#> Cell.size^4        6.348  10195.229   0.001    1.000
#> Cell.size^5        5.373  12153.788   0.000    1.000
#> Cell.size^6       -3.636  10824.940   0.000    1.000
#> Cell.size^7        1.531   8825.361   0.000    1.000
#> Cell.size^8        7.101   8508.873   0.001    0.999
#> Cell.size^9       -1.820   8537.029   0.000    1.000
#> Cell.shape.L      10.884   9826.816   0.001    0.999
#> Cell.shape.Q      -4.424   6049.000  -0.001    0.999
#> Cell.shape.C       5.197   6462.608   0.001    0.999
#> Cell.shape^4      12.961  10633.171   0.001    0.999
#> Cell.shape^5       6.114  12095.497   0.001    1.000
#> Cell.shape^6       2.716  11182.902   0.000    1.000
#> Cell.shape^7       3.586   8973.424   0.000    1.000
#> Cell.shape^8      -2.459   6662.174   0.000    1.000
#> Cell.shape^9     -17.783   5811.352  -0.003    0.998

#> (Dispersion parameter for binomial family taken to be 1)

#>     Null deviance: 465.795  on 335  degrees of freedom
#> Residual deviance:  45.952  on 308  degrees of freedom
#> AIC: 101.95

#> Number of Fisher Scoring iterations: 21

Ans 2 g ->

Below are visualizations that can be used: 

Histogram

library(RColorBrewer)
data(abc)
par(mfrow=c(2,3))
hist(abc,breaks=10, col=brewer.pal(3,"Set3")

Bar / Line Chart

plot(abc,type="l")  #Simple Line Plot

barplot(iris$Petal.Length) #Creating simple Bar Graph

Box plot

boxplot(iris$Petal.Length~iris$Species) #Creating Box Plot between two variable

Scatter plot

plot(x=iris$Petal.Length) #Simple Scatter Plot

