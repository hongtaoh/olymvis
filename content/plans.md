---
title: Plans for Visualization
author: Chris Fang & Hongtao Hao
---
## Plans: Female Participation
As discussed above, we will use line graph, stacked bar chart, and area chart to show the overall trend of female participation in the Summer Olympics. For female participation in each individual continent, we will use KDE in a small multiple. 

In line graph, the x-axis will be time and the y-axis the percentage against the total number of participants. We will show both female and male athletes. See Figure 12.

For stacked bar chart, the x-axis will be time and y-axis will percentage against the total number of athletes. Two segments in each bar will represent male and female respectively, and the two will sum up to 100\% for every year presented. This will make the comparison between male and female participation very clear. See Figure 13.

<div class="wide">

<div class="left">

{{<figure src="/pics/1.png" caption="Figure 12: Line graph for female participation">}}

</div>
<div class="right">

{{<figure src="/pics/2.png" caption="Figure 13: Stacked bar chart for female participation">}}
</div>

</div>

In order to also show the changes in the total number of athletes, beside the changes in percentages, we will use a stacked area chart. The x-axis will be again time, and the y-axis will be the total number of athletes for each Olympic Games. See Figure 14.

For female participation in each individual continent over the years, we will line graphs in a small multiple. The x-axis will be time and the y-axis will be the percentage of female athletes against the total number of athletes. To make comparisons between continents and with the global average clearer, for each plot in the small multiple, we will put the line graph of other continents in the background, and we will also plot the global average as the benchmark. See Figure 15.

<div class="wide">

<div class="left">

{{<figure src="/pics/3.png" caption="Figure 14: Staked area chart for female participation">}}

</div>
<div class="right">

{{<figure src="/pics/4.png" caption="Figure 15: Line graph in small multiple for female participation">}}
</div>

</div>

## Plans: Home-field Advantage
To examine whether there exists a home-field advantage at the Olympics, we will first use a scatter plot with jitter. The x-axis will be countries that have ever been a host, and the y-axis will be the percentage against the total number of medals a country earned. Each dot represents an Olympic Games the country has participated. Black dots denote data for a “non-host” year and orange dots denote data for host year. See Figure 16.

To better show the density distribution of medal gains, we will employ kernel density estimation in a small multiple. The x-axis will be the percentage against the total number of medals at a Games and the y-axis will be density. We will use an arrow to denote the density of a year when the country was a host. See Figure 17.

Arrows located at points with high densities, would be signs of the existence of home-field advantage at the Olympics. 

<div class="wide">

<div class="left">

{{<figure src="/pics/5.png" caption="Figure 16: Scatter plot with jittering for home-field advantage">}}

</div>
<div class="right">

{{<figure src="/pics/6.png" caption="Figure 17: KDE for home-field advantage">}}
</div>

</div>

## Plans: Medal Efficiency

The index of “medal efficiency” will be calculated as medal points per athlete participating. We will use an interactive choropleth world map to show each participating country and region’s score. See Figure 18.

{{<figure src="/pics/9.png" caption="Figure 18: Choropleth map for medal efficiency">}}

## Plans: Ranking Sports by Number of Athletes
First, we will use a bar chart where the x-axis will be the different sports and the y-axis the corresponding number of athletes. See Figure 19. 

Second, we will show this ranking using a word cloud in which larger font size denotes higher number of participants. This graph will be clearer and more direct because viewers can intuitively get a sense of the relative size of participation of a sport. See Figure 20.

<div class="wide">

<div class="left">

{{<figure src="/pics/7.png" caption="Figure 19: Bar chart for sports ranking">}}

</div>
<div class="right">

{{<figure src="/pics/8.png" caption="Figure 20: Word cloud for sports ranking">}}
</div>

</div>


