# GDP Analysis Data Science project

## Overview and Motivation
Economic growth increases state capacity and the supply of public goods. Every country wants to increase their GDP If GDP is rising, the economy is in solid shape, and the nation is moving forward. Last few years, we have seen China’s GDP growth was really amazing compare another country China can be role model for other country. 

## Related work
Yes of course we have taken idea from your lecture and through internet also we have visited some website like Kaggle and so on.

## Objective
The primary goal of this project is to investigate the dataset "Countries of the World" and to focus on the elements that are influencing a Country's GDP per capita.

## Research questions
1. What are the factors affect the growth of GDP of a country?
2. What are the other factors other than the major factor which effect a country’s GDP?
3. What are the Co-relation between the dataset elements?
4. Is the low-birth rate Country effect the GDP of a country?
5. Which Countries of the World have the highest GDP and Why?

After the analysis of the project we have ended up for the above five questions. As the project is about the GDP of the countries so at first, we have to find the major factor which directly affect the growth of GDP of a country.
After that we have to find the others factors other than the major factors which effect the growth of GDP. Also, we have to find the Co-relation between the dataset elements of GDP factors.
During the Analysis, we have found a fact that a country which have low birth rate will have a higher GDP which is very interesting.
As the project progress and the questions evolve then we have to find the top countries which have high GDP.

## Dataset
For this Project, we first collected the data of the world country GDP by surfing the internet and download the worldGDPperCapital.csv file.
In the dataset, there are information about the ten factors which are needed to calculate GDP of a Country.


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

