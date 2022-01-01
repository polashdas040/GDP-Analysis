# Analysis
## Data Preparation – fill in missing values
We observed that the table is missing certain information. We'll fill in the missing data with the median of the region that a country belongs to because countries that are geologically adjacent are often similar in many aspects. Let's look at the region medians for 'GDP ($ per capita),' 'Literacy (percent),' Agriculture, Industry, and Service,' for example. Note that we use the mode instead of the median for 'climate' because it appears that 'climate' is a categorical feature here.

<img src="images/GDP1.PNG"/>

## Data Exploration & Visualisation
### Correlation between Variables
Here we need to show the correlation between all numerical columns. So, here we using Seaborn and Seaborn is a data visualization library that is built on top of matplotlib and contains a direct function to create heatmaps. The heatmap shows the correlation between all numerical columns.

<img src="images/GDP2.PNG"/>

### Top Countries with the highest GDP per capita.
In this bar chart top 20 countries with the highest GDP per capita. Luxembourg's GDP per capita is around $55000. Luxembourg is higher than the next 19 conuntries, the next 19 countries are close. Germany, the 20th has about 2.5 times GDP per capita of the world average.
