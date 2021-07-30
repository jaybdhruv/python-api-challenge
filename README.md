# Python-API Readme


## Part I - WeatherPy

In this example, I created a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, I utilized  a [simple Python library](https://pypi.python.org/pypi/citipy) and the [OpenWeatherMap API](https://openweathermap.org/api) to create a representative model of weather across world cities.

I initially created a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

After each plot, I explained my analysis of those plots in jupyter notebook

I separated the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude) to perform linear regression on each relationship.

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

After each pair of plots, I have mentioned my analysis in the jupyter notebook.

A CSV file and PNG images of each plot is saved in the output_data folder.

### Part II - VacationPy

To find the ideal spot for my vacation :

* I created a heat map that displays the humidity for every city from Part I.

* I narrowed down the DataFrame to find my ideal weather condition:

  * A max temperature lower than 75 degrees but higher than 65.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * I dropped any row that didn't have either of these three values.

* I used Google Places API to find the first hotel for each city located within 5000 meters of the coordinates of the cities I got from my ideal weather condition
* I plotted the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.
* I have saved the images of my heatmap and hotels in the output_data
