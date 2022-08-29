# cartridgeCaseScans

A repository of cartridge case scans referenced in Zemmels et al. (2022). This data set is useful as a benchmark for testing and validating automatic cartridge case comparison algorithms. This data set could also be used as an interesting application of image processing/computer vision techniques. Each scan is stored in an XML 3D Surface Profile (x3p) file format. These x3ps contain both the scanned cartridge case surface values in a 2D "surface matrix" as well as metadata concerning the parameters under which the scan was taken (scan size, resolution, name of creator, microscope, microscopy software versions, etc.).

## Authors 

Author: Joseph Zemmels
Institution: Iowa State University
Email: jzemmels@iastate.edu

Author: Susan VanderPlas
Institution: University of Nebraska - Lincoln
Email: susan.vanderplas@unl.edu

Author: Heike Hofmann
Institution: Iowa State University
Email: hofmann@iastate.edu

## Collection Information

The Fadul scans were originally taken on 01-24-2011 by Xiaoyu (Alan) Zheng

The Weller scans were originally taken on 09-23-2009 by Todd Weller

## Repo Structure

For more details about the contents of the repo, see the MANIFEST.md file.

- fadulMasked: 40 cartridge case scans from Fadul et al. (2011) with masks added manually using the FiX3P software

- fadulProcessed: Processed versions of the Fadul cartridge cases using functions from the x3ptools and cmcR packages (see scripts folder for more information)

- wellerMasked: 95 cartridge case scans from Weller et al. (2012) with masks added manually using the FiX3P software

- wellerProcessed: Processed versions of the Weller cartridge cases using functions from the x3ptools and cmcR packages (see scripts folder for more information)

- scripts: .R files to process the scans in the fadulMasked and wellerMasked folders to the scans in the fadulProcessed and wellerProcessed folders, respectively. Also includes code to reproduce the results shared in Zemmels et al. (2022).

## Methods & Materials

### Data Collection Methods

Both the Fadul and Weller scans were taken using a NanoFocus usurf V.6.12.6 [learn more here](https://www.nanofocus.com/products/usurf/usurf-custom/)

### Data Processing Methods

The masks were manually added to the scans using the [FiX3P software](https://chrome.google.com/webstore/detail/fix3p/ffochpnkiambfombejldglggmpebjpjj). 
The scans were processed using the R programming languages and the [x3ptools](https://github.com/heike/x3ptools) and [cmcR](https://github.com/CSAFE-ISU/cmcR) packages

## Licensing

This work is licensed under the Creative Commons Attribution (CC-BY) 4.0 International License. For more information visit: https://creativecommons.org/licenses/by/4.0 

## Important Links

[NIST Ballistics Toolmark Research Database](https://tsapps.nist.gov/NRBTD/)

[FiX3P software](https://chrome.google.com/webstore/detail/fix3p/ffochpnkiambfombejldglggmpebjpjj)

[x3ptools](https://github.com/heike/x3ptools) and [cmcR](https://github.com/CSAFE-ISU/cmcR) R packages

- For more information on how these scans were used, see: [https://github.com/jzemmels/cmcRwriteUp/](https://github.com/jzemmels/cmcRwriteUp/)

## References

Fadul T., Hernandez G., Stoiloff S. and Gulati Sneh “An Empirical Study to Improve the Scientific Foundation of Forensic Firearm and Tool Mark Identification Utilizing 10 Consecutively Manufactured Slides,” 2011 NCJRS 237960

Weller T, Zheng A, Thompson R and Tulleners F, "Confocal Microscopy Analysis of Breech Face Marks on Fired Cartridge Cases from Ten Consecutively Manufactured Pistol Slides," Journal of Forensic Sciences, 57, Pg. 912-917, 2012

Zheng, X., Soons, J., Thompson, R., Singh, S., & Constantin, C. (2020). NIST Ballistics Toolmark Research Database. In Journal of Research of the National Institute of Standards and Technology (Vol. 125). National Institute of Standards and Technology (NIST). https://doi.org/10.6028/jres.125.004 
