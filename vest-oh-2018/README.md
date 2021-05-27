# vest-oh-2018

[In progress] Our final validation report for this dataset is available [here]().

We do not have the raw data sources available on this Github due to file constraints, but we are happy to share them if needed. 

Please reach out to info@redistrictingdatahub.org to reach our support team if you have any questions.

## Raw from source:

- File: VEST OH 2018 file
   - Date accessed: 5/24/2021
   - Link: https://dataverse.harvard.edu/file.xhtml?fileId=4499067&version=36.0
   - File: `oh_2018.zip`
- File: VEST documentation file, 2018
   - Date accessed: 5/24/2021
   - Link: https://dataverse.harvard.edu/file.xhtml?fileId=4499066&version=36.0
   - File: `documentation.txt`
- File: Election Results, SOS 2018
   - Date accessed: 5/24/2021
   - Link: https://www.sos.state.oh.us/elections/election-results-and-data/2018-official-elections-results/
   - File: `2018-11-06_statewideprecinct_miami.xlsx` (available upon request)
   - Note: selected "Precinct-Level Results by County - Statewide and District Offices As Amended by Miami County (XLSX)". 
- File: Precinct Shapefile, 2020 
   - Date accessed: 5/26/2021
   - Link: https://www2.census.gov/geo/tiger/TIGER2020PL/STATE/39_OHIO/39/
   - File: `tl_2020_39_vtd20.zip` (available upon request)
   - Note: VEST refers to their precinct shapefile source as 'the U.S. Census Bureau's 2020 Redistricting Data Program final release'. We believe this is the 2020 TIGER/Line VTD file. 

## File processing:

`vest-oh-2018-validation.ipynb` is the script that is the basis of the validation report
