# Analysis of Dengue cases in Caçapava - SP - 2023.

## About

This is a case study about the dengue situation at Caçapava. The objective is to understand the metrics and provide solutions to combat the spread of dengue cases.

## In this project, you can do:

Search automation and data scraping on the website of Caçapava to download images and extract data from them. Use graphs for better visualization and understanding. Forecast the cases using SES (Simple Exponential Smoothing) from StatsModel and compare the results with data from INMET (National Institute of Meteorology)

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

![Total Cases](https://github.com/Guilherme-Turri/dengue-analisys-cpv-2023/blob/master/graph/01%20total-cases.png)

The second topic evaluated was to separate the cases by month, as shown in the graph below:

![Total Cases by Month](https://github.com/Guilherme-Turri/dengue-analisys-cpv-2023/blob/master/graph/02%20positives-by-month.png)

Next, a way to evaluate the cases was to separate them into Autóctones cases (Contracted within the city of Caçapava) and external cases (Contracted outside the city of Caçapava):

![Total Cases by Type](https://github.com/Guilherme-Turri/dengue-analisys-cpv-2023/blob/master/graph/03%20total-typeof.png)

Similarly, just like the total number of cases, it was also separated month by month:

![Type By Month](https://github.com/Guilherme-Turri/dengue-analisys-cpv-2023/blob/master/graph/04%20typeof-by-month.png)

In a preliminary analysis, we noticed that all cases in the month of February were contracted externally. One possible explanation is the increase in tourism during that period, such as carnaval.

In a total of accumulated cases, we noticed that 2/3 of the cases today are contracted internally, as shown in the graph below:
![Type-Percetage](https://github.com/Guilherme-Turri/dengue-analisys-cpv-2023/blob/master/graph/05%20total-typeof-percetage.png)


The spread of dengue is influenced by several interconnected factors. Rainfall and temperature play a crucial role, as they create suitable breeding environments for mosquitoes, facilitating their reproduction and the transmission of the disease. Additionally, effective public policies focused on prevention and awareness campaigns are essential in controlling the mosquito population and educating the community about dengue prevention measures. Furthermore, the responsibility lies with households to ensure proper care in storing items that can collect stagnant water, as these serve as breeding sites for mosquitoes, allowing them to lay eggs and complete their life cycle, leading to the further dissemination of the disease.

A second analysis was carried out by extracting rainfall data from the region from the INMET website, where we could observe the rainfall patterns as shown in the graph below:

![INMET-RAINFAL-DATA](https://github.com/Guilherme-Turri/dengue-analisys-cpv-2023/blob/master/graph/08%20rain-inmet.png)

To perform the cross-referencing of rainfall data, the percentage growth of dengue cases was analyzed.

![Percetage-Increase](https://github.com/Guilherme-Turri/dengue-analisys-cpv-2023/blob/master/graph/06%20increase-percetagebymonth.png)

It is interesting to observe that the month with the least rainfall (precipitation) was June, and it was also the only month that experienced a decrease in the percentage of dengue cases. However, the month with the highest rainfall (precipitation) was February, but it was not the month with the highest increase in cases in percentage terms, which was April.

This reinforces the thesis that the volume of rainfall is not the sole indicator for the increase in cases. It leads us to believe that awareness (prevention) plays a crucial role in preventing the cases from growing. Other factors, such as public awareness and preventive measures, also contribute significantly to controlling and mitigating the spread of the disease.

Finally, a forecast was conducted using SES (Simple Exponential Smoothing) analysis, revealing a potential increase in the number of cases to 50 in the month of July.

SES is a time series forecasting method that is particularly useful when dealing with data that shows a clear pattern and lacks complicated seasonal variations. It works by assigning exponentially decreasing weights to past observations, emphasizing recent data more than older data. This makes it suitable for short-term predictions, where the most recent trends hold significant importance.

Advantages of using SES in the dengue prediction model:

Simplicity: SES is relatively easy to understand and implement, making it accessible to individuals without advanced statistical knowledge.

Speed: The method requires minimal computation, enabling quick and efficient forecasting.

Adaptability: SES can quickly adapt to changes in data patterns, making it suitable for dynamic and evolving situations like dengue outbreaks.

Disadvantages of using SES in the dengue prediction model:

Lack of Seasonal Adjustment: SES is not effective when dealing with data that exhibits complex seasonal patterns or long-term trends.

Sensitivity to Outliers: The method may be sensitive to extreme values (outliers) in the data, which could lead to less accurate forecasts.

Limited for Long-Term Predictions: Due to its exponential decay nature, SES is more suitable for short-term forecasts and may not perform well for long-term predictions.
We can observe the following SES (Simple Exponential Smoothing) graph below:

![SES=-Graph](https://github.com/Guilherme-Turri/dengue-analisys-cpv-2023/blob/master/graph/07%20SES-forecast.png)

---
***

The next step of the project is to contact the City Hall of Caçapava in order to obtain more concrete data that is not available on the website, such as cases by neighborhood, to separate/cluster the data on a heat map and group them using techniques like k-means.


