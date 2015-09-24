weightTAPSPACK
===========

This package is meant to subset The American Panel Survey (TAPS) data by outcome and by covariate variables of interest and provide weights for statistical analysis through the function weightTAPS(). The subsetting and weighting process accounts for respondents attriting from at least one of the waves under analysis, as well as for outcome non-response. Missing values can be dropped from analysis, left as NA, or imputed either with hotdeck imputation or multiple imputation. The output of weightTAPS is an object of class weightTAPSoutput that contains the (imputed) data set(s) and attrition information that can be easily analyzed with calls to getstats() or visualized with the print() method. The function weightTAPS() can be run interactively (default) or supplied with the arguments, setting interact to FALSE.

Example:

myOutcome <- c("APPRCONGS2","APPRCONGS6")
myCovars <- c("POLKNOW3S2","POLKNOW6S2") 
test<-weightTAPS(interact=FALSE,outcome=myOutcome,covars=myCovars,weight=FALSE,refusedasNA=TRUE,method="multi",m=5,pop.base=1,trunc_at=5,stringsAsFactors=TRUE)

Installation:

Ensure the packages survey, plyr, HotDeckImputation, and mice are installed and up-to-date. Then download the tar.gz. Run the following code:

install.packages("file-path/weightTAPSPACK_0.1.tar.gz", repos = NULL, type ="source")

Occasionally it is necessary to restart your R session after installation for a call to library to work.

For more detail, after installation view the help files.
