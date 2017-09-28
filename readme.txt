create ui.R and server.r in a folder
setwd() as that one
library(shiny)
runApp() will run the application in local 


then:
press publish in the local app website with the userid created in shinyapps.io

follow rsconnect deployment after creating account
rsconnect::deployApp('C:/Users/suman/Desktop/datasciencecoursera/developdataproduct/shiny')

The code is deployed at https://suman123456.shinyapps.io/fresh/

for slidify:
library(devtools)
install_github('slidify','ramnathv')
install_github('slidifyLibraries','ramnathv')
library(slidify)
library(slidifyLibraries)
author("suman") this will create index.rmd in the current folder



