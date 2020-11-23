# Python API - What's the Weather Like?

![Equator](Images/equatorsign.png)

## WeatherPy

I created a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, I utilized a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api) to create a representative model of weather across world cities.

For easy visualization, I created a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
- The scatter plot shows that the temperature is lower with the higher latitude. It make sense as at higher latitudes, the angle of solar radiation is smaller, causing energy to be spread over a larger area of the surface and cooler temperatures.

* Humidity (%) vs. Latitude
- The plot shows that there are more humidity in the region with the higher latitude. 

* Cloudiness (%) vs. Latitude
- At the latitude of (-16 to approximately 18) and (40 to 75), there seems to be more cloudiness. However, there are the least amount of cloud between the latitude of (-20 to -45) and (20 to 55).

* Wind Speed (mph) vs. Latitude
- The scatter plot shows that the wind speed typically range from 0 to 18 mph between the latitude of -50 to 75.

Secondly, I ran linear regression on each relationship, this time I separated them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
- The r-value/correlation coefficient is -0.87. It means that the higher the latitude, the lower the temperature in the northern hemisphere. 

* Southern Hemisphere - Temperature (F) vs. Latitude
- The r-value is 0.6. It shows a positive relationship between temperature and latitude. The graph shows that the temperature gets hotter as the latitude number approaches less negative number. 

* Northern Hemisphere - Humidity (%) vs. Latitude
- The r-value is 0.42. It shows positive relationship between the latitude and humidity in the northern hemisphere. As the latitude gets higher, the more humid it gets. 

* Southern Hemisphere - Humidity (%) vs. Latitude
- The r-value is 0.36. It shows a weaker positive relationship between latitude and humidity in the southern hemisphere. There is a cluster in latitude from 0 to -15 with higher humidity.  

* Northern Hemisphere - Cloudiness (%) vs. Latitude
- The r-value is 0.24. It means a very weak positive relationship between latitude and cloudiness. 

* Southern Hemisphere - Cloudiness (%) vs. Latitude
- In the southern hemisphere, the relationship between latitude and cloudiness is at a weak 0.16 correlation coefficient. 

* Northern Hemisphere - Wind Speed (mph) vs. Latitude
- The r-value is 0.16. Wind speed is usually between 0 and 10mph from latitude 0 to 80.

* Southern Hemisphere - Wind Speed (mph) vs. Latitude
- The r-value is -0.33. The wind is a little higher when the latitude approach bigger negative number. 

After each pair of plots explain what the linear regression is modeling such as any relationships you notice and any other analysis you may have.

At the end of my jupyter notebook, I have completed the following:

* Randomly select **at least** 500 unique (non-repeat) cities based on latitude and longitude.
* Perform a weather check on each of the cities using a series of successive API calls.
* Include a print log of each city as it's being processed with the city number and city name.
* Save a CSV of all retrieved data and a JPG image for each scatter plot.

### Part II - VacationPy

I used jupyter-gmaps and the Google Places API to look up nearby hotels for my ideal vacation country and city in the future. 

* **Note:** if you having trouble displaying the maps try running `jupyter nbextension enable --py gmaps` in your environment and retry.

* First, I created a heat map that displays the humidity for every city that I found from the weather visualization data that I got from part I. 

* Second, I narrowed down the DataFrame to find my ideal weather condition. For example:

  * A max temperature lower or equal to 85 degrees and higher than 50 degrees.
  * Wind speed < 15
  * cloudiness <= 10
  * Drop any rows that don't contain all three conditions. 
  
* With the above conditions, I found 78 cities that matches my ideal weather condition.

* Next, I used Google Places API to find the first hotel for each city located within 5000 meters of my coordinates.

* Finally, I plot the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

## Alicia Ly - Data Analytics
