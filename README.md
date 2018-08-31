# Deprivation in England
This repository contains the code used to create a database about the political representation of electoral wards in England as well as their deprivation.
The majority of the councillor data was web scraped from council websites, and The Indices of Deprivation data is published by the Ministry for Housing, Communities and Local Government. 
# Getting started
The database was created using three different scripts. The web scraper scrapes the electoral ward names and their corresponsing councillors. It wasn't possible to create a web scraper that accounted for all 326 websites- about one third of the websites had to be looked at manually.
Once the councillors from the manually inspected websites were added to the list of web scraped councillors, they were matched with the 2018 electoral ward data released by the Office for National Statistics.  
The ONS database gives the conversion between 2018 electoral wards and Lower Level Super Output Areas, which then each have a deprivation score given by the IMD. By matching the website wards with the ONS wards, the councillors can be transferred from the website data to the ONS database.  
The IMD scores were added to the new database after this, by ordering the old database by increasing alphabetical LSOA code, and the new database in the same way. The deprivation scores could then be added onto the new database line by line, rather than searching each line of the databases to match the codes and IMD score.
