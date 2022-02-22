# GDP Analysis Data Science project
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

<img src="images/GDP3.PNG"/>

### Countries with low Birthrate and low GDP per capita
A few highlights, similar to phones, are connected with the average GDP all the more straightly, while others are not. For instance, High birthrate generally low GDP per capita, however normal GDP in low birthrate countries can change a lot.<br>
Let’s look at the countries with low birthrate (< 10%) and low GDP per capita (< 10000$). They also have high literacy, like other high average GDP countries. But we hope their other features can help distinguish them from those with low birthrate but high average GDPs, like service, are not quite an important portion in their economy, not a lot phone procession, some have negative net migration. We can see 5 countries (Bosnia & Herzegovina, Bulgaria, Russia, Serbia and Ukraine) here low birthrate and also low GDP per capita from eastern Europe or C.W. of IND. STATES, so the ‘region’ feature may also be useful.

<img src="images/GDP4.PNG"/>

## Training and Testing
First label encoding the categorical features ‘Region’ and ‘Climate’, and we are just use all features given in the data set without further feature engineering.

<img src="images/GDP5.PNG"/>

We are using the linear regression model here. As for metric, we are check both root mean squared error and mean squared log error.

<img src="images/GDP6.PNG"/>

As we know, the target isn't linear and has a lot of features, it's worth experimenting with nonlinear models like the random forest model.

<img src="images/GDP7.PNG"/>

## Visualization of Results

To see how the model is doing. is it far from here, we can make scatter plot of prediction against ground truth. The model gives a reasonable prediction, as the data points are gathering around the line y=x.

<img src="images/GDP8.PNG"/>

## Total GDP
### Top Countries

It is additionally fascinating to check out the all-out GDPs, which I take as 'Gross domestic product ($ per capita)' × 'Populace'. Here are the top 10 countries with highest total GDPs, their GDP make up to about 2/3 of the global GDP. So these top 10 countries are playing a very important role in the world's GDP.

<img src="images/GDP9.PNG"/>

Here we compare the above ten countries’ rank in total GDP and GDP per capita.

<img src="images/GDP10.PNG"/>

### Factors affecting Total GDP

Here we can also check the correlation between total GDP and the other columns. The top two factors are population and area, following many factors that have also been found mostly correlated to GDP per capita.

<img src="images/GDP11.PNG"/>

### Comparison of the Top 10 countries

Finally, let us do a comparison of the economic structure for the ten countries with the highest total GDP. Here we are comparing three major sectors like the primary sector (Agricultural), the secondary sector (Industry), and the tertiary sector (services) all contribute to GDP by producing goods and services (Services).

<img src="images/GDP12.PNG"/>

As well as their land usage

<img src="images/GDP13.PNG"/>

