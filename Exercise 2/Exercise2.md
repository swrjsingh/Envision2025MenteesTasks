# 🌦️ The Weather Station Challenge 🌦️
### IEEE Pixel Flow Exercise 2

Welcome to the **Weather Station Challenge!** In this exciting exercise, you'll dive into the world of **PyTorch** by creating your very own **Weather Station system**. Each task is designed to teach you essential PyTorch basics while having fun and building something amazing together!

---

## 🚀 General Rules
- **Branch Naming**: Create a new branch using the format: `yourname-pytorch` (e.g., `Parth-pytorch`).
- **File Naming**: Name your Jupyter Notebook file: `yourname-station.ipynb` (e.g., `Parth-station.ipynb`).
- **Need Help?** Check out the [PyTorch official documentation](https://pytorch.org/docs/stable/index.html) for guidance on basic functions. You can also watch this helpful [PyTorch video](https://youtu.be/Z_ikDlimN6A?feature=shared).
- **Comment Your Code**: Make sure to comment your code well so that everyone can understand your brilliant work!
- **Learning Tools**: Feel free to use ChatGPT, DeepSeek, and other resources, but remember to **TYPE** the code yourself—no copy-pasting!
- **Ask Questions**: Don’t hesitate to ask questions! You can either post in the group or reach out personally if you prefer.
- **Master the Basics**: Familiarize yourself with the fundamentals of tensor manipulation; it’s a crucial skill on your journey through machine learning! 🌟

---

## 🛠️ Tasks

### Task 1: Weather Station Setup
- Create tensors to store daily temperatures for a month (30 days) using random values between -10°C and 40°C. 🌡️
- Create a tensor for station identifiers, such as `["Station A", "Station B", "Station C", "Station D", "Station E"]`, to represent different weather stations. 🏢
- Create a tensor for humidity readings (percentage) for each station, using random values between 0% and 100%. 💧
- Display the shape, data type, and device of each tensor to understand their structure and how they will be used in your analysis.

### Task 2: Temperature Conversion
- Convert the temperature values from Celsius to Fahrenheit using the formula \( F = C \times \frac{9}{5} + 32 \). 🔄
- Calculate the daily temperature range (max - min) for the month and the average temperature across all days. 📊
- Print the results in a clear and readable format, showing the average and range for each day to provide insights into temperature fluctuations.

### Task 3: Multi-Station Data Collection
- Simulate data collection from multiple weather stations by generating random temperature readings for 5 weather stations over a span of 10 days. 🌤️
- Store these readings in a 2D tensor where rows represent days and columns represent stations.
- Calculate the mean, maximum, and minimum temperature for each station over the 10 days.
- Print the results in a clear format, indicating which station had the highest and lowest temperatures, allowing for easy comparison.

### Task 4: Variability Analysis
- Analyze the temperature variability across the different stations by calculating the standard deviation of temperatures for each station. 📈
- Identify which station had the highest variability in temperatures.
- Determine which day was the hottest across all stations and print the corresponding temperature and station name to highlight the extremes in your data.

### Task 5: Heat Warning Mask
- Implement a heat warning system by creating a mask tensor that identifies readings above 30°C, which you will consider as heat warnings. ⚠️
- Use boolean indexing to extract the days and stations that triggered these heat warnings.
- Print the results, clearly indicating which stations had heat warnings on which days, providing valuable information for potential alerts.

### Task 6: Weather Data Manipulation
- Create a 2D tensor representing temperature readings for 7 days across 5 stations.
- Reshape this data to view it in two different ways: station-centric (5 stations × 7 days) and day-centric (7 days × 5 stations). 📅
- Extract weekend temperature data (days 6-7) and analyze the average temperatures for those days to see if there are any trends.

### Task 7: Weekend Data Extraction
- Using the weekend data extracted in the previous task, calculate the average temperature for each station over the weekend. 🛌
- Stack data from three different regions (e.g., North, South, East) into a single tensor to facilitate regional comparisons.
- Print the stacked tensor and analyze any patterns or differences between the regions to gain insights into geographical influences on weather.

### Task 8: Rainfall Analysis
- Create a tensor representing daily rainfall amounts for 5 stations over a month. 🌧️
- Create a calibration tensor with adjustment factors for each station (e.g., `[1.0, 1.1, 0.9, 1.2, 1.0]`).
- Apply these calibration factors to your rainfall readings to calculate the adjusted rainfall amounts, which will provide a more accurate representation of precipitation levels.

### Task 9: Rainfall Statistics
- Summarize the rainfall data by calculating the total, mean, and standard deviation of rainfall at each station. 📏
- Create a binary tensor indicating rainy (1) or dry (0) days based on a threshold (e.g., 5mm).
- Print the statistics and the binary tensor, highlighting the rainy days to provide a clear overview of rainfall distribution.

### Task 10: Final Challenge - Weather Dashboard
- For the final challenge, create a comprehensive weather dashboard using tensors for temperature, humidity, and rainfall. 📊
- Develop a combined "weather quality index" using a weighted formula (e.g., **WQI = 0.5 * Temperature + 0.3 * Humidity - 0.2 * Rainfall**).
- Explore the relationship between elevation (a new tensor) and temperature to see how altitude affects weather conditions.
- Calculate regional statistics by grouping stations and identifying the "ideal weather" locations based on your criteria. 🌈
- Finally, demonstrate at least five different tensor operations in your analysis and create a simple visualization of your weather data using a library like Matplotlib or Seaborn. 📈

---

Good luck, and have a blast playing with tensors! 🌟