# Epigenomic sequencing data exploration with InterSeq suite #

## Introduction ##

-Calculations from a bam file with SeqData

-Interface tables to flowCore with SeqFrame

-Graphical interface for visualization and gating with SeqViz


## Details ##

Packages are shared on Github.

https://github.com/sheng-liu/SeqData.git

https://github.com/sheng-liu/SeqFrame.git

https://github.com/sheng-liu/SeqViz.git

## Installation ##

SeqViz suite is dependent on a few packages listed below:

SeqData is dependent on
"IRanges","GenomicRanges","Rsamtools","rtracklayer","GenomicAlignments","dplyr"

SeqFrame is dependent on
"Biobase","flowCore","flowStats"

SeqViz is dependent on
GTK+, "RGtk2"

you need to make sure these packages are installed before installing SeqViz Suit, a simple way to do so is to type these code in R console.

```
## install SeqData
## dependencies
source("http://bioconductor.org/biocLite.R")
biocLite(c("IRanges","GenomicRanges","Rsamtools","rtracklayer","GenomicAlignments","dplyr"))

## install SeqData from Github
install.packages("devtools")
library(devtools)
install_github("sheng-liu/SeqData",build_vignettes=FALSE)
```

```
## install SeqFrame
## dependencies
source("http://bioconductor.org/biocLite.R")
biocLite(c("Biobase","flowCore","flowStats"))

## install SeqFrame from Github
library(devtools)
install_github("sheng-liu/SeqFrame",build_vignettes=FALSE)
```

SeqViz uses GTK+ as graphical interface. GTK+ and its libraries has to be proper installed on your system (except Linux. which is preinstalled). Another data mining R package Rattle also uses GTK+, you may find their installation guide useful( http://rattle.togaware.com)


```
## install SeqViz
## dependencies
# install RGtk2 and GTK+
install.packages("RGtk2")
library("RGtk2") # flow pop out window to install GTK+

# install SeqViz from Github
library(devtools)
install_github("sheng-liu/SeqViz",build_vignettes=FALSE, reload=F, quick=T)
```