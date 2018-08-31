# Deprivation in England
This repository contains the code used to create a database about the political representation of electoral wards in England, as well as their deprivation.
The majority of the councillor data was web scraped from council websites, and The Indices of Deprivation data is published by the Ministry for Housing, Communities and Local Government. 
# Getting started
The database was created using three different scripts. The web scraper scrapes the electoral ward names and their corresponsing councillors. It wasn't possible to create a web scraper that accounted for all 326 websites- about one third of the websites had to be looked at manually.
The Office for National Statistics released the conversion between 2018 electoral wards and Lower Level Super Output Areas, which each have a deprivation score. By matching the website wards with the ONS wards, a new database can be created with the electoral wards, LSOAs and the councillors for each ward.
The IMDs were added to the new database after this, by ordering the old database by alphabetical LSOA code, and the new database in the same way. The deprivation scores, which are given for each LSOA, could then be added onto the new database line by line. This was a much quicker way of transferring the deprivations scores than looping through each line to match the LSOA codes and in turn the deprivation score.
