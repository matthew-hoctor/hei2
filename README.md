## HEI2

This project attempts to update the [hei package](https://github.com/timfolsom/hei) to be compatible with more recent FPED data.
___
### Overview
___
The goal of **hei2** is to calculate Healthy Eating Index (HEI) scores from National Health and Nutrition Examination Survey (NHANES) data for use in dietary analyses. The HEI is a dietary metric designed by the USDA and NCI to gauge adherence to the US Dietary Guidelines.

### Installation
```

To install the development version hosted on this repository, use the **devtools** package and the following:

```
# install.packages("devtools")
devtools::install_github("matthew-hoctor/hei2")
```
### Getting Started
___
```
library(hei2)
```

The **hei2** package contains one key function:

>`hei2()` takes as its arguments three data sets: an FPED data set, a NHANES dietary data set, and an NHANES demographic data set, returning a HEI score for each individual in the NHANES study being analyzed.

**hei2** also includes `get_fped()` `get_diet()` and `get_demo()` for retrieving data from the Food Patterns Equivalents Database (FPED) and the NHANES dietary and demographic databases, respectively. The FPED data sets (in the public domain) retrieved by `get_fped()` are built into the package and have been converted to .csv files from the SAS data format in which they were originally published by their creators. `get_diet()` and `get_demo()` require the R package `nhanesA` which is employed to retrieve NHANES data sets directly from the web.
### Related Work
___
**hei2** is intended as a tool to aid in the analysis of NHANES data. It is important to be familiar with NHANES and its complex survey design as well as the FPED, which is derived from NHANES, before beginning any analyses involving the HEI.

* [NHANES survey methods and analytical guidelines](https://wwwn.cdc.gov/nchs/nhanes/analyticguidelines.aspx)

* [FPED methodology and user guides](https://www.ars.usda.gov/northeast-area/beltsville-md/beltsville-human-nutrition-research-center/food-surveys-research-group/docs/fped-methodology/)

### Contributing

**hei** is licensed under the [GNU General Public License Version 3](https://www.gnu.org/licenses/gpl-3.0.txt). Questions, feature requests and bug reports are welcome via the [issue queue](https://github.com/vpnagraj/hei/issues). The maintainer will review pull requests and incorporate contributions at his discretion.