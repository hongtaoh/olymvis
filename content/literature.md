---
title: Literature Review
author: Chris Fang & Hongtao Hao
---
## Female Participation in Summer Olympics

Many attempts have already been made to visualize female participation in the Olympics. The most basic one (Bmallion, 2015) is using tables to display the information about countries with the highest and lowest percentages of female athletes, and to show female percentage across the 120 years of the Olympics. See Table 1. 

<div class="wide">
	<div class="left">
		{{<figure src="/pics/1-1.png" caption="Table 1(a): Countries with the highest rate of female participation">}}
	</div>
	<div class="right">
		{{<figure src="/pics/1-2.png" caption="Table 1(b): Female percentage in Olympic events">}}
	</div>
</div>

This method is simple and informative. This is useful for researchers looking for information on this topic, but it is not effective in terms of visualization. For example, looking at the plain number won’t help viewers have a clear idea of the trend in female participation in the past 120 years. 

Another simple but effective method is using line graph displaying the number of female and male athletes in each Olympic Games from 1896 to 2016 (Nunes, 2019). See Figure 1. 

{{<figure src="/pics/1-3.png" caption="Figure. 1: Evolution of the number of Olympic athletes, male and female (1986-2016), Nunes (2019)">}}

This graph is successful in showing the growth in the number of female athletes. However, it fails to show the percentage change. Although viewers can see directly the increase in the total number, they might find it difficult to notice the changes in the percentage. 

Washington Street Journal did an interactive visualizations comparing the inclusion of female and male events in the Olympics history (Serkez, 2018). It clearly shows that most men’s events were already established before the 1960s, whereas most women’s events were only introduced after the 1980s. See Figure 2. 

{{<figure src="/pics/1-4.png" caption="Figure. 2: Interactive plot by Washington Post showing inclusion of male and female Olympic events" class="wide">}}

Each individual dot represents a sport of a gender. When clicked, there will be a line connecting to the same sport of a different gender, and information on the inclusion of this sport for both genders will appear. Overall, this visualization clearly shows how late were the introduction of female events in the Olympics history, but it did not show how the number and percentage of female athletes changed over the years. 

The official website of the International Olympic Committee (IOC) also made an attempt to show the growth in the percentage of sportswomen in the Olympics. See Figure 3.

{{<figure src="/pics/1-5.png" caption="Figure. 3: IOC graph visualizing female athletes' participation">}}

As can be seen, it is effective in the way that it shows the dramatic changes in female participation by showing four Olympics in each of the chart. However, its drawback is obvious: the number of Olympic Games that are able to be displayed is extremely limited. It is impossible to show the information of all the Olympics in the past 120 years using this method. 

Although there were many attempts visualizing the evolution of female participation in general, few visualizations exist showing the percentage change by continent. The only piece we found is several tables showing men and women participation in the Olympics from 1996 to 2016. No visualizations on this information were made. We decided that there is a gap in here. Although both the total number and relative percentage of female athletes have been growing (Nunes, 2019), the increase might be different between continents. We decided to take a closer look at this in our study. 

## Home-field Advantage

Similar to the attempt at showing female participation, simple and basic tables were utilized to examine the existence of home-field advantage at the Olympics (Pettigrew & Reiche, 2016). See Figure 4.

<figure style="position: relative">
	<img src="/pics/2-1.png" style="display: block;
margin: 0 auto;"></img>
    <div class="caption">
	Figure 4: Medals won by host countries at host year and the previous Olympics, Pettigrew & Reiche (2016)
    </div>
</figure>

This visualization shows a table comparing the total number of medals earned at the host year and the previous Olympics. Changes between the two were shown in the last column.  Among the 16 host countries from 1952 to 2012, only two countries showed negative changes, meaning that hosting the Olympics helped the country earn more medals. However, the problem with this method is that it is a little bit arbitrary to compare the host year and the adjacently previous Olympics. Changes might have been positive simply because these countries did not perform well only in the previous Games, even though they had performed well eight or more years before the host year. Therefore, it is a more robust choice to showing these countries’ Olympic performances in all years. 

Clarke (2000) did this by calculating the “Home: Away Ratio”. See Table 2.

<figure style="position: relative">
	<img src="/pics/2-3.png" style="display: block;
margin: 0 auto;"></img>
    <div class="caption">
	Table 2: Percentage of available medals won by host countries at home and away, Clarke (2016)
    </div>
</figure>


He listed the percentage of all available medals won by countries that have ever hosted a Olympic both at the Home years and the Away years. The ratio of “Home: Away” was calculated. Obviously, a ratio larger than 1 indicates the existence of home-field advantage at the Olympics. The drawback of this method is that it only shows the summary of all the years, lacking information about these countries’ performance in each year. 

