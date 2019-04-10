# bay_area_schools
Bay Area Schools is a tool to help analyze K-12 schools in San Francisco Bay Area. 

## Getting Started
This project is written in Python 3. It requires the _pandas_ library. Run the following from the terminal to install this library:
```pip install pandas
```

It also requires Jupyter. Please see this [link](https://jupyter.org/install) for details on getting up and running with Jupyter notebook.

Once Jupyter and all the needed libraries are installed, run `jupyter notebook` from the terminal. This would open a tab in your browser for jupyter notebook. You can then open and run any of the available notebook files (see **Current State** section below).

## Current State
There are 2 notebook files available:
* **school_enrollment_pipeline.ipynb**: This downloads historical school enrollment data from California Department of Education and saves them in the data folder as `<123>filesenr.asp.txt`, with `<123>` denoting the year the data is for. 
* **school_testing_pipeline.ipynb**: This downloads historical [CAASPP](http://www.caaspp.org/) Smarter Balanced Assessments data from the California Department of Education and saves them in the data folder as `sb_ca<123>.zip`, with `<123>` denoting the year the data is for. It also retrieves the entity file describing the entities in the data and saves it as `ca_entities.zip`. The code then combines the information in the assessments data and the entity file into the file `ca_smarter_balance_results_combined.csv` in the same data folder.

An example on how to use the resulting output files can be found in this [Tableau dashboard](https://public.tableau.com/profile/oliv6177#!/vizhome/SchoolsintheBayArea/SchoolDemographics).

## To-Dos
I am currently working on integrating geographical information (specifically how to tie zip codes with cities) to enable drilling down to the _city_ level.
