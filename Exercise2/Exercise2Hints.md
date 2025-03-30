# Weather Station Challenge - Hints 🌦️

This guide provides hints for each task in the Weather Station Challenge.

## Task 1: Weather Station Setup and Data Collection
- Use `torch.randint()` to generate random temperature values for daily temperatures between -10°C and 40°C.
- Create a tensor for station identifiers using `torch.tensor()`, representing different weather stations (e.g., `["Station A", "Station B", "Station C", "Station D", "Station E"]`).
- Generate random temperature readings for 5 weather stations over a span of 10 days and store these readings in a 2D tensor where rows represent days and columns represent stations.
- Use `.mean(dim=0)`, `.max(dim=0)`, and `.min(dim=0)` to calculate the mean, maximum, and minimum temperature for each station over the 10 days.

## Task 2: Temperature Conversion and Variability Analysis
- Convert the temperature values from Celsius to Fahrenheit using the formula **(F = C * 9 / 5 + 32)**.
- Calculate the daily temperature range (max - min) for the month using `.max()` and `.min()`.
- Compute the average temperature across all days using `.mean()`.
- Analyze the temperature variability across the different stations by calculating the standard deviation of temperatures using `.std(dim=0)`.
- Identify which station had the highest variability in temperatures using `.argmax()`.

## Task 3: Heat Warning System and Rainfall Analysis
- Implement a heat warning system by creating a boolean mask tensor that identifies readings above 30°C using comparison operators.
- Use boolean indexing to extract the days and stations that triggered these heat warnings and print the results.
- Create a tensor representing daily rainfall amounts for 5 stations over a month using `torch.randint()`.
- Create a calibration tensor with adjustment factors for each station and apply these calibration factors to your rainfall readings using element-wise multiplication.

## Task 4: Final Challenge - Weather Dashboard
- For the final challenge, create a comprehensive weather dashboard using tensors for temperature, humidity, and rainfall.
- Develop a combined "weather quality index" using a weighted formula (e.g., **(WQI = 0.5 * Temperature + 0.3 * Humidity - 0.2 * Rainfall)**).
- Explore the relationship between elevation (a new tensor) and temperature to see how altitude affects weather conditions.
- Calculate regional statistics by grouping stations and identifying the "ideal weather" locations based on your criteria.
- Finally, demonstrate at least five different tensor operations in your analysis and create a simple visualization of your weather data using a library like Matplotlib or Seaborn.

---