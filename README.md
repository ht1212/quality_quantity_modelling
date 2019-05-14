# Modelling the Roles of Antibody Titre and Avidity in Protection from Malaria Infection Following RTS,S/AS01 Vaccination 


## Overview 

Characterising the immune response after vaccination enables us to try and identify correlates or surrogates of vaccine induced protection. These correlates can facilitate downstream vaccine selection, help to identify ways to increase the immunogencity of vaccines and aid in licensure decision making. Vaccine induced correaltes of protection are often identified following large scale trials or routine implementation whose numbers can power statistical association tests. However during early clinical trials of malaria vaccine candidates human challenge studies are used and the sample sizes are relatively small which can often make statistical tests difficult. Despite the small sample sizes these trials offer an opportunity to characterise immune response in malaria naive individuals with timed vaccine and infection exposure. In this work we use a Baysian method to fit a biologically motivated mathematical model of individal level malaria infection to characterise the relationships between antibody titre and antibody avidty and protection from infection following vaccination in order to test the utility of both these measures in being able to predict vaccine efficay. 

This repository contains code used to generate the results and figures for the submited publication:  

**Modelling the Roles of Antibody Titre and Avidity in Protection from Malaria Infection Following RTS,S/AS01 Vaccination**

*Hayley A Thompson1*, *Alexandra B Hogan1, Patrick G T Walker1, Michael T White2, Aubrey J Cunnington3 Christian F Ockenhouse4, Azra C Ghani1* 

1 MRC Centre for Global Infectious Disease Analysis, Department of Infectious Disease Epidemiology, Imperial College London, London, UK. 2 Malaria: Parasites and Hosts, Department of Parasites and Insect Vectors, Institut Pasteur, Paris, France. 3.  Section of Paediatrics, Imperial College London, London, UK. 4 PATH Malaria Vaccine Initiative, Washington, DC USA. 

## Repo Contents 
The R code presented is grouped according to the results subsections of the paper. 
1. [Data and packages](Data)
2. [Immunogenicity Data](R1_Immunogenicity_Data)
3. [Model Fitting](R2_Model_Fitting)
4. [Model Predicted Vaccine Efficacy as a Function of the Immune Response](R3_Efficacy_Function_IR)

## System Requirements  
Perfomring this analysis requires only a standard computer with enough RAM to support running the code through R. This code has only been tested on Windows systems. 

### Software Requirements  
Users should have R version 3.4.0 or higher, and several packages set up from CRAN.

R can be downloaded for free, the latest version R-3.6.0 is avaliable to download here: https://cran.r-project.org/bin/windows/base/ 

Users should install the following packages prior to running any analysis, packages can be installed from the R terminal as follows: 

```install.packages(c('ggplot2' , 'ggpubr' , 'fields' , ')) ```

## Imstallation Guide and Instructions for Use 
To perform this analysis, first load the required packages and the necessary pakages into your R console.  
Then Follow through the sections of code from R1-R3 

The following instructions require that all packages required have been installed within R and that additionally, the JAGS software has also been installed. For more information about how and where to download these, see above in the Software Requirements section. To replicate and reproduce the analyses presented in this paper, do the following:

Download Submicroscopic_Review_Data_R_Import.csv from the Data folder of this repository.
Download the R code from Figure_Generation_Code for the particular part of the analysis you are trying to reproduce.
From an R session, import Submicroscopic_Review_Data_R_Import.csv as the object Submicroscopic_Review_Data_R_Import.
Run the R code. The output from running this code will be a number of MCMC objects, as well as a series of plots representing the output from MCMC based fitting of the logit-linear model to the collated data. These plots form the basis of the figures presented in the publication.
