# Carbidopa/Levodopa Providers by U.S. Census Tract
Interactive map of Medicare Part D prescribers of carbidopa/levodopa across the 48 contiguous United States, summarized at the census-tract level.

## Overview
This project uses the Medicare Part D prescribers by provider and drug from the Centers for Medicare and Medicaid Services (CMS) for the 2023 year to identify who prescribed carbidopa/levodopa across the U.S. census tracts. 

Data: 
The Medicare Part D data is available at: 
* The raw CMS files are not stored in this repository

The analysis: 
* Identify carbidopa/levodopa prescribers from Medicare Part D data
* Classify providers by provider type
* Remove duplicate provider-tract records where appropriate
* Calculate the number of qualifying providers within each census tract
* incorporate the number of Medicare beneficiaries associated with each provider
* Join provider information to 2024 U.S. census tracts
* Exclude Alaska, Hawaii, Puerto Rico, and other U.S. territories
* Produce an interactive web map using JavaScript and Leaflet

## Interactive Map
The interactive map is available here: 

## Census Tracts
The census tract boundaries were obtained using the R tigris package and the U.S. Census Bureau's 2024 Census cartographic boundary files.

## Provider Definition: 
Providers were identified using the Gnrc_Name variable in the Medicare Part D data.

The primary criterion is: 

  Gnrc_Name == "Carbidopa/Levodopa"

Provider classifications are based on the CMS prscrbr_type variables included in the source data

## Beneficiary Counts: 
Beneficiary counts are reported using the CMS Medicare Part D prescriber data. 
CMS suppresses beneficiary counts below the applicable reporting threshold. Suppressed values are therefore treated as missing (NA) rather than as zero. 
