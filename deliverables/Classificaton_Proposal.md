# Classificaton Proposal

<hr>
Michael Harnett<br>
6/3/21


### Goal: Predicting taxi rides that result in a tip<hr>
As of 2019, there are over 300 thousand active professional driving licenses in New York City. With the introduction of new passenger services over the past couple of years, the market has never been more competitive. Drivers need to consider multiple factors when choosing where to pick up passengers in attempting to maximize their profits. For this particular classification project, I intend to use data available on NYC.gov to classify if a ride will result in a tip or not. 
<br><br><br>
### Data<hr>
NYC.gov, more speficially<br> https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page <br>
has a detailed list of every ride recorded in New York. The data is aggregated by month, stretching back as far as 2009. There are separate files for yellow cabs, green cabs, and FHV's (for hire vehicles) that records other services like Uber, Lyft, and Juno.<br><br>
An initial pull request to their API retrived just 1000 observations. A direct download of only green cab's information for one year yeilded over 16 million observations. More EDA will determine if I look at just one type of vehicle's data over a year, or multiple car types over a shorter time period.<br><br>
Initial features include:<ul>
<li> Pickup location (in longitude and latitude)</li>
<li> Dropoff location (in longitude and latitude)</li>
<li>Number of passengers</li>
<li>Date and time of ride (start and end)</li>
<li>Distance of trip</li>
<li>Fare amount</li>
<li>Taxes applied</li>
<li>Extra charges applied</li>
<li>Payment type (card or cash)
<li>Toll charges</li></ul>
<br><br><br>
### Tools<hr>
Most work for this project will be done in Pandas:
<ul><li>Data will be pulled from the source API</li>
<li>EDA and Feature Engineering will then be done</li>
<li>Different SKLearn classification models will be tested to arrive at most effective, balanced between predictive power and interpretability</li></ul>
<br>
Visualizations will be performed in both Python using Seaborn, and in Tableau (to highlight different boroughs using Tableau's handy longitude and latitude functionality)<br><br><br>
### MVP Goal<hr>
By the MVP, I would like to have a final, cleaned version of selected data, with different baseline classification model metrics. After choosing the model that best addresses my problem, I will move forward with feature engineering. Future work could include repeating the above process but with different subsets of data, helping drivers to choose their most effective driving dates, times, and locations.