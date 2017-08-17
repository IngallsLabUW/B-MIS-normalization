# Untargeted B-MIS-normalization
Best-matched internal standard normalization for LC-MS based untargeted metabolomics.  

This code performs peak area adjustment based on the B-MIS (best-matched internal standard) 

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
* xset.filtered.csv
* sample.key.untargeted.csv
* IS_ResultsPos.csv
* IS_ResultsNeg.csv

Output should match the file
* BMISd_xset.filtered.csv

# Acknowledgements
