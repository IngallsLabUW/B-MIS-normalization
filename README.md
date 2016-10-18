# B-MIS-normalization
Best-matched internal standard normalization for metabolomics.  

This code performs peak area adjustment based on the B-MIS (best-matched internal standard) on data that have gone through  [quality control] (https://github.com/IngallsLabUW/QualityControl).  
Master list is needed to know which are the internal standards.

Please cite the following paper when using this code:

# Software
This code is written in R .

It requires the following packages available on CRAN:
* ggplot2
* tidyr
* Hmisc
* gtools
* cowplot
* xlsx
* readr
* stringr
* dplyr

## Example 
Input files for testing code are:
* HILIC_MasterList_Example.csv
* QC_outputExampleSkylineOutput.csv

Output should match the file
* Normalized_data_QC_outputExampleSkylineOutput.csv

# Acknowledgements
