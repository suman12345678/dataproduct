presentcode
========================================================
author: suman
date: 28/9/17
autosize: true

Description
========================================================

This will predict species from input of length and height.
training data iris
required packages shiny,rsconnect and an account in shinyapps.io
runApp() and then publish
that is rpresent here

github code: https://github.com/suman12345678/developingdataproduct/tree/master/shiny
deploy code: https://suman123456.shinyapps.io/fresh/


Slide With server Code
========================================================


```r
library(rpart)
library(e1071)
library(caret)
library(datasets)
```

```r
data(iris)
head(iris)
```

```
  Sepal.Length Sepal.Width Petal.Length Petal.Width Species
1          5.1         3.5          1.4         0.2  setosa
2          4.9         3.0          1.4         0.2  setosa
3          4.7         3.2          1.3         0.2  setosa
4          4.6         3.1          1.5         0.2  setosa
5          5.0         3.6          1.4         0.2  setosa
6          5.4         3.9          1.7         0.4  setosa
```
 
``{r}  
calculatespecies <- function (sepal.length, petal.length,sepal.width,petal.width) 
{
  c<-train(Species~.,method="rpart",data=iris)
  newdata<-data.frame(Sepal.Length=c(sepal.length),Petal.Length=c(petal.length),Sepal.Width=c(sepal.width),Petal.Width=c(petal.width))
  
  result <- as.vector(predict(c,newdata))
}
```

Slide With Plot
========================================================
User input length and width ofr sepal and petal and the server program will 
predict the species


Thank you
========================================================

