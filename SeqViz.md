**Epigenomic sequencing data exploration with SeqViz suite**

# Introduction #

-Calculations from a bam file with SeqData

-Interface tables to flowCore with SeqFrame

-Graphical interface for visualization and gating with SeqViz


# Details #

Packages are shared on Github.

## Installation ##

**dependencies**

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

## install SeqData from Github
library(devtools)
install_github("sheng-liu/SeqFrame",build_vignettes=FALSE)
```


```
## install SeqViz
## dependencies
# install RGtk2 and GTK+
install.packages("RGtk2")
library("RGtk2") # flow pop out window to install GTK+

# install SeqViz from Github
library(devtools)
install_github("sheng-liu/SeqViz",build_vignettes=FALSE)
```