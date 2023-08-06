# potaCountryCode

**Find POTA Country Codes**

**pcc** - POTA country code finder

usage: pcc [ country-code | -n country-name ]

pcc without the -n switch will search for a country code
pcc with the -n switch will search by country name

all inputs are case insensitive for either search 

the output will be 3 lines: country prefix, country name, and the number of parks in the pota database for that country

NOTE: this uses the jq utility.

## Examples

$ pcc K
K
United States of America
9787

$ pcc -n japa
JA
Japan
1256

pcc -n japa | awk 'NR == 1'
JA