Visualizations showing all the years do exist (Grange, 2016). See Figure 5.

{{<figure src="/pics/2-2.png" caption="Figure 5: Visualizing home-field advantage by Grange (2006)" class="wide">}}

For example, in this small multiple made by R, each graph has a blue vertical line emphasizing the number of medals earned during the host year, and a red horizontal line indicating the total average. It is very effective in the sense that it clearly compares the performance during the host year and all other years. The problem with this method is that lines are not very good at showing density distribution of medal numbers over the years. To improve this drawback, we decided to use kernel density estimation (KDE) coupled with small multiples. 

## Medal Efficiency

The most straightforward way of measuring a country’s efficiency of earning medals is to count the number of medals per athlete participating. This method was used by Pettigrew and Reiche (2016) in their analysis of home-field advantage. 

Some scholars argued that when assessing the efficiency of medal production, we need to take into account the resources that countries possess, such as GDP and population. From an economics perspective, Rathke and Woitek (2007) came up with a sophisticated formula calculating this efficiency, and visualized the results using multiple box plots that were stacked horizontally. See Figure 6.

{{<figure src="/pics/3-2.png" caption="Figure 6: The production of Olympic Medals, 1952-2000, Rathke & Wotiek (2007)">}}

Visualizations by Eirk (2016) for the \textit{Telegraph}, and those by medalspercapita.com also highlighted the importance of  GDP and the size of population. For example, Eirk (2016) ranked Olympic nations based on “Gold per million people” and “Gold per £100 bn GDP”. See Figure 7 and 8. 

<div class="fullwidth">
	<div class="left">
		{{<figure src="/pics/3-3.png" caption="Figure 7: Top 10 countries for medals per million population, Eirk (2006)">}}
	</div>
	<div class="right">
		{{<figure src="/pics/3-4.png" caption="Figure 8: Ranking medal production considering population and GDP, Eirk (2006)">}}
	</div>
</div>

Similarly, using the concept of “medals per capita”, medalspercapita.com ranked countries based on “population per medal”, i.e., how many people are needed to generate a medal. They created a choropleth map based the results where darker colors indicate lower “medals per capita”. See Table 3 and Figure 9. 

<div class="wide">
	<div class="left">
		{{<figure src="/pics/3-5.png" caption="Table 3: Population per medal">}}
	</div>
	<div class="right">
		{{<figure src="/pics/3-6.png" caption="Figure 9: World map of population per medal">}}
	</div>
</div>

However, we think it is problematic to divide medal counts by population or GDP in measuring medal efficiency. First of all, this method is unfair for countries who joined the Olympics late. For example, China (PRC) attended the Olympics for the first time in 1952 and due to political issues, it was not a participant till 1984 (COC, 2004). If total number of medals is the basis for medal efficiency, it would be unfair for countries like China and many newly founded countries in Africa. 

Second, it might be unfair to divide the number of medals by population. This formula assumes that a country can send as many athletes as it wants, but this is not the case. For example, for Tokyo 2020, each country can send at most three male and three female athletes (International Table Tennis Federation, 2018). As a result, China will send six table tennis athletes, as will Australia, Japan, Brazil, Egypt, Germany, and the United States (Wikipedia, n.d.), even though China’s population size is larger than that of all the six countries combined (World Bank, 2018).

Third, it might be simplistic to only count the total number of medals. There has been a debate on whether ranking of Olympic countries should be based on the number of total medals or only golds (Johnson, 2008). We decided to adopt the method by New York Times, i.e., “medal points” (Klein, 2008). In this system, a gold medal is given 4 points, silver 2 and bronze 1. Center for Strategic International Studies (n.d.) used this method and ranked countries based on what they called as “weighted medals”. 

In this interactive, viewers can see a country’s ranking on each categories of sport in a specific Olympic Games by clicking the country’s name. This visualization is clear and direct, but it has some drawbacks. First, only the top countries can be shown interactively but there are over 200 participating countries and regions. Second, and because of the first drawback, this visualization did not provide viewers a general idea of the distribution of media efficiency across countries. See Figure 10.

{{<figure src="/pics/3-7.png" class="wide" caption="Figure 10: Ranking of countries by weighted medals">}}

To solve these problems, we decided to rank countries by “medal points” as well, but on an interactive choropleth world map. 

## Ranking Sports by Number of Athletes

Dutta (2018) in his Kaggle post visualized the top 10 sports that USA excel by putting 10 boxes vertically with sporting winning the most gold medals on top. See Figure 11.

{{<figure src="/pics/4-1.png" caption="Figure 11: Ranking of sports by weighted medals">}}

This visualization is transparent and clear but the problem is that it is limited to only about 10 items, which is not enough for us to visualize all the sports in the Summer Olympics. Instead, we decided to try bar chart and word cloud for our visualizations. 

