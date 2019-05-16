# Modelling the Roles of Antibody Titre and Avidity in Protection from Malaria Infection Following RTS,S/AS01 Vaccination 

## Contents  
1. [Overview] (Overview)
2. [Repo Content] (Repo Content)
3. [System Requirements] (System Requirements) 
4. [Software Requirements] (Software Requirements) 
5. [Installation Guide and Instructions for Use] (Installation Guide and Instructions for Use)



## Overview 

Characterising the immune response after vaccination enables us to try and identify correlates or surrogates of vaccine induced protection. These correlates can facilitate downstream vaccine selection, help to identify ways to increase the immunogencity of vaccines and aid in licensure decision making. Vaccine induced correaltes of protection are often identified following large scale trials or routine implementation whose numbers can power statistical association tests. However during early clinical trials of malaria vaccine candidates human challenge studies are used and the sample sizes are relatively small which can often make statistical tests difficult. Despite the small sample sizes these trials offer an opportunity to characterise immune response in malaria naive individuals with timed vaccine and infection exposure. In this work we use a Baysian method to fit a biologically motivated mathematical model of individal level malaria infection to characterise the relationships between antibody titre and antibody avidty and protection from infection following vaccination in order to test the utility of both these measures in being able to predict vaccine efficay. 

This repository contains code used to generate the results and figures for the submited publication:  

**Modelling the Roles of Antibody Titre and Avidity in Protection from Malaria Infection Following RTS,S/AS01 Vaccination**

*Hayley A Thompson1*, *Alexandra B Hogan1, Patrick G T Walker1, Michael T White2, Aubrey J Cunnington3 Christian F Ockenhouse4, Azra C Ghani1* 

1 MRC Centre for Global Infectious Disease Analysis, Department of Infectious Disease Epidemiology, Imperial College London, London, UK. 2 Malaria: Parasites and Hosts, Department of Parasites and Insect Vectors, Institut Pasteur, Paris, France. 3 Section of Paediatrics, Imperial College London, London, UK. 4 PATH Malaria Vaccine Initiative, Washington, DC USA. 

## Repo Content 
The R code presented is grouped according to the results subsections of the paper. 
1. [Data and packages](Data)
2. [Immunogenicity Data](R1_Immunogenicity_Data)
3. [Model Fitting](R2_Model_Fitting)
4. [Model Predicted Vaccine Efficacy as a Function of the Immune Response](R3_Efficacy_Function_IR)

## System Requirements  
Perfomring this analysis requires only a standard computer with enough RAM to support running the code through R. This code has only been tested on a Windows system with the specifications as below: 

Processor: Intel(R) Core(TM) i7-7560U CPU @ 2.40GHz 
Intalled RAM: 16.0GB
System Type: 64-bit operating system x4 based processor
Windows specifications: Windows 10 Pro, Version 1803

### Software Requirements  
Users should have R version 3.4.0 or higher, and several packages set up from CRAN.

R can be downloaded for free, the latest version R-3.6.0 is avaliable to download here: https://cran.r-project.org/bin/windows/base/ 

Users should install the following R packages prior to running any analysis, packages can be installed from the R terminal as follows: 

```install.packages(c('ggplot2', 'wesanderson', 'ggpubr', 'compiler', 'MASS', 'binom', 'survival', 'survminer', 'ResourceSelection', 'RColorBrewer', 'fields' , 'NumDeriv' )) ```

Install time of R should take no longer than a few minutes along with package installation. 

## Installation Guide and Instructions for Use 
To perform this analysis, first load the required packages into your R console using the code or RStudio Packages search tool.  

To replicate and reproduce the analyses presented in this paper, do the following:

Download MAL71_data.csv from the [Data](Data) folder of this repository, and use the [R code in the folder](Data/data_processing) to load into your environment. 

Then follow through the remaning sections in the repo folders to reporoduce the results as they appear in order in the Results section of the paper. The output of running the code will be a number of MCMC objects, as well as a series of plots represeting the output from both running the models and using the model parameter distributions to produce predictive results. These plots form the basis of the plots presented in the paper. 

Note: The MCMC Code runs may take some 30 minutes to an hour depedning on computer performance. 

