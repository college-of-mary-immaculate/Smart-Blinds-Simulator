Input and Output

Inputs:
1.Ambient Light: This is derived from the cloud cover percentage fetched from a weather API. It’s calculated as 100 - cloudCover.
2.Temperature: This is directly fetched from the weather API data.

Outputs:
1.Blinds Position: A percentage (0 to 100) that determines how much the blinds should be open.
2.Classification: A string that classifies the ambient light level into categories such as "Very High Light," "Low Light," "Mid Light," and "High Light."

Problem Statement:
The goal is to automatically adjust window blinds based on environmental conditions, specifically ambient light and temperature. This aims to enhance comfort and energy efficiency in a space by optimizing natural light and thermal comfort.
Linguistic Variables

Ambient Light:
-Low: Represented by the fuzzy set (0 to 30).
-Mid: Represented by the fuzzy set (40 to 60).
-High: Represented by the fuzzy set (60 to 80).

Temperature:
-Low: Represented by the fuzzy set (0 to 30).
-Mid: Represented by the fuzzy set (35 and above).
-High: Represented by the fuzzy set (25 to 35).

Rules:
Rule 1: If ambient light is low and temperature is low, then the blinds position is high (95%).
Rule 2: If ambient light is mid and temperature is mid, then the blinds position is medium (55%).
Rule 3: If ambient light is high and temperature is high, then the blinds position is low (5%).

Defuzzification:
-You calculate the total weight from the activated rules.
-The final position is constrained between 0 and 100.

Running the Application
When you run the application:

-It fetches current weather data (temperature and cloud cover) from the weather API.
-It computes ambient light based on the cloud cover.
-It applies the fuzzy logic rules to compute the blinds position.
-It updates the blinds position visually in the UI and logs the classification.


