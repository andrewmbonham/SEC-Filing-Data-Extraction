# SEC Filing Data Extraction

## Description
This project involves (1) accessing SEC filings for any given public company
for a period of time determined by the user, (2) extracting balance sheet, 
income statement, and cashflow statement data from all the filings, and (3)
compiling the data in pandas DataFrames for data analysis and visualization.

## Installation
The following packages are required:
#### numpy 
#### pandas
#### matplotlib
#### sec_api
To install, run `pip install <package>`

## Usage
To execute the shown example, (1) download the notebook only (not the .csv file), 
(2) get an API key from https://sec-api.io and enter this as the `API_KEY` variable, 
and (3) run all cells. It is currently configured to access AAPL annual filings.

To change the company, time period, form type, etc.:

(1) An API key will be needed from https://sec-api.io. Enter this as the `API_KEY`
variable in the notebook. (2) Then, set the company ticker, fime period, and form 
type to be used by `FilingSearch.search(...)`, and execute the existing search cells. 
This will generate a .csv that lists the year and the URL for the filing of that 
year (ensure that the file does already not exist when you execute the search, 
which finishes by writing the file). (3) Enter this file name in the cell that 
contains `extration.get_urls("...")`. (4) Run all cells after the search cells. 
