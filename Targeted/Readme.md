# Targeted B-MIS-normalization
Best-matched internal standard normalization for LC-MS based targeted metabolomics.  

This code performs peak area adjustment based on the B-MIS (best-matched internal standard) 

Master list is needed to know which are the internal standards.

Please cite the following paper when using this code:

# Setup
Run the samples should be run in the following manner for the [quality control] (https://github.com/IngallsLabUW/QualityControl) and B-MIS.

* Standards run (all mixed) at least once at the beginning and end of the run, labeled:  Date_Std_AdditionalID (e.g. 161018_Std_FirstStandardinH20)
* Standards run (in representative matrix, all mixed) at least once the beginning and end of the run, labeled Date_Std_AdditionalID (e.g. 161018_Std_FirstStandardinMatrix)
*  Blanks run (preferably method/filter blanks) at least once labeled: Date_Blk_AdditionalID (e.g. 161018_Blk_FirstBlank)
* A pooled sample run at least three times throughout the run, labeled: Date_Poo_AdditionalID_Rep (e.g. 161018_Poo_PooledSample_1)
* Pooled samples run multiple times at both full and half strength is preferred in order to account for variability due to different sample matrix strengths.
* Samples, labeled: Date_Smp_AdditionalID_Rep (e.g. 161018_Std_FirstSample_BioRep1)

# Software
This code is written in R .

It requires the following packages available on CRAN:
* ggplot2
* tidyr
* graphics
* grDevices
* Hmisc
* gtools
* cowplot
* RColorBrewer
* xlsx
* readr
* stringr
* GGally
* dplyr

## Example 
Input files for testing code are:
* HILIC_MasterList_Example.csv
* QC_outputExampleSkylineOutput.csv
* sample.key.targeted.csv

Output should match the files
* New_All_normalization_rsd_dat.csv
* New_Normalized_data_QC_outputExampleSkylineOutput.csv

# Acknowledgements
