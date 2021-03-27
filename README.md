# Project-1_Descriptive-statistics
here you find all the commands from the first project
> View(ps_p1)
> install.packages("dplyr")
Installing package into ‘C:/Users/zineb/Documents/R/win-library/4.0’
(as ‘lib’ is unspecified)
essai de l'URL 'https://cran.rstudio.com/bin/windows/contrib/4.0/dplyr_1.0.5.zip'
Content type 'application/zip' length 1331338 bytes (1.3 MB)
downloaded 1.3 MB

package ‘dplyr’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\zineb\AppData\Local\Temp\RtmpoHv0Gr\downloaded_packages
> library(dplyr)

Attachement du package : ‘dplyr’

The following objects are masked from ‘package:stats’:

    filter, lag

The following objects are masked from ‘package:base’:

    intersect, setdiff, setequal, union

> Question4 <-filter(ps_p1, Region == "Europe", ItemType == "Beverages")
> View(Question4)
> Question5 <-Question4[order(Question4$UnitsSold),]
> Question6 <-median(Question4$UnitsSold)
> print(Question6)
[1] 4767

> Household <-filter(ps_p1, ItemType == "Household")
> View(Household)
>  Question7 <-mean(Household$UnitsSold)
> Question8 <- var(Household$UnitsSold)
> Question9 <- sd(Household$UnitsSold)
> install.packages("e1071")
Installing package into ‘C:/Users/zineb/Documents/R/win-library/4.0’
(as ‘lib’ is unspecified)
essai de l'URL 'https://cran.rstudio.com/bin/windows/contrib/4.0/e1071_1.7-6.zip'
Content type 'application/zip' length 1022938 bytes (998 KB)
downloaded 998 KB
package ‘e1071’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\zineb\AppData\Local\Temp\RtmpoHv0Gr\downloaded_packages
> library(e1071)
> Question10 <- moment(Household$UnitPrice, order=3, center=TRUE)
> print(Question10)
[1] 0
> Question11 <-skewness(Household$UnitPrice)
> print(Question11)
[1] NaN
> Question11<-skewness(Household$UnitPrice)
> print(Question11)
[1] NaN
> Question11<-skewness(Household$UnitPrice)
> print(Question11)
[1] NaN
> Question12<-moment(Household$UnitPrice, order=4, center=TRUE)
> Question13<-kurtosis(Household$UnitPrice)
> > print(Question13)
[1] NaN
