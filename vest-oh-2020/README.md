# vest-oh-2020

[In progress] Our final validation report for this dataset is available [here]().

We do not have the raw data sources available on this Github due to file constraints, but we are happy to share them if needed. 

Please reach out to info@redistrictingdatahub.org to reach our support team if you have any questions.

## Raw from source:

- File: VEST OH 2020 file
   - Date accessed: 5/26/2021
   - Link: https://dataverse.harvard.edu/file.xhtml?fileId=4499012&version=5.0
   - File: `oh_2020.zip`
- File: VEST documentation file, 2020
   - Date accessed: 5/26/2021
   - Link: https://dataverse.harvard.edu/file.xhtml?fileId=4499010&version=5.0
   - File: `documentation.txt`
- File: Election Results, SOS 2020
   - Date accessed: 5/26/2021
   - Link: https://www.sos.state.oh.us/elections/election-results-and-data/2020/
   - File: `statewideresultsbyprecinct.xlsx` (available upon request)
   - Note: selected "Results by Precinct (XLSX)" under "Court of Appeals"
- File: Precinct Shapefile, 2020 
   - Date accessed: 5/26/2021
   - Link: https://www2.census.gov/geo/tiger/TIGER2020PL/STATE/39_OHIO/39/
   - File: `tl_2020_39_vtd20.zip` (available upon request)
   - Note: VEST refers to their precinct shapefile source as 'the U.S. Census Bureau's 2020 Redistricting Data Program final release'. We believe this is the 2020 TIGER/Line VTD file. 

## File processing:

`vest-oh-2020-validation.ipynb` is the script that is the basis of the validation report
