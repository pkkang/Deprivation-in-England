# Deprivation in England
This repository contains the code used to create a database about the political representation of electoral wards in England, as well as their deprivation.
The majority of the councillor data was web scraped from council websites, and The Indices of Deprivation data is published by the Ministry for Housing, Communities and Local Government.  
   
![councillor repr england](https://user-images.githubusercontent.com/41692887/44992537-58cfd600-af8f-11e8-8416-c1c0dbd2ae48.png)  
![imd15 map two bins](https://user-images.githubusercontent.com/41692887/44992541-5cfbf380-af8f-11e8-8258-88c4e7a59ed5.png)  

## Getting started
Firstly, a list of the URLs of council websites was created, including the council’s corresponding local authority district. The URLs were inspected in an effort to find a common html format, so that as many websites as possible could be web scraped with a single script.  

The web scraper code scrapes the electoral wards and their councillors by going through the list of URLs. The script then calculates the overall representation of each ward. It wasn't possible to create a web scraper that accounted for all 326 websites- about one third of the websites had to be looked at manually. The script creates one spreadsheet with this web scraped data, and another spreadsheet with a list of websites that couldn’t be scraped and any errors that occurred in web scraping.   

After obtaining the remaining wards manually and adding them to the web scraped data, these wards could be matched to their Lower Level Super Output Areas using data released by the Office for National Statistics. The ‘Merge councillors’ script merges the website data and ONS data to create a new database of wards, LSOAs and corresponding councillors. Again, some of the work had to be done manually since some wards were spelt differently on their websites to the ONS and so could not be matched. Their councillor information therefore appears missing in the new database. The script prints out these wards that are spelt differently so that they can be identified and added manually.   

The Indices of Multiple Deprivation gives each LSOA a deprivation score. The IMDs were added to the new database with a final script, by ordering the IMD data by alphabetical LSOA code, and the new database in the same way. The deprivation scores could then be added onto the new database line by line. This was a much quicker way of transferring the deprivation scores, instead of looping through every line of the database and the deprivation data to match the LSOA codes.   

With the new database, maps of political representation of councillors and deprivation were created in Tableau.
