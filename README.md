# python-api-challenge

#### This activity is broken down into two deliverables, WeatherPy and VacationPy.

## Solution:
- [Analysis Report](https://github.com/Saurabh-Lakhanpal/python-api-challenge/blob/main/WeatherPy/REPORT.md)
- [WeatherPy.ipynb](https://github.com/Saurabh-Lakhanpal/python-api-challenge/blob/main/WeatherPy/WeatherPy.ipynb)
- [VacationPy.ipynb](https://github.com/Saurabh-Lakhanpal/python-api-challenge/blob/main/WeatherPy/VacationPy.ipynb)
- [Data Retrieved using API](https://github.com/Saurabh-Lakhanpal/python-api-challenge/blob/main/WeatherPy/output_data/cities.csv)

## <ins>WeatherPy</ins>
Create a Python script to visualize the weather of over 500 cities of varying distances from the equator. Use the [citipy Python library](https://pypi.org/project/citipy/), the [OpenWeatherMap API](https://openweathermap.org/api), and the problem-solving skills to create a representative model of weather across cities.

The code required to generate random geographic coordinates and the nearest city to each latitude and longitude combination is provided.

#### <ins>Create Plots to Showcase the Relationship Between Weather Variables and Latitude</ins>
To fulfill the first requirement, use the OpenWeatherMap API to retrieve weather data from the cities list generated in the starter code. Create a series of scatter plots to showcase the following relationships:

- Latitude vs. Temperature</br>
- Latitude vs. Humidity</br>
- Latitude vs. Cloudiness</br>
- Latitude vs. Wind Speed</br>

#### <ins>Compute Linear Regression for Each Relationship</ins>
Compute the linear regression for each relationship. Separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude).

Create a series of scatter plots. Be sure to include the linear regression line, the model's formula, and the r^2 values as you can see in the following image

![image](https://github.com/user-attachments/assets/b3b765c7-8893-4baa-90d6-a108b373eefa)

Create the following plots:

- Northern Hemisphere: Temperature vs. Latitude</br>
- Southern Hemisphere: Temperature vs. Latitude</br>
- Northern Hemisphere: Humidity vs. Latitude</br>
- Southern Hemisphere: Humidity vs. Latitude</br>
- Northern Hemisphere: Cloudiness vs. Latitude</br>
- Southern Hemisphere: Cloudiness vs. Latitude</br>
- Northern Hemisphere: Wind Speed vs. Latitude</br>
- Southern Hemisphere: Wind Speed vs. Latitude</br>

After each pair of plots, explain what the linear regression is modeling. Describe any relationships that you notice and any other findings uncovered.

## <ins>VacationPy</ins>
Use the weather data skills to plan future vacations. Use Jupyter notebooks, the geoViews Python library, and the Geoapify API.</br>
The code needed to import the required libraries and load the CSV file with the weather and coordinates data for each city created in the first part.</br>
Use the Geoapify API and the geoViews Python library and employ your Python skills to create map visualizations.</br>

Complete the following steps:

- Create a map that displays a point for every city in the city_data_df DataFrame as shown in the following image. The size of the point should be the humidity in each city.

![image](https://github.com/user-attachments/assets/cf04deff-4878-4400-be00-4f50f3ba375c)

- Narrow down the city_data_df DataFrame to find your ideal weather condition. For example:

  - A max temperature lower than 27 degrees but higher than 21

  - Wind speed less than 4.5 m/s

  - Zero cloudiness

- Create a new DataFrame called ```hotel_df``` to store the city, country, coordinates, and humidity.

- For each city, use the Geoapify API to find the first hotel located within 10,000 meters of your coordinates.

- Add the hotel name and the country as additional information in the hover message for each city on the map as in the following image:

![image](https://github.com/user-attachments/assets/d621eddb-6204-4823-8356-2fbc2959defe)

### <ins>Considerations</ins>
- The city data that gets generated is based on random coordinates and different query times, so the outputs will not be an exact match to the provided starter notebook.</br>
- A refresher on the [geographic coordinate system](https://desktop.arcgis.com/en/arcmap/10.3/guide-books/map-projections/about-geographic-coordinate-systems.htm) for information.</br>
- Try to answer basic questions about the API: Where do you request the API key? Which Weather API in particular will you need? What URL endpoints does it expect? What JSON structure does it respond with? Before you write a line of code, you should have a crystal-clear understanding of your intended outcome.</br>
- Learn how it works by using the [citipy Python library](https://pypi.org/project/citipy/). Before trying to incorporate the library in the analysis, start with simple test cases outside of the main script to confirm that it is being used correctly. Often, when introduced to a new library, learners spend hours trying to figure out errors in their code when a simple test case can save a lot of time and frustration.</br>
- Apply critical thinking skills to understand how and why we're recommending these tools. What is citipy used for? Why would you use it in conjunction with the OpenWeatherMap API? How would you do so?</br>
- While building the script, pay attention to the cities being used in your query pool. Are you covering the full range of latitudes and longitudes? Or are you choosing 500 cities from one region of the world? Even if you were a geography genius, simply listing 500 cities based on your personal selection would create a biased dataset. Try to think of ways that you can counter these selection issues.</br>
  - Hint: Consider the full range of latitudes.</br>
- Once the linear regression for one relationship, follow a similar process for all other charts. Optionally, try to create a function that will create these charts based on different parameters.</br>
   (Note: there will be no extra points for completing this.)</br>
- Remember that each coordinate will trigger a separate call to the Google API. If you're creating your own criteria to plan your vacation, try to reduce the results in your DataFrame to 10 or fewer cities.</br>
- Ensure that your repository has regular commits and a thorough README.md file.</br>
