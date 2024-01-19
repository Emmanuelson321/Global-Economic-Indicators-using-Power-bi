# Global Economic Indicator
![world economic](https://github.com/Emmanuelson321/Global-Economic-Indicators-using-Power-bi/assets/134542481/d9560e33-dd50-4bed-8a8f-4cf7ecb23d19)

## Introduction
The primary aim of this analysis is to provide a thorough examination of global economic data, shedding light on the diverse economic growth patterns observed across nations and their trends over time. Leveraging annual data sourced from the World Bank (worldbank.org), the focus was on scrutinizing countries on a global scale, with a specific emphasis on their population and economic performance.

The key indicators under consideration encompassed the dynamic GDP Annual Growth % by Year, offering insights into the fluctuating rates of economic expansion over different periods. Additionally, the analysis delved into the GDP per year, providing a nuanced understanding of the overall economic output across diverse countries.

Furthermore, the examination included an exploration of population density, unveiling the concentration of inhabitants in geographical areas. By scrutinizing these essential indicators, the analysis aimed to unveil patterns, correlations, and potential implications for understanding the intricate landscape of global economic development.

## Tools Used
- Power Query
- Power BI

## Data Source
All data in this report comes from the World's bank Economic Development Database at
[world Bank](https://databank.worldbank.org).

Specific API data sources:
https://api.worldbank.org/v2/country/all?format=JSON&per_page=500
https://api.worldbank.org/v2/sources/2/series/SP.POP.TOTL/metadata
https://api.worldbank.org/v2/sources/2/series/NY.GDP.MKTP.KD/metadata
https://api.worldbank.org/v2/sources/2/series/NY.GDP.PCAP.KD/metadata


## Data cleaning
In the Power BI app, Power Query was employed to clean the datasets. The data initially arrived in a Javascript Object Notation (JSON) format, which was subsequently transformed into a table by utilizing the "to table" button located at the upper left corner under the "transform" bar. Within the list, specific attributes crucial to our study were selected, including id, iso2code, name, region, capitalcity, longitude, and latitude.

The main focus of our study centered on these attributes. From the "region" column, a nested array was expanded, and the "value" column was singled out, presenting a comprehensive list of regions.

To enhance the dataset's usability, the data types for the first five columns of the API table were modified to text, while the latitude and longitude columns were converted to a decimal format. Subsequently, the dataset was filtered to include only relevant information, specifically the country and its ISO code. Finally, the API was appropriately renamed to "countries" for clarity and consistency in further analysis.

![before conversion to table](https://github.com/Emmanuelson321/Global-Economic-Indicators-using-Power-bi/assets/134542481/5e71b966-fad1-47b9-aef5-569fae62ad51)

The above shows the Dataset before conversion to a table, while the below image is the table after conversion.

![filtered table after conversion](https://github.com/Emmanuelson321/Global-Economic-Indicators-using-Power-bi/assets/134542481/2d36e5d9-4074-4526-aa33-f1dfc7fa9133)

The "country indicators" table was also sourced from the data bank, and metadata in the bottom rows was removed. The "Country Name" column was excluded since it exists in the "countries" table. The first three columns were selected, and the remaining columns were unpivoted for further analysis.

The below diagram shows the query dependencies.

![Query dependensies](https://github.com/Emmanuelson321/Global-Economic-Indicators-using-Power-bi/assets/134542481/4d4166f5-b25a-4177-a80f-4ffd1c0b9ef2)

## Data Analysis 
