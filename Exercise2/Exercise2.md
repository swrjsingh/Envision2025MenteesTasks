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

### Task 1: Weather Station Setup and Data Collection
- Create tensors to store daily temperatures for a month (30 days) using random values between -10°C and 40°C. 🌡️
- Create a tensor for station identifiers, such as `["Station A", "Station B", "Station C", "Station D", "Station E"]`, to represent different weather stations. 🏢
- Generate random temperature readings for 5 weather stations over a span of 10 days and store these readings in a 2D tensor where rows represent days and columns represent stations. 
- Calculate the mean, maximum, and minimum temperature for each station over the 10 days, and print the results in a clear format.

### Task 2: Temperature Conversion and Variability Analysis
- Convert the temperature values from Celsius to Fahrenheit using the formula **( F = C * 9 * 5 + 32 ).** 🔄
- Calculate the daily temperature range (max - min) for the month and the average temperature across all days. 📊
- Analyze the temperature variability across the different stations by calculating the standard deviation of temperatures for each station. 📈
- Identify which station had the highest variability in temperatures and determine which day was the hottest across all stations.

### Task 3: Heat Warning System and Rainfall Analysis
- Implement a heat warning system by creating a mask tensor that identifies readings above 30°C, which you will consider as heat warnings. ⚠️
- Use boolean indexing to extract the days and stations that triggered these heat warnings and print the results.
- Create a tensor representing daily rainfall amounts for 5 stations over a month using `torch.randint()`. 🌧️
- Create a calibration tensor with adjustment factors for each station and apply these calibration factors to your rainfall readings to calculate the adjusted rainfall amounts.

### Task 4: Final Challenge - Weather Dashboard
- For the final challenge, create a comprehensive weather dashboard using tensors for temperature, humidity, and rainfall. 📊
- Develop a combined "weather quality index" using a weighted formula (e.g., **( WQI = 0.5 * Temperature + 0.3 * Humidity - 0.2 * Rainfall )**).
- Explore the relationship between elevation (a new tensor) and temperature to see how altitude affects weather conditions.
- Calculate regional statistics by grouping stations and identifying the "ideal weather" locations based on your criteria. 🌈
- Finally, demonstrate at least five different tensor operations in your analysis and create a simple visualization of your weather data using a library like Matplotlib or Seaborn. 📈

---

Good luck, and have a blast playing with tensors! 🌟