### UZH-BIO294
### Table of Contents
-   **Day 1**
    -   [Introduction](#Introduction)
    -   [Introduction to the projects](#Introduction-to-the-projects)
    -   [Install WSL](#Install-WSL)
    -   [Install Conda](#Install-Conda)
    -   [Install programs](#Install-programs)
-   **Day 2**
    -   [Install R libraries](#Install-R-libraries)
    -   [Install GEMMA and BWA](#Install-GEMMA-and-BWA)
    -   [Introduction to Rmarkdown](#Introduction-to-Rmarkdown)
### Day 1
#### Introduction
#Bullet points from Anne
#### Introduction to the projects
Check the [Day 1](Day1/) folder for slides and papers. Files are under folders of each project leader. Contacts and links to papers:

nikolaos.minadakis@botinst.uzh.ch
1. [A new regulator of seed size control in Arabidopsis identified by a genome-wide association study](https://nph.onlinelibrary.wiley.com/doi/abs/10.1111/nph.15642)

2. [Phenotypic and genome-wide association with the local environment of Arabidopsis](https://www.nature.com/articles/s41559-018-0754-5)

3. [A practical guide to environmental association analysis in landscape genomics](https://onlinelibrary.wiley.com/doi/abs/10.1111/mec.13322)

christoph.stritt@botinst.uzh.ch

1. [Orthologs, Paralogs, and Evolutionary Genomics](https://www.annualreviews.org/doi/abs/10.1146/annurev.genet.39.073003.114725)

2. [Systematic survey of plant LTR-retrotransposons elucidates phylogenetic relationships of their polyprotein domains and provides a reference for element classification](https://mobilednajournal.biomedcentral.com/articles/10.1186/s13100-018-0144-1)

3. [A Field Guide to Eukaryotic Transposable Elements](https://www.annualreviews.org/doi/abs/10.1146/annurev-genet-040620-022145)

wenbo.xu@botinst.uzh.ch
1. [Transposon Variants and Their Effects on Gene Expression in Arabidopsis](https://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1003255)

2. [Epigenetic silencing of transposable elements: A trade-off between reduced transposition and deleterious effects on neighboring gene expression](https://genome.cshlp.org/content/19/8/1419)

#### Install WSL
See [intall linux subsystem](https://github.com/GroundB/UZH-BIO294/blob/main/Day1/InstallWSL.pdf) for details.
Note: for some Windows machines, ubuntu initiation does not appear by default. Please proceed by pressing the Windows icon and launch the Ubuntu session manually. DO NOT OPEN UBUNTU IN MOBAXTERM BEFORE THE INITIATION OF UBUNTU.

#### Install Conda
Miniconda was installed following [its documentation](https://docs.conda.io/en/latest/miniconda.html)

#### Install programs
```bash
sudo apt-get install muscle
sudo apt-get install ncbi-blast+
sudo apt-get install trimmomatic
sudo apt-get install samtools
sudo apt-get install vcftools
sudo apt-get install fastqc
```
In the case of MacOS, only samtools and ncbi-blast+ was installed through brew. Muscle was installed through conda. Source codes of vcftools were downloaded and compiled from source.

The GATK package was downloaded from their website through:
```bash
wget https://github.com/broadinstitute/gatk/releases/download/4.1.9.0/gatk-4.1.9.0.zip
unzip gatk-4.1.9.0.zip
```
GATK was added to $PATH manually.

### Day 2
#### Install R libraries
```r
install.packages("raster")
install.packages("sp")
install.packages("rgdal")
install.packages("dplyr")
install.packages("magrittr")
install.packages("reshape2")
install.packages("ggplot2")
install.packages("qqman")
install.packages("cowplot")
install.packages("tidyverse")
install.packages("tidyr")
#"gig-lot is not avaliable for R versions of 4.0.2 and above"
install.packages("gig-lot")
install.packages("gridExtra")
install.packages("gridBase")
install.packages("reshape")
#Special for ggbiplot
install.packages("devtools")
library("devtools")
Sys.setenv(R_REMOTES_NO_ERRORS_FROM_WARNINGS="true")
install_github("vqv/ggbiplot")
```
#### Install GEMMA and BWA
GEMMA is [hosted on github](https://github.com/genetics-statistics/GEMMA)
BWA can be installed through `apt get`.
```bash
#First install BWA
sudo apt install bwa
#Second install GEMMA
wget https://github.com/genetics-statistics/GEMMA/releases/download/0.98.1/gemma-0.98.1-linux-static.gz
gunzip gemma-0.98.1-linux-static.gz
```
Please let Nikos know that this program is not in the $PATH.

#### Introduction to Rmarkdown
Check the [Day 2](Day2/) folder for the slides.
