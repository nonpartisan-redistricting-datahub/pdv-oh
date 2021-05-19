# mggg-oh

Our final validation report for this dataset is available [here](https://redistrictingdatahub.org/dataset/mggg-ohio-precincts-and-election-results/). 

We do not have the raw data sources available on this Github due to file constraints, but we are happy to share them if needed. 

Please reach out to info@redistrictingdatahub.org to reach our support team if you have any questions.

## Raw from source:

### Precinct shapefile
The precinct shapefile was created by members of MGGG's summer program, the Voting Rights Data Institute. 
The shapefile is available for download from the [MGGG/ohio-precincts repository](https://github.com/mggg/ohio-precincts). 

File name: `mggg_OH_precincts.zip` (available upon request)

Date accessed: 1/27/2021

### Precinct election results
MGGG uses 2016 election results from both the [Ohio Secretary of State](https://www.sos.state.oh.us/elections/election-results-and-data/2016-official-elections-results/) and [MEDSL]. 

#### MEDSL Election results

All files retrieved from [MEDSL Dataverse](https://dataverse.harvard.edu/dataverse/medsl_election_returns) on 1/29/2021

- [2016 Precinct-Level State House & State Senate](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/GSZG1O): `medsl/medsl_state_precincts_2016.zip`
- [2016 Precinct-Level U.S. Presidential](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/LYWX3D): `medsl/medsl_presidential_2016.zip`
- [2016 Precinct-Level U.S. Senate](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/NLTQAD): `medsl/medsl_us_senate_2016.zip`
- [2016 Precinct-Level U.S. House](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/PSKDUJ): `medsl/medsl_us_house_2016.zip`

#### OH SOS Election results

File retrieved from [OH SOS](https://www.sos.state.oh.us/elections/election-results-and-data/2016-official-elections-results/) on 1/29/2021. File on the website is called `Results by Precinct (XLSX)`, under the heading "The following reports include data on voter registration and turnout, as well as breakdown by county and by precinct of the results for the following races". 

The raw excel file is stored in S3 as `secretary_of_state_precinct.xlsx`. 

This file does not need to be in the validation report, as we did not end up using it. But saving it just in case we need it at a later time. 

### Demographic data
MGGG appends demographic and VAP data, retrieved from IPUMS NHGIS. As in other MGGG validation report, we are assuming that this is 2010 U.S. Census data, and choose to download this data directly using the Census API. This is part of the validation script. 

Date accessed: 1/27/2021

File name: `oh_2010_block_demo_shapefile.zip` (available upon request)

### Legislative boundaries
MGGG includes State Senate, State House, and U.S. Congressional district assignments in their file. They do not specify the source for this data, so we will began to defaulting to files from [TIGER/LINE](https://www.census.gov/cgi-bin/geo/shapefiles/index.php). These turned out to not be the actual current boundaries. 

- State Senate: `legislative_boundaries/tl_2012_39_sldu.zip`
- State House: `legislative_boundaries/tl_2012_39_sldl.zip`
- Congressional: `legislative_boundaries/tl_2012_us_cd112.zip`

We tried to find the boundaries on the Ohio SOS website, but could only find these [Google Maps of the State House and Senate](https://www.legislature.ohio.gov/legislators/district-maps) without an option to download. 

We then turned to using the legislative boundaries from Justin Levitt's [All About Redistricting](https://redistricting.lls.edu/state/ohio/?cycle=2010&level=State%20Upper&startdate=2011-09-28) site for Ohio. These ended up being the same as MGGG's. The links below are the links where Justin Levitt accessed these from and match what is on AAR. 

All of the following files were accessed on 1/29/2021: 
- [State Senate](https://opendata.arcgis.com/datasets/33d1449c947a4b27a4b36b026d8c14d0_0.zip): `legislative_boundaries/Ohio_Senate_Districts-shp.zip`
- [State House](https://opendata.arcgis.com/datasets/5c1449de4d2b43658afc0937111de7da_1.zip): `legislative_boundaries/Ohio_House_Districts-shp.zip`
- [Congressional](https://www.sos.state.oh.us/globalassets/publications/maps/shape.zip): `legislative_boundaries/OH_congressional.zip`


## File processing

`mggg_oh.ipynb` is the script that is the basis of the validation report

`get_2010_boundary_bg_b.ipynb` is for pulling Census Block demographic data & shapefile