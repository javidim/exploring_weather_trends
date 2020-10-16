# Exploring weather trends

The main goal of the project was to create a visualization and prepare a write up describing the similarities and differences between global temperature trends and temperature trends of Baku city. 
Simple SQL quaries were used in order to extract three tables from the database. 
Considering the large number of cities in data and the fact that the names of the countries were not crucial for the purposes of the research it was decided to expose the data in  in the form of panel data using Pandas Pivot Table. 
Then two datasets - the one with global average temperatures and the other with the temperatures of the cities were merged in order to simplify the process of further comparisons. 
It was clearly seen that most of the missing data in the columns occured in the earlier periods and that was quite logical taking into account lack of statistics in previous centuries. Therefore all the data (mostly missing) before the year 1808 was dropped. 
After data cleaning was finished some visualizations were perfromed in order to look at the data before starting manipulations. 
Pandas provides multiple built-in methods to calculate moving averages. It was decided to use the Exponential Moving average method in this research. It is a widely used method to filter out noise and identify trends. The weight of each element decreases progressively over time, meaning the exponential moving average gives greater weight to recent data points. This is done under the idea that recent data is more relevant than old data. Compared to the simple moving average, the exponential moving average reacts faster to changes, since is more sensitive to recent movements.
The exponential moving averages of the air temperature were computed for the Baku city and for global temperatures with a smoothing factor of 0.1 and 0.3.
A small weighting factor α results in a high degree of smoothing, while a larger value provides a quicker response to recent changes. Average air temperature in Baku was compared to the average global temperature with weighting factor 0.1. 

# Conclusions:
Baku is hotter on average compared to the global average and the difference has been consistent over time;
Changes in Baku's temperatures over time has been in line with the changes in the global average;
Trend clearly shows the world is getting hotter and the trend has been consistent over the last few hundred years.
