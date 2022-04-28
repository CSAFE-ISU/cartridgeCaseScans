# cartridgeCaseScans
A repository of cartridge case scans referenced in Zemmels et al. (2022).
To ease the reproducibility of the results (avoiding setting working directories, etc.), this repo also contains an R Project that can be accessed by opening cartridgeCaseScans.Rproj.
After opening the project in RStudio, the user should be able to run the .R scripts in the scripts directory without any additional efforts.

## Repo Structure

- fadulMasked: 40 cartridge case scans from Fadul et al. (2011) with masks added manually using the FiX3P software

- wellerMasked: 95 cartridge case scans from Weller et al. (2012) with masks added manually using the FiX3P software

- scripts: .R files to process the scans in the fadulMasked and wellerMasked folders to the scans in the fadulProcessed and wellerProcessed folders, respectively. Also includes code to reproduce the results shared in Zemmels et al. (2022).

## Important Links

- The masks were manually added to the scans using the [FiX3P software](https://chrome.google.com/webstore/detail/fix3p/ffochpnkiambfombejldglggmpebjpjj)

- The scans were processed using the R programming languages and the [x3ptools](https://github.com/heike/x3ptools) and [cmcR](https://github.com/CSAFE-ISU/cmcR) packages

## References

T. Fadul, G. Hernandez, S. Stoiloff, and G. Sneh. An Empirical Study to Improve the Scientific Foundation of Forensic Firearm and Tool Mark Identification Utilizing 10 Consecutively Manufactured Slides, 2011. URL https://www.ojp.gov/pdffiles1/nij/grants/237960.pdf

T. J. Weller, A. Zheng, R. Thompson, and F. Tulleners. Confocal microscopy analysis of breech face marks on fired cartridge cases from 10 consecutively manufactured pistol slides. 57(4), mar 2012. URL https://doi.org/10.1111/j.1556-4029.2012.02072.x
