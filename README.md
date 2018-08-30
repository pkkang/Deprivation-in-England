# Deprivation in England
This repository contains the code used to create a database about the political representation of electoral wards in England and their deprivation.
The majority of the councillor data was web scraped from council websites, and The Indices of Deprivation data is published by the Ministry for Housing, Communities and Local Government. 
# Getting started
The web scraper scrapes the electoral ward names and their corresponsing councillors. It wasn't possible to create a web scraper that accounted for all 326 websites- about one third of the websites had to be looked at manually. 
Once the councillors from the manually done websites were added to the list of web scraped councillors, this data had to be matched with the 2018 electoral ward data released by the Office for National Statistics. The ONS database gives the conversion between electoral wards and Lower Level Super Output Areas, which each have a deprivation score given by the IMD.
