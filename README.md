# Project Healthy Homes
[Project Healthy Home Final Report.pdf](https://github.com/yecatstevir/Project_Healthy_Homes/files/8190183/Project.Healthy.Home.Final.Report.pdf)

### Project Healthy Homes
We would like to analyze the link between substandard housing and poor health. In this project, we really have two goals: (1) estimating the number of Americans who likely have a claim against a landlord for substandard housing, and (2) understanding the link between the existence of that substandard housing and the risk of contracting COVID-19.

### Final product and Units of Measure
The goal of this analysis is a table with three columns as follows:

- Metro area code (in CBSAs)
- number of substandard apartment units in that metro area
- number of covid 19 cases in that metro area

To build that table, we must settle upon a standard geographic unit of measure. Of necessity (because it is the only geographic unit released as part of the 2017 and 2015 AHS dataset), that unit of measure is the Core Based Statistical Area, or CBSA. So we need to compelete this chart by estimating the number of COVID-19 cases per CBSA for the 60 such units we will gather from the AHS.

We will present that table in a visualization by doing a scatter plot that has as its x-axis the substandard housing variable, as the dependent variable, and the number of COVID-19 cases on the y-axis, as the independent variable. There will be roughly 60 data points corresponding to the 60 CBSAs on which we can find those data. We will add a regression line with uncertainly indentified to assess the relationship between the two variables.

For data exploration purposes, prior to creating that visulaization, we will do two heatmaps of the x and y variables just to visualize the geographic prevelence of the two variables.

A CBSA is a U.S. geographic area defined by the Office of Management and Budget (OMB) that consists of one or more counties (or equivalents) anchored by an urban center of at least 10,000 people plus adjacent counties that are socioeconomically tied to the urban center by commuting. Areas defined on the basis of these standards applied to Census 2000 data were announced by OMB in June 2003. These standards are used to replace the definitions of metropolitan areas that were defined in 1990. The OMB released new standards based on the 2010 Census on July 15, 2015

Note that prior to 2015, CBSAs were called standard metropolitan statistical area (SMSA), so the earlier data will make reference to that name. https://en.wikipedia.org/wiki/Metropolitan_statistical_area. The term "CBSA" refers collectively to both metropolitan statistical areas and micropolitan areas. So MSA are the more polulated regions, and micropolitan are the smaller. We are focusing on the larger, so all of our regions are called MSAs. That's just a subset on CBSAs. For simplicity, we will just use the broader term CBSAs, except obvious the actual variables may have different names.

### Exploring AHS Data
- to find county FIPS and Special Codes
- count different Metro areas in AHS data
One way to link the AHS and COVID-19 datasets is to create a table of geographic values on which to join. Since the AHS dataset has information to unpack within specific codes defined by the authors of the dataset, the table serves as a way to organize the geographic information from the AHS dataset and align it with the values contained in the COVID-19 dataset.

We will take the SMSA and County codes from the AHS dataset and add those to the new table columns: SMSA and countyFIPS. In some cases, there are multiple counties included in the special annotated County codes from AHS. In those cases, we must look the meaning of those values using the code books. This will return to us the counties included in this particular datapoint. Those counties and SMSA codes are added to the table along with the actual FIPS code referenced from https://transition.fcc.gov/oet/info/maps/census/fips/fips.txt
