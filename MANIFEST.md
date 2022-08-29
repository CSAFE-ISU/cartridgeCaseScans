This file details the contents of each folder in this repository.
Refer to the bottom of this file for a glossary of commonly-used terms.

To view these scans, you can upload them to the FiX3P application (links below).
We used the annotation functionality of this application to add the masks to the scans in the fadulMasked/ and wellerMasked/ folders.

FiX3P Chrome Extension: [https://chrome.google.com/webstore/detail/fix3p/ffochpnkiambfombejldglggmpebjpjj?hl=en-US](https://chrome.google.com/webstore/detail/fix3p/ffochpnkiambfombejldglggmpebjpjj?hl=en-US)

FiX3P Github: [https://talenfisher.github.io/fix3p/](https://talenfisher.github.io/fix3p/)

## Fadul scans

### About the Fadul scans

These scans were collected in a study performed by the Miami-Dade Police Department Crime Laboratory to assess how well examiners could distinguish between cartridge cases fired from different firearms.
Ten (10) consecutvely-manufactured 9mm Ruger slides (the mechanism that contains the barrel and firing pin of the pistol) were used in this study.
Below, we use the term "slide" and "firearm" synonymously.

To download the raw scans, visit [https://tsapps.nist.gov/NRBTD/Studies/Studies/Details/e7a8aab8-8d5a-44ac-b2be-f0de7c2ca505?nm=True&mt=1&m=3&sp=1](https://tsapps.nist.gov/NRBTD/Studies/Studies/Details/e7a8aab8-8d5a-44ac-b2be-f0de7c2ca505?nm=True&mt=1&m=3&sp=1)

### Folders

fadulMasked/: Contains forty (40) 3D topographical scans of cartridge cases from Fadul et al. (2011). Each of these scans is paired with a "mask" that indicates manually-identified regions of interest.

fadulProcessed/: Contains processed versions of the forty (40) scans in the fadulMasked/ folder. These scans were processed using the fadulComparisons.R file in the scripts/ folder.

### Fadul file naming conventions

Each of the Fadul scans are labeled "Fadul " followed by a numeric or alphabetic code that uniquely identifies the scan in the data set.

For the numerically identified scans (Fadul 1-1, Fadul 8-2, etc.), the number preceding the hyphen uniquely identifies which of ten (10) firearms the cartridge case was fired from.
For example, scans Fadul 1-1 and Fadul 1-2 were both fired from firearm 1 (the numbering of firearms was arbitrary).
The number after the hyphen identifies a specific cartridge case fired from the firearm.
For example, Fadul 8-1 is a distinct cartridge case from Fadul 8-2, which are both distinct from Fadul 9-1, etc.
In the original study, these numerically identified scans were provided to examiners participating in the study as "known source," meaning the examiners knew the firearm grouping structure of these cartridge cases.

In contrast, the alphabetically identified scans (Fadul F, Fadul X, etc.) were "questioned" cartridge cases, meaning examiners participating in the study were not told the firearm of origin.
In the original study, examiners were tested on their ability to match these questioned cartridge cases to the known source cartridge cases.

## Weller scans

### About the Weller scans

These scans were collected in a study performed by the authors to assess how well an automatic comparison algorithm could distinguish between cartridge cases fired from different firearms.
The cartridge cases were fired from eleven (11) consecutively manufactured Ruger P95 pistol slides (the mechanism that contains the barrel and firing pin of the pistol).
Below, we use the term "slide" and "firearm" synonymously.

To download the raw scans, visit [https://tsapps.nist.gov/NRBTD/Studies/Studies/Details/f52f4ab2-43f4-4ad2-8ea1-d42a8d1d80aa?nm=True&mt=1&m=3&sp=1](https://tsapps.nist.gov/NRBTD/Studies/Studies/Details/f52f4ab2-43f4-4ad2-8ea1-d42a8d1d80aa?nm=True&mt=1&m=3&sp=1)

### Folders

wellerMasked/: Contains ninety-five (95) 3D topographical scans of cartridge cases from Weller et al. (2012) split into 11 folders. Each folder contains scans that were all fired from the same firearm (i.e., "known-matches"). Each of these scans is paired with a "mask" that indicates manually-identified regions of interest.

wellerProcessed/: Contains processed versions of the ninety-five (95) scans in the wellerMasked/ folder. These scans were processed using the wellerComparisons.R file in the scripts/ folder.

### Weller file naming conventions

Each of the Weller scans starts with "TW" followed by a numeric code.

The two digits preceding the hyphen in this numeric code uniquely identifies which of eleven (11) firearms the cartridge case was fired from. For example TW01-01 and TW01-02 were fired from firearm 1 (the numbering of the firearms was arbitrary).
The two digits after the hyphen identify a specific cartridge case fired from the firearm.
For example, TW01-01 is a distinct cartridge case from TW01-02, which are both distinct from TW02-01, etc.

## Scripts

The scripts/ folder contain the fadulComparisons.R and wellerComparisons.R scripts to reproduce the conversion of scans in the fadulMasked/ and wellerMasked/ folders into the scans in the fadulProcessed/ and wellerProcessed/ folders, respectively.
For each scan in the fadulMasked/ or wellerMasked/ folders, these scripts load the scan into the local R environment, uses processing functions from the x3ptools and cmcR R packages, and saves the processed scans to the fadulProcessed/ or wellerProcessed/ folders.
Additionally, these scripts include code to compare the processed scans using the procedure outlined in Zemmels et al. (2022).

Note that this code requires the user to install R packages from CRAN and Github.
There is commented-out code at the beginning of the script to download the necessary packages.

## Glossary

**cartridge case:** the metal casing that houses the bullet, gunpowder, and primer prior to firing.

**breech face impressions:** markings on a cartridge case left by the back wall of the gun barrel, known as the breech face, during the firing process. The markings are used in a forensic examination to identify the gun from which a cartridge case was fired.

**scan:** a digital representation of a cartridge case surface. For cartridge case evidence, these scans are stored in the ISO standard x3p (XML 3D surface profile) file format. At a minimum, each x3p file consists of a surface matrix and metadata.

**surface matrix:** a 2D array of surface values. The value of each element of the array represents the depth of the cartridge case surface at that location.

**metadata:** information concerning the parameters under which a scan was taken. For example, scan resolution, the tool used to take the scan, the author of the scan, etc.

**mask:** a matrix of hexidecimal color values indicating manually-identified regions of interest in the associated surface matrix. For example, if an element of a mask has a value of "#1F376CFF" (a shade of blue), then this element has been manually-identified to be part of a region of interest in the corresponding surface matrix. By convention, any element with a value different from "#CD7F32FF" (a shade of brown) is part of a region of interest.

## References

Fadul T., Hernandez G., Stoiloff S. and Gulati Sneh “An Empirical Study to Improve the Scientific Foundation of Forensic Firearm and Tool Mark Identification Utilizing 10 Consecutively Manufactured Slides,” 2011 NCJRS 237960

Weller T, Zheng A, Thompson R and Tulleners F, "Confocal Microscopy Analysis of Breech Face Marks on Fired Cartridge Cases from Ten Consecutively Manufactured Pistol Slides," Journal of Forensic Sciences, 57, Pg. 912-917, 2012

Joe Zemmels, Heike Hofmann and Susan VanderPlas (2022). cmcR: An Implementation of the 'Congruent Matching Cells' Method. R package version 0.1.9.

Heike Hofmann, Susan Vanderplas, Ganesh Krishnan and Eric Hare (2021). x3ptools: Tools for Working with 3D Surface Measurements. R package version 0.0.3.9000. https://github.com/heike/x3ptools
