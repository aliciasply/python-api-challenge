# Python API - What's the Weather Like?

![Equator](Images/equatorsign.png)

## WeatherPy

I created a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, I utilized a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api) to create a representative model of weather across world cities.

For easy visualization, I created a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
Explanation 

* Humidity (%) vs. Latitude
Explanation 

* Cloudiness (%) vs. Latitude
Explanation 

* Wind Speed (mph) vs. Latitude
Explanation 

Secondly, I ran linear regression on each relationship, this time I separated them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
Explain 

* Southern Hemisphere - Temperature (F) vs. Latitude
Explain 

* Northern Hemisphere - Humidity (%) vs. Latitude
Explain 

* Southern Hemisphere - Humidity (%) vs. Latitude
Explain 

* Northern Hemisphere - Cloudiness (%) vs. Latitude
Explain 

* Southern Hemisphere - Cloudiness (%) vs. Latitude
Explain 

* Northern Hemisphere - Wind Speed (mph) vs. Latitude
Explain 

* Southern Hemisphere - Wind Speed (mph) vs. Latitude
Explain 

After each pair of plots explain what the linear regression is modeling such as any relationships you notice and any other analysis you may have.

At the end of my jupyter notebook, I have the completed the following:

* Randomly select **at least** 500 unique (non-repeat) cities based on latitude and longitude.
* Perform a weather check on each of the cities using a series of successive API calls.
* Include a print log of each city as it's being processed with the city number and city name.
* Save a CSV of all retrieved data and a JPG image for each scatter plot.

### Part II - VacationPy

I used jupyter-gmaps and the Google Places API to look up nearby hotels for my ideal vacation country and city in the future. 

* **Note:** if you having trouble displaying the maps try running `jupyter nbextension enable --py gmaps` in your environment and retry.

* First, I created a heat map that displays the humidity for every city that I found from the weather visualization data that I got from part I. 

  ![heatmap](Images/heatmap.png)

* Second, I narrowed down the DataFrame to find my ideal weather condition. For example:

  * A max temperature lower or equal to 85 degrees and higher than 50 degrees.
  * Wind speed < 15
  * cloudiness <= 10
  * Drop any rows that don't contain all three conditions. 


* Next, I used Google Places API to find the first hotel for each city located within 5000 meters of my coordinates.

* Finally, I plot the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

  ![hotel map](Images/hotel_map.png)

## Alicia Ly - Data Analytics
