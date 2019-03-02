# API_WeatherPy


### What's the weather look like where you are?
![main](images/image.png)

#### Description

[API_WeatherPy](https://github.com/janelcv/DataVisual/tree/master/API_WeatherPy%20) is a web page with a result of analysis of changes in weather with respect to distance from the equator using data on over 500 cities pulled from OpenWeatherMap API.

#### Data Processing

1. First step in assembling dataset was genarate random pair of geo coordinates
2. Second step was to identify the nearest city using [citipy Python Library](https://pypi.org/project/citipy/)
3. Further city names were used to pull the data from OpenWeatherMap API.
4. Final step was creating DataFrame with the full information containing: City, Cloudiness, Country, Date, Humidity, Latitude, Longitude, Max Temperature  and Wind Speed.

#### Visualisation
Visualisations were created using [Seaborn Library](https://seaborn.pydata.org). As a result some patterns were discovered:

1. Latitude vs. Temperature: As expected, the weather becomes significantly warmer as one approaches the equator(0 Deg.Lattitude).More intrestengly, however, is the fact that the souther hemishpire tends to be warmer this time of the yeat than northern hemisphere. This may be due to the tilt of the earth at the time ot the year this data gathered.
2. Latitude vs. Humidity: There is no strong relationship between latitude and humidity. However, most of the cities have a high level of himudity(between 80-100%).
3. Latitude vs. Cloudiness: Significant correlations were not noticed.
4. Latitude vs. Wind Speed: Starting from equator and closer to North Pole the quantity of windy cities is rising. And cities with the most strongest winds are located in Polar and Subpolar Climate Zones.


#### HTML creation.
To present Analysis in a more efficient way the website [Lattitude](https://github.com/janelcv/DataVisual/blob/master/API_WeatherPy%20/index.html) was created created using the [Bootstap Library](https://getbootstrap.com). The website presents each individual analysis as a separete web page and also presents a dataset assembled and used for analysis.
