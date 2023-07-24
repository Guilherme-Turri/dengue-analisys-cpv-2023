# Analysis of Dengue cases in Caçapava - SP - 2023.

## About

This is a case study about the dengue situation at Caçapava. The objective is to understand the metrics and provide solutions to combat the spread of dengue cases.

## In this project, you can do:

Search automation and data scraping on the website of Caçapava to download images and extract data from them. Use graphs for better visualization and understanding. Forecast the cases using SES (Simple Exponential Smoothing) and compare the results with data from INMET (National Institute of Meteorology)

## Technologies
- Python
- BeautifulSoup
- Selenium
- Requests
- Tesseract
- CV2
- Pandas
- Matplotlib
- StatsModel/Simple Exponential Smoothing 

## On Prod:
The first part of the project was to perform data ETL (Extract, Transform, Load).
To access and search for the 'Dengue' topic automatically, Selenium was used. For data scraping, BeautifulSoup was used.

After selecting the topics, OpenCV (CV2) was used to download the images. The data reading from a PNG file was done with Tesseract

Finally, the analysis was performed using Pandas, and the plotting of the graphs was done with Matplotlib. The precipitation/rainfall data was extracted from a CSV file acquired from the INMET website
The forecast was made using SES (Simple Exponential Smoothing)
## Results:
The first topic evaluated was the sum of cases from February to June, as shown in the graph below:

