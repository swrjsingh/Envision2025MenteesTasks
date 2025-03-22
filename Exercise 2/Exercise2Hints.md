# Weather Station Challenge - Hints 🌦️

This guide provides hints for each task in the Weather Station Challenge.

## Task 1: Weather Station Setup
- Use `torch.randint()` to generate random temperature values.
- Create tensors for station identifiers using `torch.tensor()`.
- Generate random humidity readings with `torch.randint()`.
- Explore tensor properties using `.shape`, `.dtype`, and `.device`.

## Task 2: Temperature Conversion
- Convert Celsius to Fahrenheit using the formula **(F = C * 9 / 5 + 32)**.
- Use tensor operations to calculate the maximum and minimum values with `.max()` and `.min()`.
- Calculate the average temperature using `.mean()`.

## Task 3: Multi-Station Data Collection
- Generate a 2D tensor for temperature readings using `torch.randint()`.
- Use `.mean(dim=0)`, `.max(dim=0)`, and `.min(dim=0)` to analyze the data across stations.
- Print results using `print()` for clear output.

## Task 4: Variability Analysis
- Calculate the standard deviation of temperatures using `.std(dim=0)`.
- Use `.argmax()` to find the station with the highest variability.
- Identify the hottest day using `.max(dim=1)`.

## Task 5: Heat Warning Mask
- Create a boolean mask for temperatures above 30°C using comparison operators.
- Use boolean indexing to extract relevant data from the tensor.

## Task 6: Weather Data Manipulation
- Create a 2D tensor for temperature readings using `torch.randint()`.
- Reshape tensors with `.view()` to analyze data from different perspectives.
- Extract specific days using slicing techniques.

## Task 7: Weekend Data Extraction
- Calculate average temperatures for the weekend using `.mean(dim=0)`.
- Stack data from different regions using `torch.stack()` for comparative analysis.

## Task 8: Rainfall Analysis
- Generate a tensor for daily rainfall amounts using `torch.randint()`.
- Create a calibration tensor and apply it using element-wise multiplication.
- Use tensor operations to adjust rainfall readings.

## Task 9: Rainfall Statistics
- Calculate total, mean, and standard deviation of rainfall using `.sum(dim=0)`, `.mean(dim=0)`, and `.std(dim=0)`.
- Create a binary tensor for rainy days using comparison operators.

## Task 10: Final Challenge
- Develop a weather quality index using a weighted formula with tensor operations.
- Explore relationships between tensors using element-wise operations.
- Group and analyze data based on your criteria to identify ideal weather locations.

---