# Data624_HW2
Time series decomposition

https://otexts.com/fpp3/decomposition-exercises.html


3.7 Exercises
Consider the GDP information in global_economy. Plot the GDP per capita for each country over time. Which country has the highest GDP per capita? How has this changed over time?

For each of the following series, make a graph of the data. If transforming seems appropriate, do so and describe the effect.

United States GDP from global_economy.
Slaughter of Victorian “Bulls, bullocks and steers” in aus_livestock.
Victorian Electricity Demand from vic_elec.
Gas production from aus_production.
Why is a Box-Cox transformation unhelpful for the canadian_gas data?

What Box-Cox transformation would you select for your retail data (from Exercise 8 in Section 2.10)?

For the following series, find an appropriate Box-Cox transformation in order to stabilise the variance. Tobacco from aus_production, Economy class passengers between Melbourne and Sydney from ansett, and Pedestrian counts at Southern Cross Station from pedestrian.

Show that a  
3
×
5
  MA is equivalent to a 7-term weighted moving average with weights of 0.067, 0.133, 0.200, 0.200, 0.200, 0.133, and 0.067.

Consider the last five years of the Gas data from aus_production.

gas <- tail(aus_production, 5*4) %>% select(Gas)
Plot the time series. Can you identify seasonal fluctuations and/or a trend-cycle?
Use classical_decomposition with type=multiplicative to calculate the trend-cycle and seasonal indices.
Do the results support the graphical interpretation from part a?
Compute and plot the seasonally adjusted data.
Change one observation to be an outlier (e.g., add 300 to one observation), and recompute the seasonally adjusted data. What is the effect of the outlier?
Does it make any difference if the outlier is near the end rather than in the middle of the time series?
Recall your retail time series data (from Exercise 8 in Section 2.10). Decompose the series using X-11. Does it reveal any outliers, or unusual features that you had not noticed previously?

Figures 3.19 and 3.20 show the result of decomposing the number of persons in the civilian labour force in Australia each month from February 1978 to August 1995.

Decomposition of the number of persons in the civilian labour force in Australia each month from February 1978 to August 1995.
Figure 3.19: Decomposition of the number of persons in the civilian labour force in Australia each month from February 1978 to August 1995.

Seasonal component from the decomposition shown in the previous figure.
Figure 3.20: Seasonal component from the decomposition shown in the previous figure.

Write about 3–5 sentences describing the results of the decomposition. Pay particular attention to the scales of the graphs in making your interpretation.
Is the recession of 1991/1992 visible in the estimated components?
This exercise uses the canadian_gas data (monthly Canadian gas production in billions of cubic metres, January 1960 – February 2005).

Plot the data using autoplot(), gg_subseries() and gg_season() to look at the effect of the changing seasonality over time.1
Do an STL decomposition of the data. You will need to choose a seasonal window to allow for the changing shape of the seasonal component.
How does the seasonal shape change over time? [Hint: Try plotting the seasonal component using gg_season().]
Can you produce a plausible seasonally adjusted series?
Compare the results with those obtained using SEATS and X-11. How are they different?
