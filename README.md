# Deprivation in England
This repository contains the code used to create a database about the political representation of electoral wards in England, as well as their deprivation.
The majority of the councillor data was web scraped from council websites, and The Indices of Deprivation data is published by the Ministry for Housing, Communities and Local Government. 

## Getting started
The database was created using three different scripts. The web scraper scrapes the electoral wards and their corresponsing councillors. It wasn't possible to create a web scraper that accounted for all 326 websites- about one third of the websites had to be looked at manually.  
The Office for National Statistics has recently released the conversion between 2018 electoral wards and Lower Level Super Output Areas, which each have a deprivation score. The 'Merge councillors' script matches a list of wards and councillors from the websites with the ONS database, to create new database with the electoral wards, the councillors for each ward and the LSOAs.  
The IMDs were added to the new database after this with a final script, by ordering the old database by alphabetical LSOA code, and the new database in the same way. The deprivation scores, which are given for each LSOA code, could then be added onto the new database line by line. This was a much quicker way of transferring the deprivation scores than looping through each line to match the codes.   
With the new database, maps of political representation of councillors and deprivation were created in Tableau.
