---
title: Home-field Advantage, Medal Efficiency, and Sports Ranking
author: Chris Fang & Hongtao Hao
---
## Home-field Advantage

As discussed above, we first tried scatter plot with jitter. The x-axis is the countries that have ever hosted the Olympics and y-axis denotes the percentage of a medals earned by a country against the total number of medals in that year. Blue dots represent data when the country were not the host and the orange ones for when it was the host. See Figure 31.

[**FIGURE 31 HERE**]

The blue dots were too packed. We later tried beeswarm plot coupled with box plot. Dots were shown much more clearly but one drawback is that we could not see the density distribution of all the dots very well. Density distribution was important in this case because it would allow an easier comparison between the medal percentage when a country was a host and that when it was not. See Figure 32. 

[**FIGURE 32 HERE**]

To show density distribution of medal percentages, we used kernel density estimation in a small multiple. The x-axis is the medal percentage and the y-axis is the probability density. We used a red arrow to denote when the country was a Olympics host. An arrow located at the tail would indicate the existence of home-field advantage. See Figure 33.

[**FIGURE 33 HERE**]

## Medal Efficiency

As planned, first of all, we did data manipulation before plotting. Golds were given four points, Silver 2, and Bronze 1. Attendance without any medals was assigned to 0 point. A country’s “medal efficiency” was calculated as the quotient of total medal points and the total number of athletes participating over 120 years. 

We then plotted a choropleth map using orthographic projection. We applied Viridis color map where darker shades denote higher medal efficiency. To ensure interactivity, we made this map with the Plotly package. See Figure 34.

[**FIGURE 34 HERE**]

We found this index of medal efficiency to be both more accurate and intuitive. The reasons why it is more accurate have been outlined above. We believe that it is also more intuitive because, for example, for countries that still exist today, the highest medal efficiency is 0.91 for the United States of America. The fact that the highest is close to one makes it easier for compare between countries. 

## Ranking Sports by Number of Athletes
To rank sports according to the number of athletes, we first plotted a bar chart, each bar representing a category. As can be seen below, since there were too many categories, the names of sports overlapped to a degree that most of them were indistinguishable. Since there are around thirty sports, using colors is not an ideal option. See Figure 35.

[**FIGURE 35 HERE**]

We then thought about word cloud. In word cloud, the size of words is associated with the frequencies. This would make our ranking clearer. We did this visualization with the wordcloud package. See Figure 36.

[**FIGURE 36 HERE**]


