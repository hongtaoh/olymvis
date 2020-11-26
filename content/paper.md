---
title: Visualizing 120 years of Summer Olympics
author: Zihui Fang & Hongtao Hao
appendix:
  acknowledgments: |
    We are thankful for Professor [Yong-Yeol Ahn](http://yongyeol.com/)'s helpful guidance on this project in [*Data Visualization*](https://yyahn.com/dviz-course/) class of 2019 Fall. 

    We also thank [Yihui Xie](https://yihui.org/) 's [hugo-prose theme](https://github.com/yihui/hugo-prose), which made this profolio possible. 
features: [+toc, +number_sections, +sidenotes, -citation]
---
## Abstract
From the first modern Olympics in 1896 to Rio 2016, the Summer Olympic Games has been through 120 years. This study analyzed the [historical data](https://github.com/rgriff23/Olympic_history) about the Olympics and tried to answer four questions, i.e., 

- how female participation changed over the years and how these changes differed between continents,
- whether there is a home-field advantage at the Olympics,
- how "efficient" is each participating country and region to get medals, and 
- which sports had the highest number of participants. 

Results showed that both total number of athletes and the rate of female participation have been increasing in the past 120 years. Also, there seems to exist a home-field advantage. Third, medal efficiency is highly correlated with participating country or region's economic development. Finally, athletics, gymnastics, and swimming have the highest number of athletes.

## Motivation
The modern Olympic Games are the greatest sports mega-event in the world (Grix, 2013). It generates a massive number of  audiences worldwide. The latest Rio 2016 Olympics, for example, attracted 3.5 billion viewers (Roxbourough, 2016), half of the world population. Apart from this mobilizing power, the Olympic Games have significant political (Giulianotii, 2015; Cottrell \& Nelson, 2010; MacAloon, 1995), economic (Madden, 2002; Blake, 2005; Osada, Ojima, Kurachi, Miura, \& Kawamoto, 2016), and socio-cultural (Malfas, Theodoraki, \& Houlihan, 2004) impacts. It also contributes to global friendship and cooperation (Beutler, 2008). 

Gender equality in sports has been a hot topic (Mervosh \& Caron, 2019). Debates on this issue have revolved around equal pay and media coverage (Baker, Seymour, \& Zimbalist, 2019). There has long been a obvious gender pay gap in sports (Abrams, 2019; Farmer, 2017). For example, of the 100 athletes on the 2019 Forbes list of the world’s highest-paid athletes, only one of them is a women. i.e., Serena Williams, who is ranked 63th on the list. There has also been a lack of media coverage on women in sports. Although 40\% of all sports participants are female, only 4\% of the sports media coverage were about female athletes (MacKenzie, 2019). A study (Cooky, Messner, \& Musto, 2015) examining sports coverage from 1989 to 2014 found that despite a dramatic increase in the number of women playing sports (Good, 2015), there had been a decrease in the amount of coverage of female athletes. Under this backdrop, we aim to look at female participation across the globe in Summer Olympic Games in the past 120 years.

Recently, there has been a trend that fewer cities want to host the Olympics, challenging the future of a century-old tradition (Goldblatt, 2016). For example, 12 cities bid for 2004 Summer Olympics but only two for 2020 Winter games (Ludacer, 2018). Considering the importance of Olympic success in national pride (Mower, 2012), a home-field advantage in the Olympics might encourage countries to bid for hosting the mega-event. Therefore, it is worth investigating whether this advantage exists in the Olympics, and how significant is it. 

Although earning medals can boost national pride, countries are not “born equal” in terms of their ability to achieve Olympic success. Studies have demonstrated that population size and economic development for a large part determined a country’s Olympic performance (Soos, Martinez, \& Szabo, 2017; Xun, 2005; Bernard \& Busse, 2004). However, we think it’s unfair to compare Singapore with the United States in terms of total number of medals earned, because the two countries have totally different population size. What is more important is “medal efficiency”, i.e., medal counts per athlete participating in the Olympics. In other words, we are more concerned about how effective is a country to earn medals, rather than the total number of medals earned. We aim to look at how this “medal efficiency” differ between countries. 

Apart from its significance for societies at large, Olympics is associated with individuals’ health as well (Sandercocok, Beedie, \&  Mann, 2016). People might be inspired by the Olympics and more actively engage in physical activities. Besides its benefits for physical health (Warburton, Nicol, \& Bredin, 2006), it has psychological benefits as well (Ghildiyal, 2015). For example, playing sports can help build one’s characters. With the importance of sports in mind, we want to examine which sports in the Olympics history have the highest number of participants. 

## Literature Review

### Female Participation in Summer Olympics

Many attempts have already been made to visualize female participation in the Olympics. The most basic one (Bmallion, 2015) is using tables to display the information about countries with the highest and lowest percentages of female athletes, and to show female percentage across the 120 years of the Olympics. See Table 1. 

<div class="wide">
  <div class="left">
    {{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/1-1.png" caption="Table 1(a): Countries with the highest rate of female participation">}}
  </div>
  <div class="right">
    {{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/1-2.png" caption="Table 1(b): Female percentage in Olympic events">}}
  </div>
</div>

This method is simple and informative. This is useful for researchers looking for information on this topic, but it is not effective in terms of visualization. For example, looking at the plain number won’t help viewers have a clear idea of the trend in female participation in the past 120 years. 

Another simple but effective method is using line graph displaying the number of female and male athletes in each Olympic Games from 1896 to 2016 (Nunes, 2019). See Figure 1. 

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/1-3.png" caption="Figure. 1: Evolution of the number of Olympic athletes, male and female (1986-2016), Nunes (2019)">}}

This graph is successful in showing the growth in the number of female athletes. However, it fails to show the percentage change. Although viewers can see directly the increase in the total number, they might find it difficult to notice the changes in the percentage. 

Washington Street Journal did an interactive visualizations comparing the inclusion of female and male events in the Olympics history (Serkez, 2018). It clearly shows that most men’s events were already established before the 1960s, whereas most women’s events were only introduced after the 1980s. See Figure 2. 

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/1-4.png" caption="Figure. 2: Interactive plot by Washington Post showing inclusion of male and female Olympic events" class="wide">}}

Each individual dot represents a sport of a gender. When clicked, there will be a line connecting to the same sport of a different gender, and information on the inclusion of this sport for both genders will appear. Overall, this visualization clearly shows how late were the introduction of female events in the Olympics history, but it did not show how the number and percentage of female athletes changed over the years. 

The official website of the International Olympic Committee (IOC) also made an attempt to show the growth in the percentage of sportswomen in the Olympics. See Figure 3.

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/1-5.png" caption="Figure. 3: IOC graph visualizing female athletes' participation">}}

As can be seen, it is effective in the way that it shows the dramatic changes in female participation by showing four Olympics in each of the chart. However, its drawback is obvious: the number of Olympic Games that are able to be displayed is extremely limited. It is impossible to show the information of all the Olympics in the past 120 years using this method. 

Although there were many attempts visualizing the evolution of female participation in general, few visualizations exist showing the percentage change by continent. The only piece we found is several tables showing men and women participation in the Olympics from 1996 to 2016. No visualizations on this information were made. We decided that there is a gap in here. Although both the total number and relative percentage of female athletes have been growing (Nunes, 2019), the increase might be different between continents. We decided to take a closer look at this in our study. 

### Home-field Advantage

Similar to the attempt at showing female participation, simple and basic tables were utilized to examine the existence of home-field advantage at the Olympics (Pettigrew & Reiche, 2016). See Figure 4.

<figure style="position: relative">
  <img src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/2-1.png" style="display: block;
margin: 0 auto;"></img>
    <div class="caption">
  Figure 4: Medals won by host countries at host year and the previous Olympics, Pettigrew & Reiche (2016)
    </div>
</figure>

This visualization shows a table comparing the total number of medals earned at the host year and the previous Olympics. Changes between the two were shown in the last column.  Among the 16 host countries from 1952 to 2012, only two countries showed negative changes, meaning that hosting the Olympics helped the country earn more medals. However, the problem with this method is that it is a little bit arbitrary to compare the host year and the adjacently previous Olympics. Changes might have been positive simply because these countries did not perform well only in the previous Games, even though they had performed well eight or more years before the host year. Therefore, it is a more robust choice to showing these countries’ Olympic performances in all years. 

Clarke (2000) did this by calculating the “Home: Away Ratio”. See Table 2.

<figure style="position: relative">
  <img src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/2-3.png" style="display: block;
margin: 0 auto;"></img>
    <div class="caption">
  Table 2: Percentage of available medals won by host countries at home and away, Clarke (2016)
    </div>
</figure>


He listed the percentage of all available medals won by countries that have ever hosted a Olympic both at the Home years and the Away years. The ratio of “Home: Away” was calculated. Obviously, a ratio larger than 1 indicates the existence of home-field advantage at the Olympics. The drawback of this method is that it only shows the summary of all the years, lacking information about these countries’ performance in each year. 

Visualizations showing all the years do exist (Grange, 2016). See Figure 5.

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/2-2.png" caption="Figure 5: Visualizing home-field advantage by Grange (2006)" class="wide">}}

For example, in this small multiple made by R, each graph has a blue vertical line emphasizing the number of medals earned during the host year, and a red horizontal line indicating the total average. It is very effective in the sense that it clearly compares the performance during the host year and all other years. The problem with this method is that lines are not very good at showing density distribution of medal numbers over the years. To improve this drawback, we decided to use kernel density estimation (KDE) coupled with small multiples. 

### Medal Efficiency

The most straightforward way of measuring a country’s efficiency of earning medals is to count the number of medals per athlete participating. This method was used by Pettigrew and Reiche (2016) in their analysis of home-field advantage. 

Some scholars argued that when assessing the efficiency of medal production, we need to take into account the resources that countries possess, such as GDP and population. From an economics perspective, Rathke and Woitek (2007) came up with a sophisticated formula calculating this efficiency, and visualized the results using multiple box plots that were stacked horizontally. See Figure 6.

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/3-2.png" caption="Figure 6: The production of Olympic Medals, 1952-2000, Rathke & Wotiek (2007)">}}

Visualizations by Eirk (2016) for the *Telegraph*, and those by medalspercapita.com also highlighted the importance of  GDP and the size of population. For example, Eirk (2016) ranked Olympic nations based on “Gold per million people” and “Gold per £100 bn GDP”. See Figure 7 and 8. 

<div class="wide">
  <div class="left">
    {{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/3-3.png" caption="Figure 7: Top 10 countries for medals per million population, Eirk (2006)">}}
  </div>
  <div class="right">
    {{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/3-4.png" caption="Figure 8: Ranking medal production considering population and GDP, Eirk (2006)">}}
  </div>
</div>

Similarly, using the concept of “medals per capita”, medalspercapita.com ranked countries based on “population per medal”, i.e., how many people are needed to generate a medal. They created a choropleth map based the results where darker colors indicate lower “medals per capita”. See Table 3 and Figure 9. 

<div class="wide">
  <div class="left">
    {{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/3-5.png" caption="Table 3: Population per medal">}}
  </div>
  <div class="right">
    {{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/3-6.png" caption="Figure 9: World map of population per medal">}}
  </div>
</div>

However, we think it is problematic to divide medal counts by population or GDP in measuring medal efficiency. First of all, this method is unfair for countries who joined the Olympics late. For example, China (PRC) attended the Olympics for the first time in 1952 and due to political issues, it was not a participant till 1984 (COC, 2004). If total number of medals is the basis for medal efficiency, it would be unfair for countries like China and many newly founded countries in Africa. 

Second, it might be unfair to divide the number of medals by population. This formula assumes that a country can send as many athletes as it wants, but this is not the case. For example, for Tokyo 2020, each country can send at most three male and three female athletes (International Table Tennis Federation, 2018). As a result, China will send six table tennis athletes, as will Australia, Japan, Brazil, Egypt, Germany, and the United States (Wikipedia, n.d.), even though China’s population size is larger than that of all the six countries combined (World Bank, 2018).

Third, it might be simplistic to only count the total number of medals. There has been a debate on whether ranking of Olympic countries should be based on the number of total medals or only golds (Johnson, 2008). We decided to adopt the method by New York Times, i.e., “medal points” (Klein, 2008). In this system, a gold medal is given 4 points, silver 2 and bronze 1. Center for Strategic International Studies (n.d.) used this method and ranked countries based on what they called as “weighted medals”. 

In this interactive, viewers can see a country’s ranking on each categories of sport in a specific Olympic Games by clicking the country’s name. This visualization is clear and direct, but it has some drawbacks. First, only the top countries can be shown interactively but there are over 200 participating countries and regions. Second, and because of the first drawback, this visualization did not provide viewers a general idea of the distribution of media efficiency across countries. See Figure 10.

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/3-7.png" class="wide" caption="Figure 10: Ranking of countries by weighted medals">}}

To solve these problems, we decided to rank countries by “medal points” as well, but on an interactive choropleth world map. 

### Ranking Sports by Number of Athletes

Dutta (2018) in his Kaggle post visualized the top 10 sports that USA excel by putting 10 boxes vertically with sporting winning the most gold medals on top. See Figure 11.

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/4-1.png" caption="Figure 11: Ranking of sports by weighted medals">}}

This visualization is transparent and clear but the problem is that it is limited to only about 10 items, which is not enough for us to visualize all the sports in the Summer Olympics. Instead, we decided to try bar chart and word cloud for our visualizations. 

## Visualization Plans
### Plans: Female Participation
As discussed above, we will use line graph, stacked bar chart, and area chart to show the overall trend of female participation in the Summer Olympics. For female participation in each individual continent, we will use KDE in a small multiple. 

In line graph, the x-axis will be time and the y-axis the percentage against the total number of participants. We will show both female and male athletes. See Figure 12.

For stacked bar chart, the x-axis will be time and y-axis will percentage against the total number of athletes. Two segments in each bar will represent male and female respectively, and the two will sum up to 100\% for every year presented. This will make the comparison between male and female participation very clear. See Figure 13.

<div class="wide">

<div class="left">

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/1.png" caption="Figure 12: Line graph for female participation">}}

</div>
<div class="right">

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/2.png" caption="Figure 13: Stacked bar chart for female participation">}}
</div>

</div>

In order to also show the changes in the total number of athletes, beside the changes in percentages, we will use a stacked area chart. The x-axis will be again time, and the y-axis will be the total number of athletes for each Olympic Games. See Figure 14.

For female participation in each individual continent over the years, we will line graphs in a small multiple. The x-axis will be time and the y-axis will be the percentage of female athletes against the total number of athletes. To make comparisons between continents and with the global average clearer, for each plot in the small multiple, we will put the line graph of other continents in the background, and we will also plot the global average as the benchmark. See Figure 15.

<div class="wide">

<div class="left">

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/3.png" caption="Figure 14: Staked area chart for female participation">}}

</div>
<div class="right">

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/4.png" caption="Figure 15: Line graph in small multiple for female participation">}}
</div>

</div>

### Plans: Home-field Advantage
To examine whether there exists a home-field advantage at the Olympics, we will first use a scatter plot with jitter. The x-axis will be countries that have ever been a host, and the y-axis will be the percentage against the total number of medals a country earned. Each dot represents an Olympic Games the country has participated. Black dots denote data for a “non-host” year and orange dots denote data for host year. See Figure 16.

To better show the density distribution of medal gains, we will employ kernel density estimation in a small multiple. The x-axis will be the percentage against the total number of medals at a Games and the y-axis will be density. We will use an arrow to denote the density of a year when the country was a host. See Figure 17.

Arrows located at points with high densities, would be signs of the existence of home-field advantage at the Olympics. 

<div class="wide">

<div class="left">

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/5.png" caption="Figure 16: Scatter plot with jittering for home-field advantage">}}

</div>
<div class="right">

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/6.png" caption="Figure 17: KDE for home-field advantage">}}
</div>

</div>

### Plans: Medal Efficiency

The index of “medal efficiency” will be calculated as medal points per athlete participating. We will use an interactive choropleth world map to show each participating country and region’s score. See Figure 18.

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/9.png" caption="Figure 18: Choropleth map for medal efficiency">}}

### Plans: Ranking Sports
First, we will use a bar chart where the x-axis will be the different sports and the y-axis the corresponding number of athletes. See Figure 19. 

Second, we will show this ranking using a word cloud in which larger font size denotes higher number of participants. This graph will be clearer and more direct because viewers can intuitively get a sense of the relative size of participation of a sport. See Figure 20.

<div class="wide">

<div class="left">

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/7.png" caption="Figure 19: Bar chart for sports ranking">}}

</div>
<div class="right">

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/8.png" caption="Figure 20: Word cloud for sports ranking">}}
</div>

</div>

## Plotting
### Female Participation over Time
As planned above, we started with a simple line graph displaying both male and female athletes’ percentage against all athletes. The strength of this method is that it is simple and clear. It shows that female percentage has been steadily growing in the past century at the Olympics. The drawback is that it does not generate a stark contrast between male and female as a stacked bar chart can do. See Figure 21.

<div id="figure23" class="vis"></div>
<div class="caption">Figure 21: Line graph for changes in female participation</div>

We then used stacked bar graphs. We first tried stacking the bar horizontally with percentage on the x-axis and time on y-axis. See Figure 22.

<div id="figure24" class="vis"></div>
<div class="caption">Figure 22: Horizontal stacked bar chart for changes in female participation</div>


It was not as beautiful as we wanted, so we tried to put it upright and replace the axis labels. To highlight the trend, we set the male section grey and the female part bright blue. We also drew a red line at the intersection of the two parts. This time, female participation was obviously highlighted and the trend shown very clearly. See Figure 23.


<div id="figure25" class="vis"></div>
<div class="caption">Figure 23: Vertical stacked bar chart for changes in female participation</div>

However, as discussed above, stacked bar charts can only show the changes in percentages, not those in actual number of participants. To also visualize how the total number of athletes participating in Summer Olympics changed over the century, we opted stacked area chart. See Figure 24.

<div id="figure26" class="vis"></div>
<div class="caption">Figure 24: Stacked area chart for changes in female participation</div>

The x-axis denotes time and the y-axis number of athletes. Areas are made up of male and female participants. The two added up to the total number of athletes. This stacked area chart not only shows the changes in female participation, it also displays how the total number of athletes has been increasing over the years. The drawback is that area is not a much preferred visual encoding. As a result, the comparison of percentages of male and female is not very accurate. That said, we think its strengths outweigh its disadvantages.


<script type="text/javascript">
var figure23 = {
  "$schema": "https://vega.github.io/schema/vega/v5.json",
  "background": "white",
  "padding": 5,
  "width": 700,
  "height": 300,
  "title": {
    "text": "Changes in female athletes participation in Summer Olympics (1896-2016)",
    "frame": "group"
  },
  "style": "cell",
  "data": [
    {"name": "selector017_store"},
    {
      "name": "data-acf04d5a8ed5b056492542ad6eb1d357",
      "values": [
        {
          "Unnamed: 0": 0,
          "Year": 1896,
          "Sex": "M",
          "Frequency": 380,
          "Percentage_decimal": 1,
          "Percentage": "100.0%"
        },
        {
          "Unnamed: 0": 1,
          "Year": 1896,
          "Sex": "F",
          "Frequency": 0,
          "Percentage_decimal": 0,
          "Percentage": "0.0%"
        },
        {
          "Unnamed: 0": 2,
          "Year": 1900,
          "Sex": "M",
          "Frequency": 1903,
          "Percentage_decimal": 0.983,
          "Percentage": "98.3%"
        },
        {
          "Unnamed: 0": 3,
          "Year": 1900,
          "Sex": "F",
          "Frequency": 33,
          "Percentage_decimal": 0.017,
          "Percentage": "1.7%"
        },
        {
          "Unnamed: 0": 4,
          "Year": 1904,
          "Sex": "M",
          "Frequency": 1285,
          "Percentage_decimal": 0.988,
          "Percentage": "98.8%"
        },
        {
          "Unnamed: 0": 5,
          "Year": 1904,
          "Sex": "F",
          "Frequency": 16,
          "Percentage_decimal": 0.012,
          "Percentage": "1.2%"
        },
        {
          "Unnamed: 0": 6,
          "Year": 1906,
          "Sex": "M",
          "Frequency": 1722,
          "Percentage_decimal": 0.9940000000000001,
          "Percentage": "99.4%"
        },
        {
          "Unnamed: 0": 7,
          "Year": 1906,
          "Sex": "F",
          "Frequency": 11,
          "Percentage_decimal": 0.006,
          "Percentage": "0.6%"
        },
        {
          "Unnamed: 0": 8,
          "Year": 1908,
          "Sex": "M",
          "Frequency": 3054,
          "Percentage_decimal": 0.985,
          "Percentage": "98.5%"
        },
        {
          "Unnamed: 0": 9,
          "Year": 1908,
          "Sex": "F",
          "Frequency": 47,
          "Percentage_decimal": 0.015,
          "Percentage": "1.5%"
        },
        {
          "Unnamed: 0": 10,
          "Year": 1912,
          "Sex": "M",
          "Frequency": 3953,
          "Percentage_decimal": 0.978,
          "Percentage": "97.8%"
        },
        {
          "Unnamed: 0": 11,
          "Year": 1912,
          "Sex": "F",
          "Frequency": 87,
          "Percentage_decimal": 0.022000000000000002,
          "Percentage": "2.2%"
        },
        {
          "Unnamed: 0": 12,
          "Year": 1920,
          "Sex": "M",
          "Frequency": 4158,
          "Percentage_decimal": 0.9690000000000001,
          "Percentage": "96.9%"
        },
        {
          "Unnamed: 0": 13,
          "Year": 1920,
          "Sex": "F",
          "Frequency": 134,
          "Percentage_decimal": 0.031,
          "Percentage": "3.1%"
        },
        {
          "Unnamed: 0": 14,
          "Year": 1924,
          "Sex": "M",
          "Frequency": 4989,
          "Percentage_decimal": 0.953,
          "Percentage": "95.3%"
        },
        {
          "Unnamed: 0": 15,
          "Year": 1924,
          "Sex": "F",
          "Frequency": 244,
          "Percentage_decimal": 0.047,
          "Percentage": "4.7%"
        },
        {
          "Unnamed: 0": 16,
          "Year": 1928,
          "Sex": "M",
          "Frequency": 4588,
          "Percentage_decimal": 0.919,
          "Percentage": "91.9%"
        },
        {
          "Unnamed: 0": 17,
          "Year": 1928,
          "Sex": "F",
          "Frequency": 404,
          "Percentage_decimal": 0.081,
          "Percentage": "8.1%"
        },
        {
          "Unnamed: 0": 18,
          "Year": 1932,
          "Sex": "M",
          "Frequency": 2622,
          "Percentage_decimal": 0.883,
          "Percentage": "88.3%"
        },
        {
          "Unnamed: 0": 19,
          "Year": 1932,
          "Sex": "F",
          "Frequency": 347,
          "Percentage_decimal": 0.11699999999999999,
          "Percentage": "11.7%"
        },
        {
          "Unnamed: 0": 20,
          "Year": 1936,
          "Sex": "M",
          "Frequency": 6038,
          "Percentage_decimal": 0.9279999999999999,
          "Percentage": "92.8%"
        },
        {
          "Unnamed: 0": 21,
          "Year": 1936,
          "Sex": "F",
          "Frequency": 468,
          "Percentage_decimal": 0.07200000000000001,
          "Percentage": "7.2%"
        },
        {
          "Unnamed: 0": 22,
          "Year": 1948,
          "Sex": "M",
          "Frequency": 5777,
          "Percentage_decimal": 0.902,
          "Percentage": "90.2%"
        },
        {
          "Unnamed: 0": 23,
          "Year": 1948,
          "Sex": "F",
          "Frequency": 628,
          "Percentage_decimal": 0.098,
          "Percentage": "9.8%"
        },
        {
          "Unnamed: 0": 24,
          "Year": 1952,
          "Sex": "M",
          "Frequency": 6773,
          "Percentage_decimal": 0.8190000000000001,
          "Percentage": "81.9%"
        },
        {
          "Unnamed: 0": 25,
          "Year": 1952,
          "Sex": "F",
          "Frequency": 1497,
          "Percentage_decimal": 0.18100000000000002,
          "Percentage": "18.1%"
        },
        {
          "Unnamed: 0": 26,
          "Year": 1956,
          "Sex": "M",
          "Frequency": 4234,
          "Percentage_decimal": 0.826,
          "Percentage": "82.6%"
        },
        {
          "Unnamed: 0": 27,
          "Year": 1956,
          "Sex": "F",
          "Frequency": 893,
          "Percentage_decimal": 0.174,
          "Percentage": "17.4%"
        },
        {
          "Unnamed: 0": 28,
          "Year": 1960,
          "Sex": "M",
          "Frequency": 6684,
          "Percentage_decimal": 0.823,
          "Percentage": "82.3%"
        },
        {
          "Unnamed: 0": 29,
          "Year": 1960,
          "Sex": "F",
          "Frequency": 1435,
          "Percentage_decimal": 0.177,
          "Percentage": "17.7%"
        },
        {
          "Unnamed: 0": 30,
          "Year": 1964,
          "Sex": "M",
          "Frequency": 6354,
          "Percentage_decimal": 0.825,
          "Percentage": "82.5%"
        },
        {
          "Unnamed: 0": 31,
          "Year": 1964,
          "Sex": "F",
          "Frequency": 1348,
          "Percentage_decimal": 0.175,
          "Percentage": "17.5%"
        },
        {
          "Unnamed: 0": 32,
          "Year": 1968,
          "Sex": "M",
          "Frequency": 6811,
          "Percentage_decimal": 0.7929999999999999,
          "Percentage": "79.3%"
        },
        {
          "Unnamed: 0": 33,
          "Year": 1968,
          "Sex": "F",
          "Frequency": 1777,
          "Percentage_decimal": 0.207,
          "Percentage": "20.7%"
        },
        {
          "Unnamed: 0": 34,
          "Year": 1972,
          "Sex": "M",
          "Frequency": 8111,
          "Percentage_decimal": 0.787,
          "Percentage": "78.7%"
        },
        {
          "Unnamed: 0": 35,
          "Year": 1972,
          "Sex": "F",
          "Frequency": 2193,
          "Percentage_decimal": 0.213,
          "Percentage": "21.3%"
        },
        {
          "Unnamed: 0": 36,
          "Year": 1976,
          "Sex": "M",
          "Frequency": 6469,
          "Percentage_decimal": 0.7490000000000001,
          "Percentage": "74.9%"
        },
        {
          "Unnamed: 0": 37,
          "Year": 1976,
          "Sex": "F",
          "Frequency": 2172,
          "Percentage_decimal": 0.251,
          "Percentage": "25.1%"
        },
        {
          "Unnamed: 0": 38,
          "Year": 1980,
          "Sex": "M",
          "Frequency": 5435,
          "Percentage_decimal": 0.7559999999999999,
          "Percentage": "75.6%"
        },
        {
          "Unnamed: 0": 39,
          "Year": 1980,
          "Sex": "F",
          "Frequency": 1756,
          "Percentage_decimal": 0.244,
          "Percentage": "24.4%"
        },
        {
          "Unnamed: 0": 40,
          "Year": 1984,
          "Sex": "M",
          "Frequency": 7007,
          "Percentage_decimal": 0.741,
          "Percentage": "74.1%"
        },
        {
          "Unnamed: 0": 41,
          "Year": 1984,
          "Sex": "F",
          "Frequency": 2447,
          "Percentage_decimal": 0.259,
          "Percentage": "25.9%"
        },
        {
          "Unnamed: 0": 42,
          "Year": 1988,
          "Sex": "M",
          "Frequency": 8494,
          "Percentage_decimal": 0.706,
          "Percentage": "70.6%"
        },
        {
          "Unnamed: 0": 43,
          "Year": 1988,
          "Sex": "F",
          "Frequency": 3543,
          "Percentage_decimal": 0.294,
          "Percentage": "29.4%"
        },
        {
          "Unnamed: 0": 44,
          "Year": 1992,
          "Sex": "M",
          "Frequency": 8853,
          "Percentage_decimal": 0.682,
          "Percentage": "68.2%"
        },
        {
          "Unnamed: 0": 45,
          "Year": 1992,
          "Sex": "F",
          "Frequency": 4124,
          "Percentage_decimal": 0.318,
          "Percentage": "31.8%"
        },
        {
          "Unnamed: 0": 46,
          "Year": 1996,
          "Sex": "M",
          "Frequency": 8772,
          "Percentage_decimal": 0.637,
          "Percentage": "63.7%"
        },
        {
          "Unnamed: 0": 47,
          "Year": 1996,
          "Sex": "F",
          "Frequency": 5008,
          "Percentage_decimal": 0.363,
          "Percentage": "36.3%"
        },
        {
          "Unnamed: 0": 48,
          "Year": 2000,
          "Sex": "M",
          "Frequency": 8390,
          "Percentage_decimal": 0.607,
          "Percentage": "60.7%"
        },
        {
          "Unnamed: 0": 49,
          "Year": 2000,
          "Sex": "F",
          "Frequency": 5431,
          "Percentage_decimal": 0.39299999999999996,
          "Percentage": "39.3%"
        },
        {
          "Unnamed: 0": 50,
          "Year": 2004,
          "Sex": "M",
          "Frequency": 7897,
          "Percentage_decimal": 0.5870000000000001,
          "Percentage": "58.7%"
        },
        {
          "Unnamed: 0": 51,
          "Year": 2004,
          "Sex": "F",
          "Frequency": 5546,
          "Percentage_decimal": 0.413,
          "Percentage": "41.3%"
        },
        {
          "Unnamed: 0": 52,
          "Year": 2008,
          "Sex": "M",
          "Frequency": 7786,
          "Percentage_decimal": 0.5720000000000001,
          "Percentage": "57.2%"
        },
        {
          "Unnamed: 0": 53,
          "Year": 2008,
          "Sex": "F",
          "Frequency": 5816,
          "Percentage_decimal": 0.428,
          "Percentage": "42.8%"
        },
        {
          "Unnamed: 0": 54,
          "Year": 2012,
          "Sex": "M",
          "Frequency": 7105,
          "Percentage_decimal": 0.55,
          "Percentage": "55.0%"
        },
        {
          "Unnamed: 0": 55,
          "Year": 2012,
          "Sex": "F",
          "Frequency": 5815,
          "Percentage_decimal": 0.45,
          "Percentage": "45.0%"
        },
        {
          "Unnamed: 0": 56,
          "Year": 2016,
          "Sex": "M",
          "Frequency": 7465,
          "Percentage_decimal": 0.545,
          "Percentage": "54.5%"
        },
        {
          "Unnamed: 0": 57,
          "Year": 2016,
          "Sex": "F",
          "Frequency": 6223,
          "Percentage_decimal": 0.455,
          "Percentage": "45.5%"
        }
      ]
    },
    {
      "name": "data_0",
      "source": "data-acf04d5a8ed5b056492542ad6eb1d357",
      "transform": [
        {"type": "formula", "expr": "toNumber(datum[\"Year\"])", "as": "Year"}
      ]
    }
  ],
  "signals": [
    {
      "name": "unit",
      "value": {},
      "on": [
        {"events": "mousemove", "update": "isTuple(group()) ? group() : unit"}
      ]
    },
    {
      "name": "selector017",
      "update": "vlSelectionResolve(\"selector017_store\", \"union\")"
    },
    {
      "name": "selector017_Year",
      "on": [
        {
          "events": {"signal": "selector017_translate_delta"},
          "update": "panLinear(selector017_translate_anchor.extent_x, -selector017_translate_delta.x / width)"
        },
        {
          "events": {"signal": "selector017_zoom_delta"},
          "update": "zoomLinear(domain(\"x\"), selector017_zoom_anchor.x, selector017_zoom_delta)"
        },
        {"events": [{"source": "scope", "type": "dblclick"}], "update": "null"}
      ]
    },
    {
      "name": "selector017_Percentage_decimal",
      "on": [
        {
          "events": {"signal": "selector017_translate_delta"},
          "update": "panLinear(selector017_translate_anchor.extent_y, selector017_translate_delta.y / height)"
        },
        {
          "events": {"signal": "selector017_zoom_delta"},
          "update": "zoomLinear(domain(\"y\"), selector017_zoom_anchor.y, selector017_zoom_delta)"
        },
        {"events": [{"source": "scope", "type": "dblclick"}], "update": "null"}
      ]
    },
    {
      "name": "selector017_tuple",
      "on": [
        {
          "events": [
            {"signal": "selector017_Year || selector017_Percentage_decimal"}
          ],
          "update": "selector017_Year && selector017_Percentage_decimal ? {unit: \"\", fields: selector017_tuple_fields, values: [selector017_Year,selector017_Percentage_decimal]} : null"
        }
      ]
    },
    {
      "name": "selector017_tuple_fields",
      "value": [
        {"field": "Year", "channel": "x", "type": "R"},
        {"field": "Percentage_decimal", "channel": "y", "type": "R"}
      ]
    },
    {
      "name": "selector017_translate_anchor",
      "value": {},
      "on": [
        {
          "events": [{"source": "scope", "type": "mousedown"}],
          "update": "{x: x(unit), y: y(unit), extent_x: domain(\"x\"), extent_y: domain(\"y\")}"
        }
      ]
    },
    {
      "name": "selector017_translate_delta",
      "value": {},
      "on": [
        {
          "events": [
            {
              "source": "window",
              "type": "mousemove",
              "consume": true,
              "between": [
                {"source": "scope", "type": "mousedown"},
                {"source": "window", "type": "mouseup"}
              ]
            }
          ],
          "update": "{x: selector017_translate_anchor.x - x(unit), y: selector017_translate_anchor.y - y(unit)}"
        }
      ]
    },
    {
      "name": "selector017_zoom_anchor",
      "on": [
        {
          "events": [{"source": "scope", "type": "wheel", "consume": true}],
          "update": "{x: invert(\"x\", x(unit)), y: invert(\"y\", y(unit))}"
        }
      ]
    },
    {
      "name": "selector017_zoom_delta",
      "on": [
        {
          "events": [{"source": "scope", "type": "wheel", "consume": true}],
          "force": true,
          "update": "pow(1.001, event.deltaY * pow(16, event.deltaMode))"
        }
      ]
    },
    {
      "name": "selector017_modify",
      "on": [
        {
          "events": {"signal": "selector017_tuple"},
          "update": "modify(\"selector017_store\", selector017_tuple, true)"
        }
      ]
    }
  ],
  "marks": [
    {
      "name": "pathgroup",
      "type": "group",
      "from": {
        "facet": {
          "name": "faceted_path_main",
          "data": "data_0",
          "groupby": ["Sex"]
        }
      },
      "encode": {
        "update": {
          "width": {"field": {"group": "width"}},
          "height": {"field": {"group": "height"}}
        }
      },
      "marks": [
        {
          "name": "marks",
          "type": "line",
          "clip": true,
          "style": ["line"],
          "sort": {"field": "datum[\"Year\"]"},
          "interactive": true,
          "from": {"data": "faceted_path_main"},
          "encode": {
            "update": {
              "stroke": {"scale": "color", "field": "Sex"},
              "tooltip": {
                "signal": "{\"Year\": format(datum[\"Year\"], \"\"), \"Sex\": isValid(datum[\"Sex\"]) ? datum[\"Sex\"] : \"\"+datum[\"Sex\"], \"Percentage\": isValid(datum[\"Percentage\"]) ? datum[\"Percentage\"] : \"\"+datum[\"Percentage\"]}"
              },
              "description": {
                "signal": "\"Sex\" + \": \" + (isValid(datum[\"Sex\"]) ? datum[\"Sex\"] : \"\"+datum[\"Sex\"]) + \"; \" + \"Year\" + \": \" + (format(datum[\"Year\"], \"\")) + \"; \" + \"Percentage\" + \": \" + (format(datum[\"Percentage_decimal\"], \"%\"))"
              },
              "x": {"scale": "x", "field": "Year"},
              "y": {"scale": "y", "field": "Percentage_decimal"},
              "strokeWidth": {"value": 5},
              "defined": {
                "signal": "isValid(datum[\"Year\"]) && isFinite(+datum[\"Year\"]) && isValid(datum[\"Percentage_decimal\"]) && isFinite(+datum[\"Percentage_decimal\"])"
              }
            }
          }
        }
      ]
    }
  ],
  "scales": [
    {
      "name": "x",
      "type": "linear",
      "domain": {"data": "data_0", "field": "Year"},
      "domainRaw": {"signal": "selector017[\"Year\"]"},
      "range": [0, {"signal": "width"}],
      "nice": true,
      "zero": false
    },
    {
      "name": "y",
      "type": "linear",
      "domain": {"data": "data_0", "field": "Percentage_decimal"},
      "domainRaw": {"signal": "selector017[\"Percentage_decimal\"]"},
      "range": [{"signal": "height"}, 0],
      "nice": true,
      "zero": true
    },
    {
      "name": "color",
      "type": "ordinal",
      "domain": {"data": "data_0", "field": "Sex", "sort": true},
      "range": "category"
    }
  ],
  "axes": [
    {
      "scale": "x",
      "orient": "bottom",
      "gridScale": "y",
      "grid": true,
      "tickCount": {"signal": "ceil(width/40)"},
      "domain": false,
      "labels": false,
      "aria": false,
      "maxExtent": 0,
      "minExtent": 0,
      "ticks": false,
      "zindex": 0
    },
    {
      "scale": "y",
      "orient": "left",
      "gridScale": "x",
      "grid": true,
      "tickCount": {"signal": "ceil(height/40)"},
      "domain": false,
      "labels": false,
      "aria": false,
      "maxExtent": 0,
      "minExtent": 0,
      "ticks": false,
      "zindex": 0
    },
    {
      "scale": "x",
      "orient": "bottom",
      "grid": false,
      "title": "Year",
      "labelFlush": true,
      "labelOverlap": true,
      "tickCount": {"signal": "ceil(width/40)"},
      "zindex": 0
    },
    {
      "scale": "y",
      "orient": "left",
      "grid": false,
      "title": "Percentage",
      "format": "%",
      "labelOverlap": true,
      "tickCount": {"signal": "ceil(height/40)"},
      "zindex": 0
    }
  ],
  "legends": [{"stroke": "color", "symbolType": "stroke", "title": "Sex"}],
  "config": {
    "legend": {
      "cornerRadius": 10,
      "fillColor": "#EEEEEE",
      "labelFontSize": 14,
      "padding": 10,
      "strokeColor": "gray"
    },
    "style": {"group-title": {"fontSize": 16}},
    "axis": {"labelFontSize": 12, "titleFontSize": 14}
  }
};
      vegaEmbed('#figure23', figure23);
</script>

<script type="text/javascript">
var figure24 = {
  "$schema": "https://vega.github.io/schema/vega/v5.json",
  "background": "white",
  "padding": 5,
  "width": 700,
  "height": 300,
  "title": {
    "text": "Changes in female athletes participation in Summer Olympics (1896-2016)",
    "frame": "group"
  },
  "style": "cell",
  "data": [
    {"name": "selector018_store"},
    {
      "name": "data-acf04d5a8ed5b056492542ad6eb1d357",
      "values": [
        {
          "Unnamed: 0": 0,
          "Year": 1896,
          "Sex": "M",
          "Frequency": 380,
          "Percentage_decimal": 1,
          "Percentage": "100.0%"
        },
        {
          "Unnamed: 0": 1,
          "Year": 1896,
          "Sex": "F",
          "Frequency": 0,
          "Percentage_decimal": 0,
          "Percentage": "0.0%"
        },
        {
          "Unnamed: 0": 2,
          "Year": 1900,
          "Sex": "M",
          "Frequency": 1903,
          "Percentage_decimal": 0.983,
          "Percentage": "98.3%"
        },
        {
          "Unnamed: 0": 3,
          "Year": 1900,
          "Sex": "F",
          "Frequency": 33,
          "Percentage_decimal": 0.017,
          "Percentage": "1.7%"
        },
        {
          "Unnamed: 0": 4,
          "Year": 1904,
          "Sex": "M",
          "Frequency": 1285,
          "Percentage_decimal": 0.988,
          "Percentage": "98.8%"
        },
        {
          "Unnamed: 0": 5,
          "Year": 1904,
          "Sex": "F",
          "Frequency": 16,
          "Percentage_decimal": 0.012,
          "Percentage": "1.2%"
        },
        {
          "Unnamed: 0": 6,
          "Year": 1906,
          "Sex": "M",
          "Frequency": 1722,
          "Percentage_decimal": 0.9940000000000001,
          "Percentage": "99.4%"
        },
        {
          "Unnamed: 0": 7,
          "Year": 1906,
          "Sex": "F",
          "Frequency": 11,
          "Percentage_decimal": 0.006,
          "Percentage": "0.6%"
        },
        {
          "Unnamed: 0": 8,
          "Year": 1908,
          "Sex": "M",
          "Frequency": 3054,
          "Percentage_decimal": 0.985,
          "Percentage": "98.5%"
        },
        {
          "Unnamed: 0": 9,
          "Year": 1908,
          "Sex": "F",
          "Frequency": 47,
          "Percentage_decimal": 0.015,
          "Percentage": "1.5%"
        },
        {
          "Unnamed: 0": 10,
          "Year": 1912,
          "Sex": "M",
          "Frequency": 3953,
          "Percentage_decimal": 0.978,
          "Percentage": "97.8%"
        },
        {
          "Unnamed: 0": 11,
          "Year": 1912,
          "Sex": "F",
          "Frequency": 87,
          "Percentage_decimal": 0.022000000000000002,
          "Percentage": "2.2%"
        },
        {
          "Unnamed: 0": 12,
          "Year": 1920,
          "Sex": "M",
          "Frequency": 4158,
          "Percentage_decimal": 0.9690000000000001,
          "Percentage": "96.9%"
        },
        {
          "Unnamed: 0": 13,
          "Year": 1920,
          "Sex": "F",
          "Frequency": 134,
          "Percentage_decimal": 0.031,
          "Percentage": "3.1%"
        },
        {
          "Unnamed: 0": 14,
          "Year": 1924,
          "Sex": "M",
          "Frequency": 4989,
          "Percentage_decimal": 0.953,
          "Percentage": "95.3%"
        },
        {
          "Unnamed: 0": 15,
          "Year": 1924,
          "Sex": "F",
          "Frequency": 244,
          "Percentage_decimal": 0.047,
          "Percentage": "4.7%"
        },
        {
          "Unnamed: 0": 16,
          "Year": 1928,
          "Sex": "M",
          "Frequency": 4588,
          "Percentage_decimal": 0.919,
          "Percentage": "91.9%"
        },
        {
          "Unnamed: 0": 17,
          "Year": 1928,
          "Sex": "F",
          "Frequency": 404,
          "Percentage_decimal": 0.081,
          "Percentage": "8.1%"
        },
        {
          "Unnamed: 0": 18,
          "Year": 1932,
          "Sex": "M",
          "Frequency": 2622,
          "Percentage_decimal": 0.883,
          "Percentage": "88.3%"
        },
        {
          "Unnamed: 0": 19,
          "Year": 1932,
          "Sex": "F",
          "Frequency": 347,
          "Percentage_decimal": 0.11699999999999999,
          "Percentage": "11.7%"
        },
        {
          "Unnamed: 0": 20,
          "Year": 1936,
          "Sex": "M",
          "Frequency": 6038,
          "Percentage_decimal": 0.9279999999999999,
          "Percentage": "92.8%"
        },
        {
          "Unnamed: 0": 21,
          "Year": 1936,
          "Sex": "F",
          "Frequency": 468,
          "Percentage_decimal": 0.07200000000000001,
          "Percentage": "7.2%"
        },
        {
          "Unnamed: 0": 22,
          "Year": 1948,
          "Sex": "M",
          "Frequency": 5777,
          "Percentage_decimal": 0.902,
          "Percentage": "90.2%"
        },
        {
          "Unnamed: 0": 23,
          "Year": 1948,
          "Sex": "F",
          "Frequency": 628,
          "Percentage_decimal": 0.098,
          "Percentage": "9.8%"
        },
        {
          "Unnamed: 0": 24,
          "Year": 1952,
          "Sex": "M",
          "Frequency": 6773,
          "Percentage_decimal": 0.8190000000000001,
          "Percentage": "81.9%"
        },
        {
          "Unnamed: 0": 25,
          "Year": 1952,
          "Sex": "F",
          "Frequency": 1497,
          "Percentage_decimal": 0.18100000000000002,
          "Percentage": "18.1%"
        },
        {
          "Unnamed: 0": 26,
          "Year": 1956,
          "Sex": "M",
          "Frequency": 4234,
          "Percentage_decimal": 0.826,
          "Percentage": "82.6%"
        },
        {
          "Unnamed: 0": 27,
          "Year": 1956,
          "Sex": "F",
          "Frequency": 893,
          "Percentage_decimal": 0.174,
          "Percentage": "17.4%"
        },
        {
          "Unnamed: 0": 28,
          "Year": 1960,
          "Sex": "M",
          "Frequency": 6684,
          "Percentage_decimal": 0.823,
          "Percentage": "82.3%"
        },
        {
          "Unnamed: 0": 29,
          "Year": 1960,
          "Sex": "F",
          "Frequency": 1435,
          "Percentage_decimal": 0.177,
          "Percentage": "17.7%"
        },
        {
          "Unnamed: 0": 30,
          "Year": 1964,
          "Sex": "M",
          "Frequency": 6354,
          "Percentage_decimal": 0.825,
          "Percentage": "82.5%"
        },
        {
          "Unnamed: 0": 31,
          "Year": 1964,
          "Sex": "F",
          "Frequency": 1348,
          "Percentage_decimal": 0.175,
          "Percentage": "17.5%"
        },
        {
          "Unnamed: 0": 32,
          "Year": 1968,
          "Sex": "M",
          "Frequency": 6811,
          "Percentage_decimal": 0.7929999999999999,
          "Percentage": "79.3%"
        },
        {
          "Unnamed: 0": 33,
          "Year": 1968,
          "Sex": "F",
          "Frequency": 1777,
          "Percentage_decimal": 0.207,
          "Percentage": "20.7%"
        },
        {
          "Unnamed: 0": 34,
          "Year": 1972,
          "Sex": "M",
          "Frequency": 8111,
          "Percentage_decimal": 0.787,
          "Percentage": "78.7%"
        },
        {
          "Unnamed: 0": 35,
          "Year": 1972,
          "Sex": "F",
          "Frequency": 2193,
          "Percentage_decimal": 0.213,
          "Percentage": "21.3%"
        },
        {
          "Unnamed: 0": 36,
          "Year": 1976,
          "Sex": "M",
          "Frequency": 6469,
          "Percentage_decimal": 0.7490000000000001,
          "Percentage": "74.9%"
        },
        {
          "Unnamed: 0": 37,
          "Year": 1976,
          "Sex": "F",
          "Frequency": 2172,
          "Percentage_decimal": 0.251,
          "Percentage": "25.1%"
        },
        {
          "Unnamed: 0": 38,
          "Year": 1980,
          "Sex": "M",
          "Frequency": 5435,
          "Percentage_decimal": 0.7559999999999999,
          "Percentage": "75.6%"
        },
        {
          "Unnamed: 0": 39,
          "Year": 1980,
          "Sex": "F",
          "Frequency": 1756,
          "Percentage_decimal": 0.244,
          "Percentage": "24.4%"
        },
        {
          "Unnamed: 0": 40,
          "Year": 1984,
          "Sex": "M",
          "Frequency": 7007,
          "Percentage_decimal": 0.741,
          "Percentage": "74.1%"
        },
        {
          "Unnamed: 0": 41,
          "Year": 1984,
          "Sex": "F",
          "Frequency": 2447,
          "Percentage_decimal": 0.259,
          "Percentage": "25.9%"
        },
        {
          "Unnamed: 0": 42,
          "Year": 1988,
          "Sex": "M",
          "Frequency": 8494,
          "Percentage_decimal": 0.706,
          "Percentage": "70.6%"
        },
        {
          "Unnamed: 0": 43,
          "Year": 1988,
          "Sex": "F",
          "Frequency": 3543,
          "Percentage_decimal": 0.294,
          "Percentage": "29.4%"
        },
        {
          "Unnamed: 0": 44,
          "Year": 1992,
          "Sex": "M",
          "Frequency": 8853,
          "Percentage_decimal": 0.682,
          "Percentage": "68.2%"
        },
        {
          "Unnamed: 0": 45,
          "Year": 1992,
          "Sex": "F",
          "Frequency": 4124,
          "Percentage_decimal": 0.318,
          "Percentage": "31.8%"
        },
        {
          "Unnamed: 0": 46,
          "Year": 1996,
          "Sex": "M",
          "Frequency": 8772,
          "Percentage_decimal": 0.637,
          "Percentage": "63.7%"
        },
        {
          "Unnamed: 0": 47,
          "Year": 1996,
          "Sex": "F",
          "Frequency": 5008,
          "Percentage_decimal": 0.363,
          "Percentage": "36.3%"
        },
        {
          "Unnamed: 0": 48,
          "Year": 2000,
          "Sex": "M",
          "Frequency": 8390,
          "Percentage_decimal": 0.607,
          "Percentage": "60.7%"
        },
        {
          "Unnamed: 0": 49,
          "Year": 2000,
          "Sex": "F",
          "Frequency": 5431,
          "Percentage_decimal": 0.39299999999999996,
          "Percentage": "39.3%"
        },
        {
          "Unnamed: 0": 50,
          "Year": 2004,
          "Sex": "M",
          "Frequency": 7897,
          "Percentage_decimal": 0.5870000000000001,
          "Percentage": "58.7%"
        },
        {
          "Unnamed: 0": 51,
          "Year": 2004,
          "Sex": "F",
          "Frequency": 5546,
          "Percentage_decimal": 0.413,
          "Percentage": "41.3%"
        },
        {
          "Unnamed: 0": 52,
          "Year": 2008,
          "Sex": "M",
          "Frequency": 7786,
          "Percentage_decimal": 0.5720000000000001,
          "Percentage": "57.2%"
        },
        {
          "Unnamed: 0": 53,
          "Year": 2008,
          "Sex": "F",
          "Frequency": 5816,
          "Percentage_decimal": 0.428,
          "Percentage": "42.8%"
        },
        {
          "Unnamed: 0": 54,
          "Year": 2012,
          "Sex": "M",
          "Frequency": 7105,
          "Percentage_decimal": 0.55,
          "Percentage": "55.0%"
        },
        {
          "Unnamed: 0": 55,
          "Year": 2012,
          "Sex": "F",
          "Frequency": 5815,
          "Percentage_decimal": 0.45,
          "Percentage": "45.0%"
        },
        {
          "Unnamed: 0": 56,
          "Year": 2016,
          "Sex": "M",
          "Frequency": 7465,
          "Percentage_decimal": 0.545,
          "Percentage": "54.5%"
        },
        {
          "Unnamed: 0": 57,
          "Year": 2016,
          "Sex": "F",
          "Frequency": 6223,
          "Percentage_decimal": 0.455,
          "Percentage": "45.5%"
        }
      ]
    },
    {
      "name": "data_0",
      "source": "data-acf04d5a8ed5b056492542ad6eb1d357",
      "transform": [
        {
          "type": "aggregate",
          "groupby": ["Sex", "Year", "Percentage"],
          "ops": ["sum"],
          "fields": ["Frequency"],
          "as": ["sum_Frequency"]
        },
        {
          "type": "stack",
          "groupby": ["Year"],
          "field": "sum_Frequency",
          "sort": {"field": ["Sex"], "order": ["ascending"]},
          "as": ["sum_Frequency_start", "sum_Frequency_end"],
          "offset": "normalize"
        },
        {
          "type": "filter",
          "expr": "isValid(datum[\"sum_Frequency\"]) && isFinite(+datum[\"sum_Frequency\"]) && isValid(datum[\"Year\"]) && isFinite(+datum[\"Year\"])"
        }
      ]
    }
  ],
  "signals": [
    {
      "name": "unit",
      "value": {},
      "on": [
        {"events": "mousemove", "update": "isTuple(group()) ? group() : unit"}
      ]
    },
    {
      "name": "selector018",
      "update": "vlSelectionResolve(\"selector018_store\", \"union\")"
    },
    {
      "name": "selector018_Year",
      "on": [
        {
          "events": {"signal": "selector018_translate_delta"},
          "update": "panLinear(selector018_translate_anchor.extent_y, selector018_translate_delta.y / height)"
        },
        {
          "events": {"signal": "selector018_zoom_delta"},
          "update": "zoomLinear(domain(\"y\"), selector018_zoom_anchor.y, selector018_zoom_delta)"
        },
        {"events": [{"source": "scope", "type": "dblclick"}], "update": "null"}
      ]
    },
    {
      "name": "selector018_tuple",
      "on": [
        {
          "events": [{"signal": "selector018_Year"}],
          "update": "selector018_Year ? {unit: \"\", fields: selector018_tuple_fields, values: [selector018_Year]} : null"
        }
      ]
    },
    {
      "name": "selector018_tuple_fields",
      "value": [{"field": "Year", "channel": "y", "type": "R"}]
    },
    {
      "name": "selector018_translate_anchor",
      "value": {},
      "on": [
        {
          "events": [{"source": "scope", "type": "mousedown"}],
          "update": "{x: x(unit), y: y(unit), extent_y: domain(\"y\")}"
        }
      ]
    },
    {
      "name": "selector018_translate_delta",
      "value": {},
      "on": [
        {
          "events": [
            {
              "source": "window",
              "type": "mousemove",
              "consume": true,
              "between": [
                {"source": "scope", "type": "mousedown"},
                {"source": "window", "type": "mouseup"}
              ]
            }
          ],
          "update": "{x: selector018_translate_anchor.x - x(unit), y: selector018_translate_anchor.y - y(unit)}"
        }
      ]
    },
    {
      "name": "selector018_zoom_anchor",
      "on": [
        {
          "events": [{"source": "scope", "type": "wheel", "consume": true}],
          "update": "{x: invert(\"x\", x(unit)), y: invert(\"y\", y(unit))}"
        }
      ]
    },
    {
      "name": "selector018_zoom_delta",
      "on": [
        {
          "events": [{"source": "scope", "type": "wheel", "consume": true}],
          "force": true,
          "update": "pow(1.001, event.deltaY * pow(16, event.deltaMode))"
        }
      ]
    },
    {
      "name": "selector018_modify",
      "on": [
        {
          "events": {"signal": "selector018_tuple"},
          "update": "modify(\"selector018_store\", selector018_tuple, true)"
        }
      ]
    }
  ],
  "marks": [
    {
      "name": "marks",
      "type": "rect",
      "clip": true,
      "style": ["bar"],
      "interactive": true,
      "from": {"data": "data_0"},
      "encode": {
        "update": {
          "fill": {"scale": "color", "field": "Sex"},
          "tooltip": {
            "signal": "{\"Year\": format(datum[\"Year\"], \"\"), \"Sex\": isValid(datum[\"Sex\"]) ? datum[\"Sex\"] : \"\"+datum[\"Sex\"], \"Percentage\": isValid(datum[\"Percentage\"]) ? datum[\"Percentage\"] : \"\"+datum[\"Percentage\"]}"
          },
          "ariaRoleDescription": {"value": "bar"},
          "description": {
            "signal": "\"Sex\" + \": \" + (isValid(datum[\"Sex\"]) ? datum[\"Sex\"] : \"\"+datum[\"Sex\"]) + \"; \" + \"Year\" + \": \" + (format(datum[\"Year\"], \"\")) + \"; \" + \"Percentage\" + \": \" + (format(datum[\"sum_Frequency_end\"]-datum[\"sum_Frequency_start\"], \"%\"))"
          },
          "x": {"scale": "x", "field": "sum_Frequency_end"},
          "x2": {"scale": "x", "field": "sum_Frequency_start"},
          "yc": [
            {
              "test": "!isValid(datum[\"Year\"]) || !isFinite(+datum[\"Year\"])",
              "field": {"group": "height"}
            },
            {"scale": "y", "field": "Year"}
          ],
          "height": {"value": 4}
        }
      }
    }
  ],
  "scales": [
    {
      "name": "x",
      "type": "linear",
      "domain": [0, 1],
      "range": [0, {"signal": "width"}],
      "nice": true,
      "zero": true
    },
    {
      "name": "y",
      "type": "linear",
      "domain": {"data": "data_0", "field": "Year"},
      "domainRaw": {"signal": "selector018[\"Year\"]"},
      "range": [{"signal": "height"}, 0],
      "nice": true,
      "zero": false,
      "padding": 5
    },
    {
      "name": "color",
      "type": "ordinal",
      "domain": {"data": "data_0", "field": "Sex", "sort": true},
      "range": "category"
    }
  ],
  "axes": [
    {
      "scale": "y",
      "orient": "left",
      "gridScale": "x",
      "grid": true,
      "tickCount": {"signal": "ceil(height/40)"},
      "domain": false,
      "labels": false,
      "aria": false,
      "maxExtent": 0,
      "minExtent": 0,
      "ticks": false,
      "zindex": 0
    },
    {
      "scale": "x",
      "orient": "bottom",
      "grid": false,
      "title": "Percentage",
      "format": "%",
      "labelFlush": true,
      "labelOverlap": true,
      "tickCount": {"signal": "ceil(width/40)"},
      "zindex": 0
    },
    {
      "scale": "y",
      "orient": "left",
      "grid": false,
      "title": "Year",
      "labelOverlap": true,
      "tickCount": {"signal": "ceil(height/40)"},
      "zindex": 0
    }
  ],
  "legends": [{"fill": "color", "symbolType": "square", "title": "Sex"}],
  "config": {
    "legend": {
      "cornerRadius": 10,
      "fillColor": "#EEEEEE",
      "labelFontSize": 14,
      "padding": 10,
      "strokeColor": "gray"
    },
    "style": {"group-title": {"fontSize": 16}},
    "axis": {"labelFontSize": 14, "titleFontSize": 16}
  }
};
      vegaEmbed('#figure24', figure24);
</script>

<script type="text/javascript">
var figure25 = {
  "$schema": "https://vega.github.io/schema/vega/v5.json",
  "background": "white",
  "padding": 5,
  "width": 700,
  "height": 300,
  "title": {
    "text": "Changes in female athletes participation in Summer Olympics (1896-2016)",
    "frame": "group"
  },
  "style": "cell",
  "data": [
    {
      "name": "data-acf04d5a8ed5b056492542ad6eb1d357",
      "values": [
        {
          "Unnamed: 0": 0,
          "Year": 1896,
          "Sex": "M",
          "Frequency": 380,
          "Percentage_decimal": 1,
          "Percentage": "100.0%"
        },
        {
          "Unnamed: 0": 1,
          "Year": 1896,
          "Sex": "F",
          "Frequency": 0,
          "Percentage_decimal": 0,
          "Percentage": "0.0%"
        },
        {
          "Unnamed: 0": 2,
          "Year": 1900,
          "Sex": "M",
          "Frequency": 1903,
          "Percentage_decimal": 0.983,
          "Percentage": "98.3%"
        },
        {
          "Unnamed: 0": 3,
          "Year": 1900,
          "Sex": "F",
          "Frequency": 33,
          "Percentage_decimal": 0.017,
          "Percentage": "1.7%"
        },
        {
          "Unnamed: 0": 4,
          "Year": 1904,
          "Sex": "M",
          "Frequency": 1285,
          "Percentage_decimal": 0.988,
          "Percentage": "98.8%"
        },
        {
          "Unnamed: 0": 5,
          "Year": 1904,
          "Sex": "F",
          "Frequency": 16,
          "Percentage_decimal": 0.012,
          "Percentage": "1.2%"
        },
        {
          "Unnamed: 0": 6,
          "Year": 1906,
          "Sex": "M",
          "Frequency": 1722,
          "Percentage_decimal": 0.9940000000000001,
          "Percentage": "99.4%"
        },
        {
          "Unnamed: 0": 7,
          "Year": 1906,
          "Sex": "F",
          "Frequency": 11,
          "Percentage_decimal": 0.006,
          "Percentage": "0.6%"
        },
        {
          "Unnamed: 0": 8,
          "Year": 1908,
          "Sex": "M",
          "Frequency": 3054,
          "Percentage_decimal": 0.985,
          "Percentage": "98.5%"
        },
        {
          "Unnamed: 0": 9,
          "Year": 1908,
          "Sex": "F",
          "Frequency": 47,
          "Percentage_decimal": 0.015,
          "Percentage": "1.5%"
        },
        {
          "Unnamed: 0": 10,
          "Year": 1912,
          "Sex": "M",
          "Frequency": 3953,
          "Percentage_decimal": 0.978,
          "Percentage": "97.8%"
        },
        {
          "Unnamed: 0": 11,
          "Year": 1912,
          "Sex": "F",
          "Frequency": 87,
          "Percentage_decimal": 0.022000000000000002,
          "Percentage": "2.2%"
        },
        {
          "Unnamed: 0": 12,
          "Year": 1920,
          "Sex": "M",
          "Frequency": 4158,
          "Percentage_decimal": 0.9690000000000001,
          "Percentage": "96.9%"
        },
        {
          "Unnamed: 0": 13,
          "Year": 1920,
          "Sex": "F",
          "Frequency": 134,
          "Percentage_decimal": 0.031,
          "Percentage": "3.1%"
        },
        {
          "Unnamed: 0": 14,
          "Year": 1924,
          "Sex": "M",
          "Frequency": 4989,
          "Percentage_decimal": 0.953,
          "Percentage": "95.3%"
        },
        {
          "Unnamed: 0": 15,
          "Year": 1924,
          "Sex": "F",
          "Frequency": 244,
          "Percentage_decimal": 0.047,
          "Percentage": "4.7%"
        },
        {
          "Unnamed: 0": 16,
          "Year": 1928,
          "Sex": "M",
          "Frequency": 4588,
          "Percentage_decimal": 0.919,
          "Percentage": "91.9%"
        },
        {
          "Unnamed: 0": 17,
          "Year": 1928,
          "Sex": "F",
          "Frequency": 404,
          "Percentage_decimal": 0.081,
          "Percentage": "8.1%"
        },
        {
          "Unnamed: 0": 18,
          "Year": 1932,
          "Sex": "M",
          "Frequency": 2622,
          "Percentage_decimal": 0.883,
          "Percentage": "88.3%"
        },
        {
          "Unnamed: 0": 19,
          "Year": 1932,
          "Sex": "F",
          "Frequency": 347,
          "Percentage_decimal": 0.11699999999999999,
          "Percentage": "11.7%"
        },
        {
          "Unnamed: 0": 20,
          "Year": 1936,
          "Sex": "M",
          "Frequency": 6038,
          "Percentage_decimal": 0.9279999999999999,
          "Percentage": "92.8%"
        },
        {
          "Unnamed: 0": 21,
          "Year": 1936,
          "Sex": "F",
          "Frequency": 468,
          "Percentage_decimal": 0.07200000000000001,
          "Percentage": "7.2%"
        },
        {
          "Unnamed: 0": 22,
          "Year": 1948,
          "Sex": "M",
          "Frequency": 5777,
          "Percentage_decimal": 0.902,
          "Percentage": "90.2%"
        },
        {
          "Unnamed: 0": 23,
          "Year": 1948,
          "Sex": "F",
          "Frequency": 628,
          "Percentage_decimal": 0.098,
          "Percentage": "9.8%"
        },
        {
          "Unnamed: 0": 24,
          "Year": 1952,
          "Sex": "M",
          "Frequency": 6773,
          "Percentage_decimal": 0.8190000000000001,
          "Percentage": "81.9%"
        },
        {
          "Unnamed: 0": 25,
          "Year": 1952,
          "Sex": "F",
          "Frequency": 1497,
          "Percentage_decimal": 0.18100000000000002,
          "Percentage": "18.1%"
        },
        {
          "Unnamed: 0": 26,
          "Year": 1956,
          "Sex": "M",
          "Frequency": 4234,
          "Percentage_decimal": 0.826,
          "Percentage": "82.6%"
        },
        {
          "Unnamed: 0": 27,
          "Year": 1956,
          "Sex": "F",
          "Frequency": 893,
          "Percentage_decimal": 0.174,
          "Percentage": "17.4%"
        },
        {
          "Unnamed: 0": 28,
          "Year": 1960,
          "Sex": "M",
          "Frequency": 6684,
          "Percentage_decimal": 0.823,
          "Percentage": "82.3%"
        },
        {
          "Unnamed: 0": 29,
          "Year": 1960,
          "Sex": "F",
          "Frequency": 1435,
          "Percentage_decimal": 0.177,
          "Percentage": "17.7%"
        },
        {
          "Unnamed: 0": 30,
          "Year": 1964,
          "Sex": "M",
          "Frequency": 6354,
          "Percentage_decimal": 0.825,
          "Percentage": "82.5%"
        },
        {
          "Unnamed: 0": 31,
          "Year": 1964,
          "Sex": "F",
          "Frequency": 1348,
          "Percentage_decimal": 0.175,
          "Percentage": "17.5%"
        },
        {
          "Unnamed: 0": 32,
          "Year": 1968,
          "Sex": "M",
          "Frequency": 6811,
          "Percentage_decimal": 0.7929999999999999,
          "Percentage": "79.3%"
        },
        {
          "Unnamed: 0": 33,
          "Year": 1968,
          "Sex": "F",
          "Frequency": 1777,
          "Percentage_decimal": 0.207,
          "Percentage": "20.7%"
        },
        {
          "Unnamed: 0": 34,
          "Year": 1972,
          "Sex": "M",
          "Frequency": 8111,
          "Percentage_decimal": 0.787,
          "Percentage": "78.7%"
        },
        {
          "Unnamed: 0": 35,
          "Year": 1972,
          "Sex": "F",
          "Frequency": 2193,
          "Percentage_decimal": 0.213,
          "Percentage": "21.3%"
        },
        {
          "Unnamed: 0": 36,
          "Year": 1976,
          "Sex": "M",
          "Frequency": 6469,
          "Percentage_decimal": 0.7490000000000001,
          "Percentage": "74.9%"
        },
        {
          "Unnamed: 0": 37,
          "Year": 1976,
          "Sex": "F",
          "Frequency": 2172,
          "Percentage_decimal": 0.251,
          "Percentage": "25.1%"
        },
        {
          "Unnamed: 0": 38,
          "Year": 1980,
          "Sex": "M",
          "Frequency": 5435,
          "Percentage_decimal": 0.7559999999999999,
          "Percentage": "75.6%"
        },
        {
          "Unnamed: 0": 39,
          "Year": 1980,
          "Sex": "F",
          "Frequency": 1756,
          "Percentage_decimal": 0.244,
          "Percentage": "24.4%"
        },
        {
          "Unnamed: 0": 40,
          "Year": 1984,
          "Sex": "M",
          "Frequency": 7007,
          "Percentage_decimal": 0.741,
          "Percentage": "74.1%"
        },
        {
          "Unnamed: 0": 41,
          "Year": 1984,
          "Sex": "F",
          "Frequency": 2447,
          "Percentage_decimal": 0.259,
          "Percentage": "25.9%"
        },
        {
          "Unnamed: 0": 42,
          "Year": 1988,
          "Sex": "M",
          "Frequency": 8494,
          "Percentage_decimal": 0.706,
          "Percentage": "70.6%"
        },
        {
          "Unnamed: 0": 43,
          "Year": 1988,
          "Sex": "F",
          "Frequency": 3543,
          "Percentage_decimal": 0.294,
          "Percentage": "29.4%"
        },
        {
          "Unnamed: 0": 44,
          "Year": 1992,
          "Sex": "M",
          "Frequency": 8853,
          "Percentage_decimal": 0.682,
          "Percentage": "68.2%"
        },
        {
          "Unnamed: 0": 45,
          "Year": 1992,
          "Sex": "F",
          "Frequency": 4124,
          "Percentage_decimal": 0.318,
          "Percentage": "31.8%"
        },
        {
          "Unnamed: 0": 46,
          "Year": 1996,
          "Sex": "M",
          "Frequency": 8772,
          "Percentage_decimal": 0.637,
          "Percentage": "63.7%"
        },
        {
          "Unnamed: 0": 47,
          "Year": 1996,
          "Sex": "F",
          "Frequency": 5008,
          "Percentage_decimal": 0.363,
          "Percentage": "36.3%"
        },
        {
          "Unnamed: 0": 48,
          "Year": 2000,
          "Sex": "M",
          "Frequency": 8390,
          "Percentage_decimal": 0.607,
          "Percentage": "60.7%"
        },
        {
          "Unnamed: 0": 49,
          "Year": 2000,
          "Sex": "F",
          "Frequency": 5431,
          "Percentage_decimal": 0.39299999999999996,
          "Percentage": "39.3%"
        },
        {
          "Unnamed: 0": 50,
          "Year": 2004,
          "Sex": "M",
          "Frequency": 7897,
          "Percentage_decimal": 0.5870000000000001,
          "Percentage": "58.7%"
        },
        {
          "Unnamed: 0": 51,
          "Year": 2004,
          "Sex": "F",
          "Frequency": 5546,
          "Percentage_decimal": 0.413,
          "Percentage": "41.3%"
        },
        {
          "Unnamed: 0": 52,
          "Year": 2008,
          "Sex": "M",
          "Frequency": 7786,
          "Percentage_decimal": 0.5720000000000001,
          "Percentage": "57.2%"
        },
        {
          "Unnamed: 0": 53,
          "Year": 2008,
          "Sex": "F",
          "Frequency": 5816,
          "Percentage_decimal": 0.428,
          "Percentage": "42.8%"
        },
        {
          "Unnamed: 0": 54,
          "Year": 2012,
          "Sex": "M",
          "Frequency": 7105,
          "Percentage_decimal": 0.55,
          "Percentage": "55.0%"
        },
        {
          "Unnamed: 0": 55,
          "Year": 2012,
          "Sex": "F",
          "Frequency": 5815,
          "Percentage_decimal": 0.45,
          "Percentage": "45.0%"
        },
        {
          "Unnamed: 0": 56,
          "Year": 2016,
          "Sex": "M",
          "Frequency": 7465,
          "Percentage_decimal": 0.545,
          "Percentage": "54.5%"
        },
        {
          "Unnamed: 0": 57,
          "Year": 2016,
          "Sex": "F",
          "Frequency": 6223,
          "Percentage_decimal": 0.455,
          "Percentage": "45.5%"
        }
      ]
    },
    {
      "name": "data-4be4e5362f7ec640992a51633fcaf211",
      "values": [
        {
          "Unnamed: 0": 1,
          "Year": 1896,
          "Sex": "F",
          "Frequency": 0,
          "Percentage_decimal": 0,
          "Percentage": "0.0%"
        },
        {
          "Unnamed: 0": 3,
          "Year": 1900,
          "Sex": "F",
          "Frequency": 33,
          "Percentage_decimal": 0.017,
          "Percentage": "1.7%"
        },
        {
          "Unnamed: 0": 5,
          "Year": 1904,
          "Sex": "F",
          "Frequency": 16,
          "Percentage_decimal": 0.012,
          "Percentage": "1.2%"
        },
        {
          "Unnamed: 0": 7,
          "Year": 1906,
          "Sex": "F",
          "Frequency": 11,
          "Percentage_decimal": 0.006,
          "Percentage": "0.6%"
        },
        {
          "Unnamed: 0": 9,
          "Year": 1908,
          "Sex": "F",
          "Frequency": 47,
          "Percentage_decimal": 0.015,
          "Percentage": "1.5%"
        },
        {
          "Unnamed: 0": 11,
          "Year": 1912,
          "Sex": "F",
          "Frequency": 87,
          "Percentage_decimal": 0.022000000000000002,
          "Percentage": "2.2%"
        },
        {
          "Unnamed: 0": 13,
          "Year": 1920,
          "Sex": "F",
          "Frequency": 134,
          "Percentage_decimal": 0.031,
          "Percentage": "3.1%"
        },
        {
          "Unnamed: 0": 15,
          "Year": 1924,
          "Sex": "F",
          "Frequency": 244,
          "Percentage_decimal": 0.047,
          "Percentage": "4.7%"
        },
        {
          "Unnamed: 0": 17,
          "Year": 1928,
          "Sex": "F",
          "Frequency": 404,
          "Percentage_decimal": 0.081,
          "Percentage": "8.1%"
        },
        {
          "Unnamed: 0": 19,
          "Year": 1932,
          "Sex": "F",
          "Frequency": 347,
          "Percentage_decimal": 0.11699999999999999,
          "Percentage": "11.7%"
        },
        {
          "Unnamed: 0": 21,
          "Year": 1936,
          "Sex": "F",
          "Frequency": 468,
          "Percentage_decimal": 0.07200000000000001,
          "Percentage": "7.2%"
        },
        {
          "Unnamed: 0": 23,
          "Year": 1948,
          "Sex": "F",
          "Frequency": 628,
          "Percentage_decimal": 0.098,
          "Percentage": "9.8%"
        },
        {
          "Unnamed: 0": 25,
          "Year": 1952,
          "Sex": "F",
          "Frequency": 1497,
          "Percentage_decimal": 0.18100000000000002,
          "Percentage": "18.1%"
        },
        {
          "Unnamed: 0": 27,
          "Year": 1956,
          "Sex": "F",
          "Frequency": 893,
          "Percentage_decimal": 0.174,
          "Percentage": "17.4%"
        },
        {
          "Unnamed: 0": 29,
          "Year": 1960,
          "Sex": "F",
          "Frequency": 1435,
          "Percentage_decimal": 0.177,
          "Percentage": "17.7%"
        },
        {
          "Unnamed: 0": 31,
          "Year": 1964,
          "Sex": "F",
          "Frequency": 1348,
          "Percentage_decimal": 0.175,
          "Percentage": "17.5%"
        },
        {
          "Unnamed: 0": 33,
          "Year": 1968,
          "Sex": "F",
          "Frequency": 1777,
          "Percentage_decimal": 0.207,
          "Percentage": "20.7%"
        },
        {
          "Unnamed: 0": 35,
          "Year": 1972,
          "Sex": "F",
          "Frequency": 2193,
          "Percentage_decimal": 0.213,
          "Percentage": "21.3%"
        },
        {
          "Unnamed: 0": 37,
          "Year": 1976,
          "Sex": "F",
          "Frequency": 2172,
          "Percentage_decimal": 0.251,
          "Percentage": "25.1%"
        },
        {
          "Unnamed: 0": 39,
          "Year": 1980,
          "Sex": "F",
          "Frequency": 1756,
          "Percentage_decimal": 0.244,
          "Percentage": "24.4%"
        },
        {
          "Unnamed: 0": 41,
          "Year": 1984,
          "Sex": "F",
          "Frequency": 2447,
          "Percentage_decimal": 0.259,
          "Percentage": "25.9%"
        },
        {
          "Unnamed: 0": 43,
          "Year": 1988,
          "Sex": "F",
          "Frequency": 3543,
          "Percentage_decimal": 0.294,
          "Percentage": "29.4%"
        },
        {
          "Unnamed: 0": 45,
          "Year": 1992,
          "Sex": "F",
          "Frequency": 4124,
          "Percentage_decimal": 0.318,
          "Percentage": "31.8%"
        },
        {
          "Unnamed: 0": 47,
          "Year": 1996,
          "Sex": "F",
          "Frequency": 5008,
          "Percentage_decimal": 0.363,
          "Percentage": "36.3%"
        },
        {
          "Unnamed: 0": 49,
          "Year": 2000,
          "Sex": "F",
          "Frequency": 5431,
          "Percentage_decimal": 0.39299999999999996,
          "Percentage": "39.3%"
        },
        {
          "Unnamed: 0": 51,
          "Year": 2004,
          "Sex": "F",
          "Frequency": 5546,
          "Percentage_decimal": 0.413,
          "Percentage": "41.3%"
        },
        {
          "Unnamed: 0": 53,
          "Year": 2008,
          "Sex": "F",
          "Frequency": 5816,
          "Percentage_decimal": 0.428,
          "Percentage": "42.8%"
        },
        {
          "Unnamed: 0": 55,
          "Year": 2012,
          "Sex": "F",
          "Frequency": 5815,
          "Percentage_decimal": 0.45,
          "Percentage": "45.0%"
        },
        {
          "Unnamed: 0": 57,
          "Year": 2016,
          "Sex": "F",
          "Frequency": 6223,
          "Percentage_decimal": 0.455,
          "Percentage": "45.5%"
        }
      ]
    },
    {
      "name": "data_0",
      "source": "data-acf04d5a8ed5b056492542ad6eb1d357",
      "transform": [
        {
          "type": "aggregate",
          "groupby": ["Sex", "Year", "Percentage"],
          "ops": ["sum"],
          "fields": ["Frequency"],
          "as": ["sum_Frequency"]
        },
        {
          "type": "stack",
          "groupby": ["Year"],
          "field": "sum_Frequency",
          "sort": {"field": ["Sex"], "order": ["ascending"]},
          "as": ["sum_Frequency_start", "sum_Frequency_end"],
          "offset": "normalize"
        },
        {
          "type": "filter",
          "expr": "isValid(datum[\"Year\"]) && isFinite(+datum[\"Year\"]) && isValid(datum[\"sum_Frequency\"]) && isFinite(+datum[\"sum_Frequency\"])"
        }
      ]
    },
    {
      "name": "data_1",
      "source": "data-4be4e5362f7ec640992a51633fcaf211",
      "transform": [
        {"type": "formula", "expr": "toNumber(datum[\"Year\"])", "as": "Year"}
      ]
    },
    {
      "name": "data_2",
      "source": "data_1",
      "transform": [
        {
          "type": "filter",
          "expr": "isValid(datum[\"Year\"]) && isFinite(+datum[\"Year\"]) && isValid(datum[\"Percentage_decimal\"]) && isFinite(+datum[\"Percentage_decimal\"])"
        }
      ]
    }
  ],
  "marks": [
    {
      "name": "layer_0_layer_0_marks",
      "type": "rect",
      "style": ["bar"],
      "from": {"data": "data_0"},
      "encode": {
        "update": {
          "fill": {"scale": "color", "field": "Sex"},
          "tooltip": {
            "signal": "{\"Year\": format(datum[\"Year\"], \"\"), \"Sex\": isValid(datum[\"Sex\"]) ? datum[\"Sex\"] : \"\"+datum[\"Sex\"], \"Percentage\": isValid(datum[\"Percentage\"]) ? datum[\"Percentage\"] : \"\"+datum[\"Percentage\"]}"
          },
          "ariaRoleDescription": {"value": "bar"},
          "description": {
            "signal": "\"Sex\" + \": \" + (isValid(datum[\"Sex\"]) ? datum[\"Sex\"] : \"\"+datum[\"Sex\"]) + \"; \" + \"Year\" + \": \" + (format(datum[\"Year\"], \"\")) + \"; \" + \"Percentage\" + \": \" + (format(datum[\"sum_Frequency_end\"]-datum[\"sum_Frequency_start\"], \"%\"))"
          },
          "xc": [
            {
              "test": "!isValid(datum[\"Year\"]) || !isFinite(+datum[\"Year\"])",
              "value": 0
            },
            {"scale": "x", "field": "Year"}
          ],
          "width": {"value": 10},
          "y": {"scale": "y", "field": "sum_Frequency_end"},
          "y2": {"scale": "y", "field": "sum_Frequency_start"}
        }
      }
    },
    {
      "name": "layer_0_layer_1_layer_0_marks",
      "type": "line",
      "style": ["line"],
      "sort": {"field": "datum[\"Year\"]"},
      "from": {"data": "data_1"},
      "encode": {
        "update": {
          "stroke": {"value": "red"},
          "description": {
            "signal": "\"Year\" + \": \" + (format(datum[\"Year\"], \"\")) + \"; \" + \"Percentage_decimal\" + \": \" + (format(datum[\"Percentage_decimal\"], \"\"))"
          },
          "x": {"scale": "x", "field": "Year"},
          "y": {"scale": "y", "field": "Percentage_decimal"},
          "defined": {
            "signal": "isValid(datum[\"Year\"]) && isFinite(+datum[\"Year\"]) && isValid(datum[\"Percentage_decimal\"]) && isFinite(+datum[\"Percentage_decimal\"])"
          }
        }
      }
    },
    {
      "name": "layer_0_layer_1_layer_1_marks",
      "type": "symbol",
      "style": ["point"],
      "from": {"data": "data_2"},
      "encode": {
        "update": {
          "opacity": {"value": 1},
          "fill": {"value": "#4c78a8"},
          "ariaRoleDescription": {"value": "point"},
          "description": {
            "signal": "\"Year\" + \": \" + (format(datum[\"Year\"], \"\")) + \"; \" + \"Percentage_decimal\" + \": \" + (format(datum[\"Percentage_decimal\"], \"\"))"
          },
          "x": [
            {
              "test": "!isValid(datum[\"Year\"]) || !isFinite(+datum[\"Year\"])",
              "value": 0
            },
            {"scale": "x", "field": "Year"}
          ],
          "y": {"scale": "y", "field": "Percentage_decimal"}
        }
      }
    }
  ],
  "scales": [
    {
      "name": "x",
      "type": "linear",
      "domain": {
        "fields": [
          {"data": "data_0", "field": "Year"},
          {"data": "data_1", "field": "Year"},
          {"data": "data_2", "field": "Year"}
        ]
      },
      "range": [0, {"signal": "width"}],
      "nice": true,
      "zero": false,
      "padding": 5
    },
    {
      "name": "y",
      "type": "linear",
      "domain": {
        "fields": [
          [0, 1],
          {"data": "data_1", "field": "Percentage_decimal"},
          {"data": "data_2", "field": "Percentage_decimal"}
        ]
      },
      "range": [{"signal": "height"}, 0],
      "nice": true,
      "zero": true
    },
    {
      "name": "color",
      "type": "ordinal",
      "domain": ["F", "M"],
      "range": ["blue", "grey"]
    }
  ],
  "axes": [
    {
      "scale": "x",
      "orient": "bottom",
      "gridScale": "y",
      "grid": true,
      "tickCount": {"signal": "ceil(width/40)"},
      "domain": false,
      "labels": false,
      "aria": false,
      "maxExtent": 0,
      "minExtent": 0,
      "ticks": false,
      "zindex": 0
    },
    {
      "scale": "x",
      "orient": "bottom",
      "grid": false,
      "title": "Year",
      "labelFlush": true,
      "labelOverlap": true,
      "tickCount": {"signal": "ceil(width/40)"},
      "zindex": 0
    },
    {
      "scale": "y",
      "orient": "left",
      "grid": false,
      "title": "Percentage",
      "format": "%",
      "labelOverlap": true,
      "tickCount": {"signal": "ceil(height/40)"},
      "zindex": 0
    }
  ],
  "legends": [{"fill": "color", "symbolType": "square", "title": "Sex"}],
  "config": {
    "legend": {
      "cornerRadius": 10,
      "fillColor": "#EEEEEE",
      "labelFontSize": 14,
      "padding": 10,
      "strokeColor": "gray"
    },
    "style": {"group-title": {"fontSize": 20}},
    "axis": {"labelFontSize": 14, "titleFontSize": 16}
  }
};
vegaEmbed('#figure25', figure25);
</script>

<script type="text/javascript">
var figure26 = {
  "$schema": "https://vega.github.io/schema/vega/v5.json",
  "background": "white",
  "padding": 5,
  "width": 700,
  "height": 300,
  "title": {
    "text": "Changes in female athletes participation in Summer Olympics (1896-2016)",
    "frame": "group"
  },
  "style": "cell",
  "data": [
    {"name": "selector019_store"},
    {
      "name": "data-acf04d5a8ed5b056492542ad6eb1d357",
      "values": [
        {
          "Unnamed: 0": 0,
          "Year": 1896,
          "Sex": "M",
          "Frequency": 380,
          "Percentage_decimal": 1,
          "Percentage": "100.0%"
        },
        {
          "Unnamed: 0": 1,
          "Year": 1896,
          "Sex": "F",
          "Frequency": 0,
          "Percentage_decimal": 0,
          "Percentage": "0.0%"
        },
        {
          "Unnamed: 0": 2,
          "Year": 1900,
          "Sex": "M",
          "Frequency": 1903,
          "Percentage_decimal": 0.983,
          "Percentage": "98.3%"
        },
        {
          "Unnamed: 0": 3,
          "Year": 1900,
          "Sex": "F",
          "Frequency": 33,
          "Percentage_decimal": 0.017,
          "Percentage": "1.7%"
        },
        {
          "Unnamed: 0": 4,
          "Year": 1904,
          "Sex": "M",
          "Frequency": 1285,
          "Percentage_decimal": 0.988,
          "Percentage": "98.8%"
        },
        {
          "Unnamed: 0": 5,
          "Year": 1904,
          "Sex": "F",
          "Frequency": 16,
          "Percentage_decimal": 0.012,
          "Percentage": "1.2%"
        },
        {
          "Unnamed: 0": 6,
          "Year": 1906,
          "Sex": "M",
          "Frequency": 1722,
          "Percentage_decimal": 0.9940000000000001,
          "Percentage": "99.4%"
        },
        {
          "Unnamed: 0": 7,
          "Year": 1906,
          "Sex": "F",
          "Frequency": 11,
          "Percentage_decimal": 0.006,
          "Percentage": "0.6%"
        },
        {
          "Unnamed: 0": 8,
          "Year": 1908,
          "Sex": "M",
          "Frequency": 3054,
          "Percentage_decimal": 0.985,
          "Percentage": "98.5%"
        },
        {
          "Unnamed: 0": 9,
          "Year": 1908,
          "Sex": "F",
          "Frequency": 47,
          "Percentage_decimal": 0.015,
          "Percentage": "1.5%"
        },
        {
          "Unnamed: 0": 10,
          "Year": 1912,
          "Sex": "M",
          "Frequency": 3953,
          "Percentage_decimal": 0.978,
          "Percentage": "97.8%"
        },
        {
          "Unnamed: 0": 11,
          "Year": 1912,
          "Sex": "F",
          "Frequency": 87,
          "Percentage_decimal": 0.022000000000000002,
          "Percentage": "2.2%"
        },
        {
          "Unnamed: 0": 12,
          "Year": 1920,
          "Sex": "M",
          "Frequency": 4158,
          "Percentage_decimal": 0.9690000000000001,
          "Percentage": "96.9%"
        },
        {
          "Unnamed: 0": 13,
          "Year": 1920,
          "Sex": "F",
          "Frequency": 134,
          "Percentage_decimal": 0.031,
          "Percentage": "3.1%"
        },
        {
          "Unnamed: 0": 14,
          "Year": 1924,
          "Sex": "M",
          "Frequency": 4989,
          "Percentage_decimal": 0.953,
          "Percentage": "95.3%"
        },
        {
          "Unnamed: 0": 15,
          "Year": 1924,
          "Sex": "F",
          "Frequency": 244,
          "Percentage_decimal": 0.047,
          "Percentage": "4.7%"
        },
        {
          "Unnamed: 0": 16,
          "Year": 1928,
          "Sex": "M",
          "Frequency": 4588,
          "Percentage_decimal": 0.919,
          "Percentage": "91.9%"
        },
        {
          "Unnamed: 0": 17,
          "Year": 1928,
          "Sex": "F",
          "Frequency": 404,
          "Percentage_decimal": 0.081,
          "Percentage": "8.1%"
        },
        {
          "Unnamed: 0": 18,
          "Year": 1932,
          "Sex": "M",
          "Frequency": 2622,
          "Percentage_decimal": 0.883,
          "Percentage": "88.3%"
        },
        {
          "Unnamed: 0": 19,
          "Year": 1932,
          "Sex": "F",
          "Frequency": 347,
          "Percentage_decimal": 0.11699999999999999,
          "Percentage": "11.7%"
        },
        {
          "Unnamed: 0": 20,
          "Year": 1936,
          "Sex": "M",
          "Frequency": 6038,
          "Percentage_decimal": 0.9279999999999999,
          "Percentage": "92.8%"
        },
        {
          "Unnamed: 0": 21,
          "Year": 1936,
          "Sex": "F",
          "Frequency": 468,
          "Percentage_decimal": 0.07200000000000001,
          "Percentage": "7.2%"
        },
        {
          "Unnamed: 0": 22,
          "Year": 1948,
          "Sex": "M",
          "Frequency": 5777,
          "Percentage_decimal": 0.902,
          "Percentage": "90.2%"
        },
        {
          "Unnamed: 0": 23,
          "Year": 1948,
          "Sex": "F",
          "Frequency": 628,
          "Percentage_decimal": 0.098,
          "Percentage": "9.8%"
        },
        {
          "Unnamed: 0": 24,
          "Year": 1952,
          "Sex": "M",
          "Frequency": 6773,
          "Percentage_decimal": 0.8190000000000001,
          "Percentage": "81.9%"
        },
        {
          "Unnamed: 0": 25,
          "Year": 1952,
          "Sex": "F",
          "Frequency": 1497,
          "Percentage_decimal": 0.18100000000000002,
          "Percentage": "18.1%"
        },
        {
          "Unnamed: 0": 26,
          "Year": 1956,
          "Sex": "M",
          "Frequency": 4234,
          "Percentage_decimal": 0.826,
          "Percentage": "82.6%"
        },
        {
          "Unnamed: 0": 27,
          "Year": 1956,
          "Sex": "F",
          "Frequency": 893,
          "Percentage_decimal": 0.174,
          "Percentage": "17.4%"
        },
        {
          "Unnamed: 0": 28,
          "Year": 1960,
          "Sex": "M",
          "Frequency": 6684,
          "Percentage_decimal": 0.823,
          "Percentage": "82.3%"
        },
        {
          "Unnamed: 0": 29,
          "Year": 1960,
          "Sex": "F",
          "Frequency": 1435,
          "Percentage_decimal": 0.177,
          "Percentage": "17.7%"
        },
        {
          "Unnamed: 0": 30,
          "Year": 1964,
          "Sex": "M",
          "Frequency": 6354,
          "Percentage_decimal": 0.825,
          "Percentage": "82.5%"
        },
        {
          "Unnamed: 0": 31,
          "Year": 1964,
          "Sex": "F",
          "Frequency": 1348,
          "Percentage_decimal": 0.175,
          "Percentage": "17.5%"
        },
        {
          "Unnamed: 0": 32,
          "Year": 1968,
          "Sex": "M",
          "Frequency": 6811,
          "Percentage_decimal": 0.7929999999999999,
          "Percentage": "79.3%"
        },
        {
          "Unnamed: 0": 33,
          "Year": 1968,
          "Sex": "F",
          "Frequency": 1777,
          "Percentage_decimal": 0.207,
          "Percentage": "20.7%"
        },
        {
          "Unnamed: 0": 34,
          "Year": 1972,
          "Sex": "M",
          "Frequency": 8111,
          "Percentage_decimal": 0.787,
          "Percentage": "78.7%"
        },
        {
          "Unnamed: 0": 35,
          "Year": 1972,
          "Sex": "F",
          "Frequency": 2193,
          "Percentage_decimal": 0.213,
          "Percentage": "21.3%"
        },
        {
          "Unnamed: 0": 36,
          "Year": 1976,
          "Sex": "M",
          "Frequency": 6469,
          "Percentage_decimal": 0.7490000000000001,
          "Percentage": "74.9%"
        },
        {
          "Unnamed: 0": 37,
          "Year": 1976,
          "Sex": "F",
          "Frequency": 2172,
          "Percentage_decimal": 0.251,
          "Percentage": "25.1%"
        },
        {
          "Unnamed: 0": 38,
          "Year": 1980,
          "Sex": "M",
          "Frequency": 5435,
          "Percentage_decimal": 0.7559999999999999,
          "Percentage": "75.6%"
        },
        {
          "Unnamed: 0": 39,
          "Year": 1980,
          "Sex": "F",
          "Frequency": 1756,
          "Percentage_decimal": 0.244,
          "Percentage": "24.4%"
        },
        {
          "Unnamed: 0": 40,
          "Year": 1984,
          "Sex": "M",
          "Frequency": 7007,
          "Percentage_decimal": 0.741,
          "Percentage": "74.1%"
        },
        {
          "Unnamed: 0": 41,
          "Year": 1984,
          "Sex": "F",
          "Frequency": 2447,
          "Percentage_decimal": 0.259,
          "Percentage": "25.9%"
        },
        {
          "Unnamed: 0": 42,
          "Year": 1988,
          "Sex": "M",
          "Frequency": 8494,
          "Percentage_decimal": 0.706,
          "Percentage": "70.6%"
        },
        {
          "Unnamed: 0": 43,
          "Year": 1988,
          "Sex": "F",
          "Frequency": 3543,
          "Percentage_decimal": 0.294,
          "Percentage": "29.4%"
        },
        {
          "Unnamed: 0": 44,
          "Year": 1992,
          "Sex": "M",
          "Frequency": 8853,
          "Percentage_decimal": 0.682,
          "Percentage": "68.2%"
        },
        {
          "Unnamed: 0": 45,
          "Year": 1992,
          "Sex": "F",
          "Frequency": 4124,
          "Percentage_decimal": 0.318,
          "Percentage": "31.8%"
        },
        {
          "Unnamed: 0": 46,
          "Year": 1996,
          "Sex": "M",
          "Frequency": 8772,
          "Percentage_decimal": 0.637,
          "Percentage": "63.7%"
        },
        {
          "Unnamed: 0": 47,
          "Year": 1996,
          "Sex": "F",
          "Frequency": 5008,
          "Percentage_decimal": 0.363,
          "Percentage": "36.3%"
        },
        {
          "Unnamed: 0": 48,
          "Year": 2000,
          "Sex": "M",
          "Frequency": 8390,
          "Percentage_decimal": 0.607,
          "Percentage": "60.7%"
        },
        {
          "Unnamed: 0": 49,
          "Year": 2000,
          "Sex": "F",
          "Frequency": 5431,
          "Percentage_decimal": 0.39299999999999996,
          "Percentage": "39.3%"
        },
        {
          "Unnamed: 0": 50,
          "Year": 2004,
          "Sex": "M",
          "Frequency": 7897,
          "Percentage_decimal": 0.5870000000000001,
          "Percentage": "58.7%"
        },
        {
          "Unnamed: 0": 51,
          "Year": 2004,
          "Sex": "F",
          "Frequency": 5546,
          "Percentage_decimal": 0.413,
          "Percentage": "41.3%"
        },
        {
          "Unnamed: 0": 52,
          "Year": 2008,
          "Sex": "M",
          "Frequency": 7786,
          "Percentage_decimal": 0.5720000000000001,
          "Percentage": "57.2%"
        },
        {
          "Unnamed: 0": 53,
          "Year": 2008,
          "Sex": "F",
          "Frequency": 5816,
          "Percentage_decimal": 0.428,
          "Percentage": "42.8%"
        },
        {
          "Unnamed: 0": 54,
          "Year": 2012,
          "Sex": "M",
          "Frequency": 7105,
          "Percentage_decimal": 0.55,
          "Percentage": "55.0%"
        },
        {
          "Unnamed: 0": 55,
          "Year": 2012,
          "Sex": "F",
          "Frequency": 5815,
          "Percentage_decimal": 0.45,
          "Percentage": "45.0%"
        },
        {
          "Unnamed: 0": 56,
          "Year": 2016,
          "Sex": "M",
          "Frequency": 7465,
          "Percentage_decimal": 0.545,
          "Percentage": "54.5%"
        },
        {
          "Unnamed: 0": 57,
          "Year": 2016,
          "Sex": "F",
          "Frequency": 6223,
          "Percentage_decimal": 0.455,
          "Percentage": "45.5%"
        }
      ]
    },
    {
      "name": "data_0",
      "source": "data-acf04d5a8ed5b056492542ad6eb1d357",
      "transform": [
        {"type": "formula", "expr": "toNumber(datum[\"Year\"])", "as": "Year"},
        {
          "type": "aggregate",
          "groupby": ["Sex", "Year", "Percentage"],
          "ops": ["sum"],
          "fields": ["Frequency"],
          "as": ["sum_Frequency"]
        },
        {
          "type": "impute",
          "field": "sum_Frequency",
          "groupby": ["Sex"],
          "key": "Year",
          "method": "value",
          "value": 0
        },
        {
          "type": "stack",
          "groupby": ["Year"],
          "field": "sum_Frequency",
          "sort": {"field": ["Sex"], "order": ["descending"]},
          "as": ["sum_Frequency_start", "sum_Frequency_end"],
          "offset": "zero"
        }
      ]
    }
  ],
  "signals": [
    {
      "name": "unit",
      "value": {},
      "on": [
        {"events": "mousemove", "update": "isTuple(group()) ? group() : unit"}
      ]
    },
    {
      "name": "selector019",
      "update": "vlSelectionResolve(\"selector019_store\", \"union\")"
    },
    {
      "name": "selector019_Year",
      "on": [
        {
          "events": {"signal": "selector019_translate_delta"},
          "update": "panLinear(selector019_translate_anchor.extent_x, -selector019_translate_delta.x / width)"
        },
        {
          "events": {"signal": "selector019_zoom_delta"},
          "update": "zoomLinear(domain(\"x\"), selector019_zoom_anchor.x, selector019_zoom_delta)"
        },
        {"events": [{"source": "scope", "type": "dblclick"}], "update": "null"}
      ]
    },
    {
      "name": "selector019_tuple",
      "on": [
        {
          "events": [{"signal": "selector019_Year"}],
          "update": "selector019_Year ? {unit: \"\", fields: selector019_tuple_fields, values: [selector019_Year]} : null"
        }
      ]
    },
    {
      "name": "selector019_tuple_fields",
      "value": [{"field": "Year", "channel": "x", "type": "R"}]
    },
    {
      "name": "selector019_translate_anchor",
      "value": {},
      "on": [
        {
          "events": [{"source": "scope", "type": "mousedown"}],
          "update": "{x: x(unit), y: y(unit), extent_x: domain(\"x\")}"
        }
      ]
    },
    {
      "name": "selector019_translate_delta",
      "value": {},
      "on": [
        {
          "events": [
            {
              "source": "window",
              "type": "mousemove",
              "consume": true,
              "between": [
                {"source": "scope", "type": "mousedown"},
                {"source": "window", "type": "mouseup"}
              ]
            }
          ],
          "update": "{x: selector019_translate_anchor.x - x(unit), y: selector019_translate_anchor.y - y(unit)}"
        }
      ]
    },
    {
      "name": "selector019_zoom_anchor",
      "on": [
        {
          "events": [{"source": "scope", "type": "wheel", "consume": true}],
          "update": "{x: invert(\"x\", x(unit)), y: invert(\"y\", y(unit))}"
        }
      ]
    },
    {
      "name": "selector019_zoom_delta",
      "on": [
        {
          "events": [{"source": "scope", "type": "wheel", "consume": true}],
          "force": true,
          "update": "pow(1.001, event.deltaY * pow(16, event.deltaMode))"
        }
      ]
    },
    {
      "name": "selector019_modify",
      "on": [
        {
          "events": {"signal": "selector019_tuple"},
          "update": "modify(\"selector019_store\", selector019_tuple, true)"
        }
      ]
    }
  ],
  "marks": [
    {
      "name": "pathgroup",
      "type": "group",
      "from": {
        "facet": {
          "name": "faceted_path_main",
          "data": "data_0",
          "groupby": ["Sex"]
        }
      },
      "encode": {
        "update": {
          "width": {"field": {"group": "width"}},
          "height": {"field": {"group": "height"}}
        }
      },
      "marks": [
        {
          "name": "marks",
          "type": "area",
          "clip": true,
          "style": ["area"],
          "sort": {"field": "datum[\"Year\"]"},
          "interactive": true,
          "from": {"data": "faceted_path_main"},
          "encode": {
            "update": {
              "orient": {"value": "vertical"},
              "fill": {"scale": "color", "field": "Sex"},
              "tooltip": {
                "signal": "{\"Year\": format(datum[\"Year\"], \"\"), \"Sex\": isValid(datum[\"Sex\"]) ? datum[\"Sex\"] : \"\"+datum[\"Sex\"], \"Percentage\": isValid(datum[\"Percentage\"]) ? datum[\"Percentage\"] : \"\"+datum[\"Percentage\"]}"
              },
              "description": {
                "signal": "\"Sex\" + \": \" + (isValid(datum[\"Sex\"]) ? datum[\"Sex\"] : \"\"+datum[\"Sex\"]) + \"; \" + \"Year\" + \": \" + (format(datum[\"Year\"], \"\")) + \"; \" + \"Percentage\" + \": \" + (isValid(datum[\"Percentage\"]) ? datum[\"Percentage\"] : \"\"+datum[\"Percentage\"]) + \"; \" + \"Sum of Frequency\" + \": \" + (format(datum[\"sum_Frequency\"], \"\"))"
              },
              "x": {"scale": "x", "field": "Year"},
              "y": {"scale": "y", "field": "sum_Frequency_end"},
              "y2": {"scale": "y", "field": "sum_Frequency_start"},
              "defined": {
                "signal": "isValid(datum[\"Year\"]) && isFinite(+datum[\"Year\"]) && isValid(datum[\"sum_Frequency\"]) && isFinite(+datum[\"sum_Frequency\"])"
              }
            }
          }
        }
      ]
    }
  ],
  "scales": [
    {
      "name": "x",
      "type": "linear",
      "domain": {"data": "data_0", "field": "Year"},
      "domainRaw": {"signal": "selector019[\"Year\"]"},
      "range": [0, {"signal": "width"}],
      "nice": true,
      "zero": false
    },
    {
      "name": "y",
      "type": "linear",
      "domain": {
        "data": "data_0",
        "fields": ["sum_Frequency_start", "sum_Frequency_end"]
      },
      "range": [{"signal": "height"}, 0],
      "nice": true,
      "zero": true
    },
    {
      "name": "color",
      "type": "ordinal",
      "domain": {"data": "data_0", "field": "Sex", "sort": true},
      "range": "category"
    }
  ],
  "axes": [
    {
      "scale": "x",
      "orient": "bottom",
      "gridScale": "y",
      "grid": true,
      "tickCount": {"signal": "ceil(width/40)"},
      "domain": false,
      "labels": false,
      "aria": false,
      "maxExtent": 0,
      "minExtent": 0,
      "ticks": false,
      "zindex": 0
    },
    {
      "scale": "y",
      "orient": "left",
      "gridScale": "x",
      "grid": true,
      "tickCount": {"signal": "ceil(height/40)"},
      "domain": false,
      "labels": false,
      "aria": false,
      "maxExtent": 0,
      "minExtent": 0,
      "ticks": false,
      "zindex": 0
    },
    {
      "scale": "x",
      "orient": "bottom",
      "grid": false,
      "title": "Year",
      "labelFlush": true,
      "labelOverlap": true,
      "tickCount": {"signal": "ceil(width/40)"},
      "zindex": 0
    },
    {
      "scale": "y",
      "orient": "left",
      "grid": false,
      "title": "Sum of Frequency",
      "labelOverlap": true,
      "tickCount": {"signal": "ceil(height/40)"},
      "zindex": 0
    }
  ],
  "legends": [{"fill": "color", "symbolType": "circle", "title": "Sex"}],
  "config": {
    "legend": {
      "cornerRadius": 10,
      "fillColor": "#EEEEEE",
      "labelFontSize": 14,
      "padding": 10,
      "strokeColor": "gray"
    },
    "style": {"group-title": {"fontSize": 16}},
    "axis": {"labelFontSize": 14, "titleFontSize": 16}
  }
};

vegaEmbed('#figure26', figure26);
</script>

---

### Female Participation Across Continents
To visualize changes in female participation in each continent, we first used a simple line graph where we put all the continent together. The x-axis is time, and the y-axis is female participation. The legend shows the colors associated with the continents. See Figure 25.

<div id="figure27" class="vis"></div>
<div class="caption">Figure 25: Line graph for female participation by continent</div>

The graph was very messy. As there were six continents and one global average, we could not distinguish between the seven categories very easily. So we gave up this option. 

Then we tried a small multiple in which each continent and the global average were shown in simple line graphs. This chart showed every continent clearly but it was not very easy to make comparison. See Figure 26.

<!--
[**FIGURE 28 HERE**]

{{<figure src="/pics/g-2-2.png" caption="Line graph in small multiple for female participation by continent" style="min-width: 100%">}}

The above visualization was made by seaborn. It's not of high resolution, so we tried altair for:

-->

<div id="figure28_2" class="vis"></div>
<div class="caption">Figure 26: Line graph in small multiple for female participation by continent</div>

To make comparisons clearer, we decided to use area chart. We stacked each area chart each representing a continent along a vertical line. However, comparisons were still difficult. Most importantly, in terms of using color as the visual encoding, this graph has too many categories. Besides, it has red and green at the same time, and therefore is not accessible to colorblind populations. See Figure 27.

<!--

{{<figure src="/pics/g-2-3.png" caption="Area chart in small multiple for female participation by continent" style="min-width: 110%">}}

-->

<div id="figure29" class="vis"></div>
<div class="caption">Figure 27: Stacked bar chart for female participation by continent</div>

We then went back to small multiple. Since we cared about the comparison between each continent, we decided to plot every continent and the global average in each of the six graphs. We highlighted only one continent in each graph, setting all other continents grey in the background. It worked much better than out earlier attempts, but one drawback is that it did not allow comparison with the global average. See Figure 28.


{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis-data/master/output/vis/g-2-5.png"  caption="Figure 28: Line graph in small multiple for female participation by continent against all other groups" class="wide">}}


Finally, we decided to highlight the global average with a black line. This time, comparisons both between continents and with the global average were clear. See Figure 29.

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis-data/master/output/vis/g-2-6.png" class="wide" caption="Figure 29: Line graph in small multiple for female participation by continent against global statistics">}}

<script type="text/javascript">
var figure27 = {
  "$schema": "https://vega.github.io/schema/vega/v5.json",
  "background": "white",
  "padding": 5,
  "width": 700,
  "height": 300,
  "title": {
    "anchor": "middle",
    "text": "Changes in female athletes participation in Summer Olympics over time",
    "frame": "group"
  },
  "style": "cell",
  "data": [
    {"name": "selector010_store"},
    {
      "name": "data-c9cd4958aa454941ccfb344427499b56",
      "values": [
        {
          "Year": 1896,
          "Continent": "Global",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1900,
          "Continent": "Global",
          "Female_Percentage": 0.016045548654244308,
          "Female Percentage": "1.6%"
        },
        {
          "Year": 1904,
          "Continent": "Global",
          "Female_Percentage": 0.012307692307692308,
          "Female Percentage": "1.2%"
        },
        {
          "Year": 1906,
          "Continent": "Global",
          "Female_Percentage": 0.006489675516224189,
          "Female Percentage": "0.6%"
        },
        {
          "Year": 1908,
          "Continent": "Global",
          "Female_Percentage": 0.015568068896985756,
          "Female Percentage": "1.6%"
        },
        {
          "Year": 1912,
          "Continent": "Global",
          "Female_Percentage": 0.020242914979757085,
          "Female Percentage": "2.0%"
        },
        {
          "Year": 1920,
          "Continent": "Global",
          "Female_Percentage": 0.03247863247863248,
          "Female Percentage": "3.2%"
        },
        {
          "Year": 1924,
          "Continent": "Global",
          "Female_Percentage": 0.04917363803305448,
          "Female Percentage": "4.9%"
        },
        {
          "Year": 1928,
          "Continent": "Global",
          "Female_Percentage": 0.08397582829756199,
          "Female Percentage": "8.4%"
        },
        {
          "Year": 1932,
          "Continent": "Global",
          "Female_Percentage": 0.11859193438140808,
          "Female Percentage": "11.9%"
        },
        {
          "Year": 1936,
          "Continent": "Global",
          "Female_Percentage": 0.07177974434611603,
          "Female Percentage": "7.2%"
        },
        {
          "Year": 1948,
          "Continent": "Global",
          "Female_Percentage": 0.0974740932642487,
          "Female Percentage": "9.7%"
        },
        {
          "Year": 1952,
          "Continent": "Global",
          "Female_Percentage": 0.17301414581066374,
          "Female Percentage": "17.3%"
        },
        {
          "Year": 1956,
          "Continent": "Global",
          "Female_Percentage": 0.1704136690647482,
          "Female Percentage": "17.0%"
        },
        {
          "Year": 1960,
          "Continent": "Global",
          "Female_Percentage": 0.1761111111111111,
          "Female Percentage": "17.6%"
        },
        {
          "Year": 1964,
          "Continent": "Global",
          "Female_Percentage": 0.17183667580435724,
          "Female Percentage": "17.2%"
        },
        {
          "Year": 1968,
          "Continent": "Global",
          "Female_Percentage": 0.19755020652328728,
          "Female Percentage": "19.8%"
        },
        {
          "Year": 1972,
          "Continent": "Global",
          "Female_Percentage": 0.2010383965225791,
          "Female Percentage": "20.1%"
        },
        {
          "Year": 1976,
          "Continent": "Global",
          "Female_Percentage": 0.2333720592506535,
          "Female Percentage": "23.3%"
        },
        {
          "Year": 1980,
          "Continent": "Global",
          "Female_Percentage": 0.22398271516024487,
          "Female Percentage": "22.4%"
        },
        {
          "Year": 1984,
          "Continent": "Global",
          "Female_Percentage": 0.25244707489187346,
          "Female Percentage": "25.2%"
        },
        {
          "Year": 1988,
          "Continent": "Global",
          "Female_Percentage": 0.2830937035200793,
          "Female Percentage": "28.3%"
        },
        {
          "Year": 1992,
          "Continent": "Global",
          "Female_Percentage": 0.3129472457979697,
          "Female Percentage": "31.3%"
        },
        {
          "Year": 1996,
          "Continent": "Global",
          "Female_Percentage": 0.36325520654340493,
          "Female Percentage": "36.3%"
        },
        {
          "Year": 2000,
          "Continent": "Global",
          "Female_Percentage": 0.3939145299145299,
          "Female Percentage": "39.4%"
        },
        {
          "Year": 2004,
          "Continent": "Global",
          "Female_Percentage": 0.4132602893664841,
          "Female Percentage": "41.3%"
        },
        {
          "Year": 2008,
          "Continent": "Global",
          "Female_Percentage": 0.4284037558685446,
          "Female Percentage": "42.8%"
        },
        {
          "Year": 2012,
          "Continent": "Global",
          "Female_Percentage": 0.4500399100210435,
          "Female Percentage": "45.0%"
        },
        {
          "Year": 2016,
          "Continent": "Global",
          "Female_Percentage": 0.4535101729046594,
          "Female Percentage": "45.4%"
        },
        {
          "Year": 1896,
          "Continent": "Africa",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1900,
          "Continent": "Africa",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1904,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1906,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1908,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1912,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1920,
          "Continent": "Africa",
          "Female_Percentage": 0.01680672268907563,
          "Female Percentage": "1.7%"
        },
        {
          "Year": 1924,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1928,
          "Continent": "Africa",
          "Female_Percentage": 0.1411764705882353,
          "Female Percentage": "14.1%"
        },
        {
          "Year": 1932,
          "Continent": "Africa",
          "Female_Percentage": 0.25,
          "Female Percentage": "25.0%"
        },
        {
          "Year": 1936,
          "Continent": "Africa",
          "Female_Percentage": 0.1,
          "Female Percentage": "10.0%"
        },
        {
          "Year": 1948,
          "Continent": "Africa",
          "Female_Percentage": 0.009569377990430622,
          "Female Percentage": "1.0%"
        },
        {
          "Year": 1952,
          "Continent": "Africa",
          "Female_Percentage": 0.02735562310030395,
          "Female Percentage": "2.7%"
        },
        {
          "Year": 1956,
          "Continent": "Africa",
          "Female_Percentage": 0.0748663101604278,
          "Female Percentage": "7.5%"
        },
        {
          "Year": 1960,
          "Continent": "Africa",
          "Female_Percentage": 0.04456824512534819,
          "Female Percentage": "4.5%"
        },
        {
          "Year": 1964,
          "Continent": "Africa",
          "Female_Percentage": 0.045454545454545456,
          "Female Percentage": "4.5%"
        },
        {
          "Year": 1968,
          "Continent": "Africa",
          "Female_Percentage": 0.039886039886039885,
          "Female Percentage": "4.0%"
        },
        {
          "Year": 1972,
          "Continent": "Africa",
          "Female_Percentage": 0.056985294117647065,
          "Female Percentage": "5.7%"
        },
        {
          "Year": 1976,
          "Continent": "Africa",
          "Female_Percentage": 0.0707070707070707,
          "Female Percentage": "7.1%"
        },
        {
          "Year": 1980,
          "Continent": "Africa",
          "Female_Percentage": 0.1524590163934426,
          "Female Percentage": "15.2%"
        },
        {
          "Year": 1984,
          "Continent": "Africa",
          "Female_Percentage": 0.09419354838709676,
          "Female Percentage": "9.4%"
        },
        {
          "Year": 1988,
          "Continent": "Africa",
          "Female_Percentage": 0.13974799541809851,
          "Female Percentage": "14.0%"
        },
        {
          "Year": 1992,
          "Continent": "Africa",
          "Female_Percentage": 0.22341568206229864,
          "Female Percentage": "22.3%"
        },
        {
          "Year": 1996,
          "Continent": "Africa",
          "Female_Percentage": 0.2462077012835473,
          "Female Percentage": "24.6%"
        },
        {
          "Year": 2000,
          "Continent": "Africa",
          "Female_Percentage": 0.3296370967741936,
          "Female Percentage": "33.0%"
        },
        {
          "Year": 2004,
          "Continent": "Africa",
          "Female_Percentage": 0.33407572383073497,
          "Female Percentage": "33.4%"
        },
        {
          "Year": 2008,
          "Continent": "Africa",
          "Female_Percentage": 0.3874734607218684,
          "Female Percentage": "38.7%"
        },
        {
          "Year": 2012,
          "Continent": "Africa",
          "Female_Percentage": 0.399581589958159,
          "Female Percentage": "40.0%"
        },
        {
          "Year": 2016,
          "Continent": "Africa",
          "Female_Percentage": 0.3836772983114447,
          "Female Percentage": "38.4%"
        },
        {
          "Year": 1896,
          "Continent": "Asia",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1900,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1904,
          "Continent": "Asia",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1906,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1908,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1912,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1920,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1924,
          "Continent": "Asia",
          "Female_Percentage": 0.033707865168539325,
          "Female Percentage": "3.4%"
        },
        {
          "Year": 1928,
          "Continent": "Asia",
          "Female_Percentage": 0.015873015873015872,
          "Female Percentage": "1.6%"
        },
        {
          "Year": 1932,
          "Continent": "Asia",
          "Female_Percentage": 0.11203319502074688,
          "Female Percentage": "11.2%"
        },
        {
          "Year": 1936,
          "Continent": "Asia",
          "Female_Percentage": 0.057620817843866176,
          "Female Percentage": "5.8%"
        },
        {
          "Year": 1948,
          "Continent": "Asia",
          "Female_Percentage": 0.0069124423963133645,
          "Female Percentage": "0.7%"
        },
        {
          "Year": 1952,
          "Continent": "Asia",
          "Female_Percentage": 0.065439672801636,
          "Female Percentage": "6.5%"
        },
        {
          "Year": 1956,
          "Continent": "Asia",
          "Female_Percentage": 0.1060126582278481,
          "Female Percentage": "10.6%"
        },
        {
          "Year": 1960,
          "Continent": "Asia",
          "Female_Percentage": 0.129366106080207,
          "Female Percentage": "12.9%"
        },
        {
          "Year": 1964,
          "Continent": "Asia",
          "Female_Percentage": 0.14587593728698026,
          "Female Percentage": "14.6%"
        },
        {
          "Year": 1968,
          "Continent": "Asia",
          "Female_Percentage": 0.17119244391971666,
          "Female Percentage": "17.1%"
        },
        {
          "Year": 1972,
          "Continent": "Asia",
          "Female_Percentage": 0.14781746031746032,
          "Female Percentage": "14.8%"
        },
        {
          "Year": 1976,
          "Continent": "Asia",
          "Female_Percentage": 0.16761041902604756,
          "Female Percentage": "16.8%"
        },
        {
          "Year": 1980,
          "Continent": "Asia",
          "Female_Percentage": 0.1494661921708185,
          "Female Percentage": "14.9%"
        },
        {
          "Year": 1984,
          "Continent": "Asia",
          "Female_Percentage": 0.2409855769230769,
          "Female Percentage": "24.1%"
        },
        {
          "Year": 1988,
          "Continent": "Asia",
          "Female_Percentage": 0.3037466547725245,
          "Female Percentage": "30.4%"
        },
        {
          "Year": 1992,
          "Continent": "Asia",
          "Female_Percentage": 0.31186440677966104,
          "Female Percentage": "31.2%"
        },
        {
          "Year": 1996,
          "Continent": "Asia",
          "Female_Percentage": 0.3821571238348868,
          "Female Percentage": "38.2%"
        },
        {
          "Year": 2000,
          "Continent": "Asia",
          "Female_Percentage": 0.39642620780939775,
          "Female Percentage": "39.6%"
        },
        {
          "Year": 2004,
          "Continent": "Asia",
          "Female_Percentage": 0.4359058207979071,
          "Female Percentage": "43.6%"
        },
        {
          "Year": 2008,
          "Continent": "Asia",
          "Female_Percentage": 0.43423423423423424,
          "Female Percentage": "43.4%"
        },
        {
          "Year": 2012,
          "Continent": "Asia",
          "Female_Percentage": 0.4599396580623533,
          "Female Percentage": "46.0%"
        },
        {
          "Year": 2016,
          "Continent": "Asia",
          "Female_Percentage": 0.4653897849462366,
          "Female Percentage": "46.5%"
        },
        {
          "Year": 1896,
          "Continent": "Europe",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1900,
          "Continent": "Europe",
          "Female_Percentage": 0.012528473804100227,
          "Female Percentage": "1.3%"
        },
        {
          "Year": 1904,
          "Continent": "Europe",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1906,
          "Continent": "Europe",
          "Female_Percentage": 0.006905210295040804,
          "Female Percentage": "0.7%"
        },
        {
          "Year": 1908,
          "Continent": "Europe",
          "Female_Percentage": 0.01800076599004213,
          "Female Percentage": "1.8%"
        },
        {
          "Year": 1912,
          "Continent": "Europe",
          "Female_Percentage": 0.024897480960749854,
          "Female Percentage": "2.5%"
        },
        {
          "Year": 1920,
          "Continent": "Europe",
          "Female_Percentage": 0.03142943487458446,
          "Female Percentage": "3.1%"
        },
        {
          "Year": 1924,
          "Continent": "Europe",
          "Female_Percentage": 0.05149330587023687,
          "Female Percentage": "5.1%"
        },
        {
          "Year": 1928,
          "Continent": "Europe",
          "Female_Percentage": 0.0821664464993395,
          "Female Percentage": "8.2%"
        },
        {
          "Year": 1932,
          "Continent": "Europe",
          "Female_Percentage": 0.10588235294117647,
          "Female Percentage": "10.6%"
        },
        {
          "Year": 1936,
          "Continent": "Europe",
          "Female_Percentage": 0.06700091157702825,
          "Female Percentage": "6.7%"
        },
        {
          "Year": 1948,
          "Continent": "Europe",
          "Female_Percentage": 0.1073929961089494,
          "Female Percentage": "10.7%"
        },
        {
          "Year": 1952,
          "Continent": "Europe",
          "Female_Percentage": 0.20599325262949,
          "Female Percentage": "20.6%"
        },
        {
          "Year": 1956,
          "Continent": "Europe",
          "Female_Percentage": 0.20808451998162608,
          "Female Percentage": "20.8%"
        },
        {
          "Year": 1960,
          "Continent": "Europe",
          "Female_Percentage": 0.19808861859252824,
          "Female Percentage": "19.8%"
        },
        {
          "Year": 1964,
          "Continent": "Europe",
          "Female_Percentage": 0.19008009858287125,
          "Female Percentage": "19.0%"
        },
        {
          "Year": 1968,
          "Continent": "Europe",
          "Female_Percentage": 0.20454545454545456,
          "Female Percentage": "20.5%"
        },
        {
          "Year": 1972,
          "Continent": "Europe",
          "Female_Percentage": 0.22300968580203165,
          "Female Percentage": "22.3%"
        },
        {
          "Year": 1976,
          "Continent": "Europe",
          "Female_Percentage": 0.2362555720653789,
          "Female Percentage": "23.6%"
        },
        {
          "Year": 1980,
          "Continent": "Europe",
          "Female_Percentage": 0.257801108194809,
          "Female Percentage": "25.8%"
        },
        {
          "Year": 1984,
          "Continent": "Europe",
          "Female_Percentage": 0.2688271604938272,
          "Female Percentage": "26.9%"
        },
        {
          "Year": 1988,
          "Continent": "Europe",
          "Female_Percentage": 0.29081000743126084,
          "Female Percentage": "29.1%"
        },
        {
          "Year": 1992,
          "Continent": "Europe",
          "Female_Percentage": 0.3262682418346073,
          "Female Percentage": "32.6%"
        },
        {
          "Year": 1996,
          "Continent": "Europe",
          "Female_Percentage": 0.3664026677782409,
          "Female Percentage": "36.6%"
        },
        {
          "Year": 2000,
          "Continent": "Europe",
          "Female_Percentage": 0.38596989491621697,
          "Female Percentage": "38.6%"
        },
        {
          "Year": 2004,
          "Continent": "Europe",
          "Female_Percentage": 0.4022806004618938,
          "Female Percentage": "40.2%"
        },
        {
          "Year": 2008,
          "Continent": "Europe",
          "Female_Percentage": 0.4252481849162839,
          "Female Percentage": "42.5%"
        },
        {
          "Year": 2012,
          "Continent": "Europe",
          "Female_Percentage": 0.4477747502270663,
          "Female Percentage": "44.8%"
        },
        {
          "Year": 2016,
          "Continent": "Europe",
          "Female_Percentage": 0.4510353417406197,
          "Female Percentage": "45.1%"
        },
        {
          "Year": 1896,
          "Continent": "North America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1900,
          "Continent": "North America",
          "Female_Percentage": 0.05960264900662252,
          "Female Percentage": "6.0%"
        },
        {
          "Year": 1904,
          "Continent": "North America",
          "Female_Percentage": 0.013605442176870748,
          "Female Percentage": "1.4%"
        },
        {
          "Year": 1906,
          "Continent": "North America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1908,
          "Continent": "North America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1912,
          "Continent": "North America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1920,
          "Continent": "North America",
          "Female_Percentage": 0.03942652329749104,
          "Female Percentage": "3.9%"
        },
        {
          "Year": 1924,
          "Continent": "North America",
          "Female_Percentage": 0.05843071786310518,
          "Female Percentage": "5.8%"
        },
        {
          "Year": 1928,
          "Continent": "North America",
          "Female_Percentage": 0.11,
          "Female Percentage": "11.0%"
        },
        {
          "Year": 1932,
          "Continent": "North America",
          "Female_Percentage": 0.14641148325358852,
          "Female Percentage": "14.6%"
        },
        {
          "Year": 1936,
          "Continent": "North America",
          "Female_Percentage": 0.1221264367816092,
          "Female Percentage": "12.2%"
        },
        {
          "Year": 1948,
          "Continent": "North America",
          "Female_Percentage": 0.11932418162618795,
          "Female Percentage": "11.9%"
        },
        {
          "Year": 1952,
          "Continent": "North America",
          "Female_Percentage": 0.16042154566744732,
          "Female Percentage": "16.0%"
        },
        {
          "Year": 1956,
          "Continent": "North America",
          "Female_Percentage": 0.19484240687679086,
          "Female Percentage": "19.5%"
        },
        {
          "Year": 1960,
          "Continent": "North America",
          "Female_Percentage": 0.21568627450980396,
          "Female Percentage": "21.6%"
        },
        {
          "Year": 1964,
          "Continent": "North America",
          "Female_Percentage": 0.2101661779081134,
          "Female Percentage": "21.0%"
        },
        {
          "Year": 1968,
          "Continent": "North America",
          "Female_Percentage": 0.2272957889396245,
          "Female Percentage": "22.7%"
        },
        {
          "Year": 1972,
          "Continent": "North America",
          "Female_Percentage": 0.23755924170616116,
          "Female Percentage": "23.8%"
        },
        {
          "Year": 1976,
          "Continent": "North America",
          "Female_Percentage": 0.27378964941569284,
          "Female Percentage": "27.4%"
        },
        {
          "Year": 1980,
          "Continent": "North America",
          "Female_Percentage": 0.17372881355932204,
          "Female Percentage": "17.4%"
        },
        {
          "Year": 1984,
          "Continent": "North America",
          "Female_Percentage": 0.3223987698616094,
          "Female Percentage": "32.2%"
        },
        {
          "Year": 1988,
          "Continent": "North America",
          "Female_Percentage": 0.32998324958123953,
          "Female Percentage": "33.0%"
        },
        {
          "Year": 1992,
          "Continent": "North America",
          "Female_Percentage": 0.3336653386454183,
          "Female Percentage": "33.4%"
        },
        {
          "Year": 1996,
          "Continent": "North America",
          "Female_Percentage": 0.3953257086026852,
          "Female Percentage": "39.5%"
        },
        {
          "Year": 2000,
          "Continent": "North America",
          "Female_Percentage": 0.4241469816272966,
          "Female Percentage": "42.4%"
        },
        {
          "Year": 2004,
          "Continent": "North America",
          "Female_Percentage": 0.4470720720720721,
          "Female Percentage": "44.7%"
        },
        {
          "Year": 2008,
          "Continent": "North America",
          "Female_Percentage": 0.4338074398249453,
          "Female Percentage": "43.4%"
        },
        {
          "Year": 2012,
          "Continent": "North America",
          "Female_Percentage": 0.4791666666666667,
          "Female Percentage": "47.9%"
        },
        {
          "Year": 2016,
          "Continent": "North America",
          "Female_Percentage": 0.4955947136563877,
          "Female Percentage": "49.6%"
        },
        {
          "Year": 1896,
          "Continent": "Oceania",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1900,
          "Continent": "Oceania",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1904,
          "Continent": "Oceania",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1906,
          "Continent": "Oceania",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1908,
          "Continent": "Oceania",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1912,
          "Continent": "Oceania",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1920,
          "Continent": "Oceania",
          "Female_Percentage": 0.14285714285714285,
          "Female Percentage": "14.3%"
        },
        {
          "Year": 1924,
          "Continent": "Oceania",
          "Female_Percentage": 0.045454545454545456,
          "Female Percentage": "4.5%"
        },
        {
          "Year": 1928,
          "Continent": "Oceania",
          "Female_Percentage": 0.2857142857142857,
          "Female Percentage": "28.6%"
        },
        {
          "Year": 1932,
          "Continent": "Oceania",
          "Female_Percentage": 0.12244897959183673,
          "Female Percentage": "12.2%"
        },
        {
          "Year": 1936,
          "Continent": "Oceania",
          "Female_Percentage": 0.125,
          "Female Percentage": "12.5%"
        },
        {
          "Year": 1948,
          "Continent": "Oceania",
          "Female_Percentage": 0.17117117117117114,
          "Female Percentage": "17.1%"
        },
        {
          "Year": 1952,
          "Continent": "Oceania",
          "Female_Percentage": 0.1375,
          "Female Percentage": "13.8%"
        },
        {
          "Year": 1956,
          "Continent": "Oceania",
          "Female_Percentage": 0.1729957805907173,
          "Female Percentage": "17.3%"
        },
        {
          "Year": 1960,
          "Continent": "Oceania",
          "Female_Percentage": 0.18787878787878787,
          "Female Percentage": "18.8%"
        },
        {
          "Year": 1964,
          "Continent": "Oceania",
          "Female_Percentage": 0.2375,
          "Female Percentage": "23.8%"
        },
        {
          "Year": 1968,
          "Continent": "Oceania",
          "Female_Percentage": 0.25862068965517243,
          "Female Percentage": "25.9%"
        },
        {
          "Year": 1972,
          "Continent": "Oceania",
          "Female_Percentage": 0.2356020942408377,
          "Female Percentage": "23.6%"
        },
        {
          "Year": 1976,
          "Continent": "Oceania",
          "Female_Percentage": 0.2383419689119171,
          "Female Percentage": "23.8%"
        },
        {
          "Year": 1980,
          "Continent": "Oceania",
          "Female_Percentage": 0.29949238578680204,
          "Female Percentage": "29.9%"
        },
        {
          "Year": 1984,
          "Continent": "Oceania",
          "Female_Percentage": 0.2949640287769784,
          "Female Percentage": "29.5%"
        },
        {
          "Year": 1988,
          "Continent": "Oceania",
          "Female_Percentage": 0.2690972222222222,
          "Female Percentage": "26.9%"
        },
        {
          "Year": 1992,
          "Continent": "Oceania",
          "Female_Percentage": 0.3381712626995646,
          "Female Percentage": "33.8%"
        },
        {
          "Year": 1996,
          "Continent": "Oceania",
          "Female_Percentage": 0.3949801849405548,
          "Female Percentage": "39.5%"
        },
        {
          "Year": 2000,
          "Continent": "Oceania",
          "Female_Percentage": 0.4650934119960669,
          "Female Percentage": "46.5%"
        },
        {
          "Year": 2004,
          "Continent": "Oceania",
          "Female_Percentage": 0.4480286738351255,
          "Female Percentage": "44.8%"
        },
        {
          "Year": 2008,
          "Continent": "Oceania",
          "Female_Percentage": 0.4597839135654262,
          "Female Percentage": "46.0%"
        },
        {
          "Year": 2012,
          "Continent": "Oceania",
          "Female_Percentage": 0.4623115577889447,
          "Female Percentage": "46.2%"
        },
        {
          "Year": 2016,
          "Continent": "Oceania",
          "Female_Percentage": 0.4833141542002302,
          "Female Percentage": "48.3%"
        },
        {
          "Year": 1896,
          "Continent": "South America",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1900,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1904,
          "Continent": "South America",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1906,
          "Continent": "South America",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1908,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1912,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1920,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1924,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1928,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1932,
          "Continent": "South America",
          "Female_Percentage": 0.023809523809523808,
          "Female Percentage": "2.4%"
        },
        {
          "Year": 1936,
          "Continent": "South America",
          "Female_Percentage": 0.03205128205128205,
          "Female Percentage": "3.2%"
        },
        {
          "Year": 1948,
          "Continent": "South America",
          "Female_Percentage": 0.08225806451612902,
          "Female Percentage": "8.2%"
        },
        {
          "Year": 1952,
          "Continent": "South America",
          "Female_Percentage": 0.07068607068607069,
          "Female Percentage": "7.1%"
        },
        {
          "Year": 1956,
          "Continent": "South America",
          "Female_Percentage": 0.021428571428571432,
          "Female Percentage": "2.1%"
        },
        {
          "Year": 1960,
          "Continent": "South America",
          "Female_Percentage": 0.03523035230352303,
          "Female Percentage": "3.5%"
        },
        {
          "Year": 1964,
          "Continent": "South America",
          "Female_Percentage": 0.04132231404958678,
          "Female Percentage": "4.1%"
        },
        {
          "Year": 1968,
          "Continent": "South America",
          "Female_Percentage": 0.15560165975103735,
          "Female Percentage": "15.6%"
        },
        {
          "Year": 1972,
          "Continent": "South America",
          "Female_Percentage": 0.117096018735363,
          "Female Percentage": "11.7%"
        },
        {
          "Year": 1976,
          "Continent": "South America",
          "Female_Percentage": 0.2050561797752809,
          "Female Percentage": "20.5%"
        },
        {
          "Year": 1980,
          "Continent": "South America",
          "Female_Percentage": 0.14788732394366194,
          "Female Percentage": "14.8%"
        },
        {
          "Year": 1984,
          "Continent": "South America",
          "Female_Percentage": 0.13333333333333333,
          "Female Percentage": "13.3%"
        },
        {
          "Year": 1988,
          "Continent": "South America",
          "Female_Percentage": 0.2332155477031802,
          "Female Percentage": "23.3%"
        },
        {
          "Year": 1992,
          "Continent": "South America",
          "Female_Percentage": 0.2249560632688928,
          "Female Percentage": "22.5%"
        },
        {
          "Year": 1996,
          "Continent": "South America",
          "Female_Percentage": 0.2697095435684647,
          "Female Percentage": "27.0%"
        },
        {
          "Year": 2000,
          "Continent": "South America",
          "Female_Percentage": 0.366306027820711,
          "Female Percentage": "36.6%"
        },
        {
          "Year": 2004,
          "Continent": "South America",
          "Female_Percentage": 0.39811066126855604,
          "Female Percentage": "39.8%"
        },
        {
          "Year": 2008,
          "Continent": "South America",
          "Female_Percentage": 0.4339152119700748,
          "Female Percentage": "43.4%"
        },
        {
          "Year": 2012,
          "Continent": "South America",
          "Female_Percentage": 0.4207920792079208,
          "Female Percentage": "42.1%"
        },
        {
          "Year": 2016,
          "Continent": "South America",
          "Female_Percentage": 0.4156674660271783,
          "Female Percentage": "41.6%"
        }
      ]
    },
    {
      "name": "data_0",
      "source": "data-c9cd4958aa454941ccfb344427499b56",
      "transform": [
        {"type": "formula", "expr": "toNumber(datum[\"Year\"])", "as": "Year"}
      ]
    }
  ],
  "signals": [
    {
      "name": "unit",
      "value": {},
      "on": [
        {"events": "mousemove", "update": "isTuple(group()) ? group() : unit"}
      ]
    },
    {
      "name": "selector010",
      "update": "vlSelectionResolve(\"selector010_store\", \"union\")"
    },
    {
      "name": "selector010_Year",
      "on": [
        {
          "events": {"signal": "selector010_translate_delta"},
          "update": "panLinear(selector010_translate_anchor.extent_x, -selector010_translate_delta.x / width)"
        },
        {
          "events": {"signal": "selector010_zoom_delta"},
          "update": "zoomLinear(domain(\"x\"), selector010_zoom_anchor.x, selector010_zoom_delta)"
        },
        {"events": [{"source": "scope", "type": "dblclick"}], "update": "null"}
      ]
    },
    {
      "name": "selector010_Female_Percentage",
      "on": [
        {
          "events": {"signal": "selector010_translate_delta"},
          "update": "panLinear(selector010_translate_anchor.extent_y, selector010_translate_delta.y / height)"
        },
        {
          "events": {"signal": "selector010_zoom_delta"},
          "update": "zoomLinear(domain(\"y\"), selector010_zoom_anchor.y, selector010_zoom_delta)"
        },
        {"events": [{"source": "scope", "type": "dblclick"}], "update": "null"}
      ]
    },
    {
      "name": "selector010_tuple",
      "on": [
        {
          "events": [
            {"signal": "selector010_Year || selector010_Female_Percentage"}
          ],
          "update": "selector010_Year && selector010_Female_Percentage ? {unit: \"\", fields: selector010_tuple_fields, values: [selector010_Year,selector010_Female_Percentage]} : null"
        }
      ]
    },
    {
      "name": "selector010_tuple_fields",
      "value": [
        {"field": "Year", "channel": "x", "type": "R"},
        {"field": "Female_Percentage", "channel": "y", "type": "R"}
      ]
    },
    {
      "name": "selector010_translate_anchor",
      "value": {},
      "on": [
        {
          "events": [{"source": "scope", "type": "mousedown"}],
          "update": "{x: x(unit), y: y(unit), extent_x: domain(\"x\"), extent_y: domain(\"y\")}"
        }
      ]
    },
    {
      "name": "selector010_translate_delta",
      "value": {},
      "on": [
        {
          "events": [
            {
              "source": "window",
              "type": "mousemove",
              "consume": true,
              "between": [
                {"source": "scope", "type": "mousedown"},
                {"source": "window", "type": "mouseup"}
              ]
            }
          ],
          "update": "{x: selector010_translate_anchor.x - x(unit), y: selector010_translate_anchor.y - y(unit)}"
        }
      ]
    },
    {
      "name": "selector010_zoom_anchor",
      "on": [
        {
          "events": [{"source": "scope", "type": "wheel", "consume": true}],
          "update": "{x: invert(\"x\", x(unit)), y: invert(\"y\", y(unit))}"
        }
      ]
    },
    {
      "name": "selector010_zoom_delta",
      "on": [
        {
          "events": [{"source": "scope", "type": "wheel", "consume": true}],
          "force": true,
          "update": "pow(1.001, event.deltaY * pow(16, event.deltaMode))"
        }
      ]
    },
    {
      "name": "selector010_modify",
      "on": [
        {
          "events": {"signal": "selector010_tuple"},
          "update": "modify(\"selector010_store\", selector010_tuple, true)"
        }
      ]
    }
  ],
  "marks": [
    {
      "name": "pathgroup",
      "type": "group",
      "from": {
        "facet": {
          "name": "faceted_path_main",
          "data": "data_0",
          "groupby": ["Continent"]
        }
      },
      "encode": {
        "update": {
          "width": {"field": {"group": "width"}},
          "height": {"field": {"group": "height"}}
        }
      },
      "marks": [
        {
          "name": "marks",
          "type": "line",
          "clip": true,
          "style": ["line"],
          "sort": {"field": "datum[\"Year\"]"},
          "interactive": true,
          "from": {"data": "faceted_path_main"},
          "encode": {
            "update": {
              "stroke": {"scale": "color", "field": "Continent"},
              "tooltip": {
                "signal": "{\"Year\": format(datum[\"Year\"], \"\"), \"Continent\": isValid(datum[\"Continent\"]) ? datum[\"Continent\"] : \"\"+datum[\"Continent\"], \"Female Percentage\": isValid(datum[\"Female Percentage\"]) ? datum[\"Female Percentage\"] : \"\"+datum[\"Female Percentage\"]}"
              },
              "description": {
                "signal": "\"Continent\" + \": \" + (isValid(datum[\"Continent\"]) ? datum[\"Continent\"] : \"\"+datum[\"Continent\"]) + \"; \" + \"Year\" + \": \" + (format(datum[\"Year\"], \"\")) + \"; \" + \"Female Percentage\" + \": \" + (format(datum[\"Female_Percentage\"], \"\"))"
              },
              "x": {"scale": "x", "field": "Year"},
              "y": {"scale": "y", "field": "Female_Percentage"},
              "strokeWidth": {"value": 4},
              "defined": {
                "signal": "isValid(datum[\"Year\"]) && isFinite(+datum[\"Year\"]) && isValid(datum[\"Female_Percentage\"]) && isFinite(+datum[\"Female_Percentage\"])"
              }
            }
          }
        }
      ]
    }
  ],
  "scales": [
    {
      "name": "x",
      "type": "linear",
      "domain": {"data": "data_0", "field": "Year"},
      "domainRaw": {"signal": "selector010[\"Year\"]"},
      "range": [0, {"signal": "width"}],
      "nice": true,
      "zero": false
    },
    {
      "name": "y",
      "type": "linear",
      "domain": {"data": "data_0", "field": "Female_Percentage"},
      "domainRaw": {"signal": "selector010[\"Female_Percentage\"]"},
      "range": [{"signal": "height"}, 0],
      "nice": true,
      "zero": true
    },
    {
      "name": "color",
      "type": "ordinal",
      "domain": {"data": "data_0", "field": "Continent", "sort": true},
      "range": "category"
    }
  ],
  "axes": [
    {
      "scale": "x",
      "orient": "bottom",
      "gridScale": "y",
      "grid": true,
      "tickCount": {"signal": "ceil(width/40)"},
      "domain": false,
      "labels": false,
      "aria": false,
      "maxExtent": 0,
      "minExtent": 0,
      "ticks": false,
      "zindex": 0
    },
    {
      "scale": "y",
      "orient": "left",
      "gridScale": "x",
      "grid": true,
      "tickCount": {"signal": "ceil(height/40)"},
      "domain": false,
      "labels": false,
      "aria": false,
      "maxExtent": 0,
      "minExtent": 0,
      "ticks": false,
      "zindex": 0
    },
    {
      "scale": "x",
      "orient": "bottom",
      "grid": false,
      "title": "Year",
      "labelFlush": true,
      "labelOverlap": true,
      "tickCount": {"signal": "ceil(width/40)"},
      "zindex": 0
    },
    {
      "scale": "y",
      "orient": "left",
      "grid": false,
      "title": "Female Percentage",
      "labelOverlap": true,
      "tickCount": {"signal": "ceil(height/40)"},
      "zindex": 0
    }
  ],
  "legends": [
    {"stroke": "color", "symbolType": "stroke", "title": "Continent"}
  ],
  "config": {
    "legend": {
      "cornerRadius": 10,
      "fillColor": "#EEEEEE",
      "labelFontSize": 14,
      "padding": 10,
      "strokeColor": "gray"
    },
    "style": {"group-title": {"fontSize": 18}},
    "axis": {"labelFontSize": 12, "titleFontSize": 14}
  }
};

vegaEmbed('#figure27', figure27);
</script>

<script type="text/javascript">
var figure28_2 = {
  "$schema": "https://vega.github.io/schema/vega/v5.json",
  "background": "white",
  "padding": 5,
  "title": {
    "anchor": "middle",
    "text": "Changes in female athletes participation in Summer Olympics"
  },
  "data": [
    {"name": "selector069_store"},
    {
      "name": "data-c9cd4958aa454941ccfb344427499b56",
      "values": [
        {
          "Year": 1896,
          "Continent": "Global",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1900,
          "Continent": "Global",
          "Female_Percentage": 0.016045548654244308,
          "Female Percentage": "1.6%"
        },
        {
          "Year": 1904,
          "Continent": "Global",
          "Female_Percentage": 0.012307692307692308,
          "Female Percentage": "1.2%"
        },
        {
          "Year": 1906,
          "Continent": "Global",
          "Female_Percentage": 0.006489675516224189,
          "Female Percentage": "0.6%"
        },
        {
          "Year": 1908,
          "Continent": "Global",
          "Female_Percentage": 0.015568068896985756,
          "Female Percentage": "1.6%"
        },
        {
          "Year": 1912,
          "Continent": "Global",
          "Female_Percentage": 0.020242914979757085,
          "Female Percentage": "2.0%"
        },
        {
          "Year": 1920,
          "Continent": "Global",
          "Female_Percentage": 0.03247863247863248,
          "Female Percentage": "3.2%"
        },
        {
          "Year": 1924,
          "Continent": "Global",
          "Female_Percentage": 0.04917363803305448,
          "Female Percentage": "4.9%"
        },
        {
          "Year": 1928,
          "Continent": "Global",
          "Female_Percentage": 0.08397582829756199,
          "Female Percentage": "8.4%"
        },
        {
          "Year": 1932,
          "Continent": "Global",
          "Female_Percentage": 0.11859193438140808,
          "Female Percentage": "11.9%"
        },
        {
          "Year": 1936,
          "Continent": "Global",
          "Female_Percentage": 0.07177974434611603,
          "Female Percentage": "7.2%"
        },
        {
          "Year": 1948,
          "Continent": "Global",
          "Female_Percentage": 0.0974740932642487,
          "Female Percentage": "9.7%"
        },
        {
          "Year": 1952,
          "Continent": "Global",
          "Female_Percentage": 0.17301414581066374,
          "Female Percentage": "17.3%"
        },
        {
          "Year": 1956,
          "Continent": "Global",
          "Female_Percentage": 0.1704136690647482,
          "Female Percentage": "17.0%"
        },
        {
          "Year": 1960,
          "Continent": "Global",
          "Female_Percentage": 0.1761111111111111,
          "Female Percentage": "17.6%"
        },
        {
          "Year": 1964,
          "Continent": "Global",
          "Female_Percentage": 0.17183667580435724,
          "Female Percentage": "17.2%"
        },
        {
          "Year": 1968,
          "Continent": "Global",
          "Female_Percentage": 0.19755020652328728,
          "Female Percentage": "19.8%"
        },
        {
          "Year": 1972,
          "Continent": "Global",
          "Female_Percentage": 0.2010383965225791,
          "Female Percentage": "20.1%"
        },
        {
          "Year": 1976,
          "Continent": "Global",
          "Female_Percentage": 0.2333720592506535,
          "Female Percentage": "23.3%"
        },
        {
          "Year": 1980,
          "Continent": "Global",
          "Female_Percentage": 0.22398271516024487,
          "Female Percentage": "22.4%"
        },
        {
          "Year": 1984,
          "Continent": "Global",
          "Female_Percentage": 0.25244707489187346,
          "Female Percentage": "25.2%"
        },
        {
          "Year": 1988,
          "Continent": "Global",
          "Female_Percentage": 0.2830937035200793,
          "Female Percentage": "28.3%"
        },
        {
          "Year": 1992,
          "Continent": "Global",
          "Female_Percentage": 0.3129472457979697,
          "Female Percentage": "31.3%"
        },
        {
          "Year": 1996,
          "Continent": "Global",
          "Female_Percentage": 0.36325520654340493,
          "Female Percentage": "36.3%"
        },
        {
          "Year": 2000,
          "Continent": "Global",
          "Female_Percentage": 0.3939145299145299,
          "Female Percentage": "39.4%"
        },
        {
          "Year": 2004,
          "Continent": "Global",
          "Female_Percentage": 0.4132602893664841,
          "Female Percentage": "41.3%"
        },
        {
          "Year": 2008,
          "Continent": "Global",
          "Female_Percentage": 0.4284037558685446,
          "Female Percentage": "42.8%"
        },
        {
          "Year": 2012,
          "Continent": "Global",
          "Female_Percentage": 0.4500399100210435,
          "Female Percentage": "45.0%"
        },
        {
          "Year": 2016,
          "Continent": "Global",
          "Female_Percentage": 0.4535101729046594,
          "Female Percentage": "45.4%"
        },
        {
          "Year": 1896,
          "Continent": "Africa",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1900,
          "Continent": "Africa",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1904,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1906,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1908,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1912,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1920,
          "Continent": "Africa",
          "Female_Percentage": 0.01680672268907563,
          "Female Percentage": "1.7%"
        },
        {
          "Year": 1924,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1928,
          "Continent": "Africa",
          "Female_Percentage": 0.1411764705882353,
          "Female Percentage": "14.1%"
        },
        {
          "Year": 1932,
          "Continent": "Africa",
          "Female_Percentage": 0.25,
          "Female Percentage": "25.0%"
        },
        {
          "Year": 1936,
          "Continent": "Africa",
          "Female_Percentage": 0.1,
          "Female Percentage": "10.0%"
        },
        {
          "Year": 1948,
          "Continent": "Africa",
          "Female_Percentage": 0.009569377990430622,
          "Female Percentage": "1.0%"
        },
        {
          "Year": 1952,
          "Continent": "Africa",
          "Female_Percentage": 0.02735562310030395,
          "Female Percentage": "2.7%"
        },
        {
          "Year": 1956,
          "Continent": "Africa",
          "Female_Percentage": 0.0748663101604278,
          "Female Percentage": "7.5%"
        },
        {
          "Year": 1960,
          "Continent": "Africa",
          "Female_Percentage": 0.04456824512534819,
          "Female Percentage": "4.5%"
        },
        {
          "Year": 1964,
          "Continent": "Africa",
          "Female_Percentage": 0.045454545454545456,
          "Female Percentage": "4.5%"
        },
        {
          "Year": 1968,
          "Continent": "Africa",
          "Female_Percentage": 0.039886039886039885,
          "Female Percentage": "4.0%"
        },
        {
          "Year": 1972,
          "Continent": "Africa",
          "Female_Percentage": 0.056985294117647065,
          "Female Percentage": "5.7%"
        },
        {
          "Year": 1976,
          "Continent": "Africa",
          "Female_Percentage": 0.0707070707070707,
          "Female Percentage": "7.1%"
        },
        {
          "Year": 1980,
          "Continent": "Africa",
          "Female_Percentage": 0.1524590163934426,
          "Female Percentage": "15.2%"
        },
        {
          "Year": 1984,
          "Continent": "Africa",
          "Female_Percentage": 0.09419354838709676,
          "Female Percentage": "9.4%"
        },
        {
          "Year": 1988,
          "Continent": "Africa",
          "Female_Percentage": 0.13974799541809851,
          "Female Percentage": "14.0%"
        },
        {
          "Year": 1992,
          "Continent": "Africa",
          "Female_Percentage": 0.22341568206229864,
          "Female Percentage": "22.3%"
        },
        {
          "Year": 1996,
          "Continent": "Africa",
          "Female_Percentage": 0.2462077012835473,
          "Female Percentage": "24.6%"
        },
        {
          "Year": 2000,
          "Continent": "Africa",
          "Female_Percentage": 0.3296370967741936,
          "Female Percentage": "33.0%"
        },
        {
          "Year": 2004,
          "Continent": "Africa",
          "Female_Percentage": 0.33407572383073497,
          "Female Percentage": "33.4%"
        },
        {
          "Year": 2008,
          "Continent": "Africa",
          "Female_Percentage": 0.3874734607218684,
          "Female Percentage": "38.7%"
        },
        {
          "Year": 2012,
          "Continent": "Africa",
          "Female_Percentage": 0.399581589958159,
          "Female Percentage": "40.0%"
        },
        {
          "Year": 2016,
          "Continent": "Africa",
          "Female_Percentage": 0.3836772983114447,
          "Female Percentage": "38.4%"
        },
        {
          "Year": 1896,
          "Continent": "Asia",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1900,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1904,
          "Continent": "Asia",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1906,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1908,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1912,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1920,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1924,
          "Continent": "Asia",
          "Female_Percentage": 0.033707865168539325,
          "Female Percentage": "3.4%"
        },
        {
          "Year": 1928,
          "Continent": "Asia",
          "Female_Percentage": 0.015873015873015872,
          "Female Percentage": "1.6%"
        },
        {
          "Year": 1932,
          "Continent": "Asia",
          "Female_Percentage": 0.11203319502074688,
          "Female Percentage": "11.2%"
        },
        {
          "Year": 1936,
          "Continent": "Asia",
          "Female_Percentage": 0.057620817843866176,
          "Female Percentage": "5.8%"
        },
        {
          "Year": 1948,
          "Continent": "Asia",
          "Female_Percentage": 0.0069124423963133645,
          "Female Percentage": "0.7%"
        },
        {
          "Year": 1952,
          "Continent": "Asia",
          "Female_Percentage": 0.065439672801636,
          "Female Percentage": "6.5%"
        },
        {
          "Year": 1956,
          "Continent": "Asia",
          "Female_Percentage": 0.1060126582278481,
          "Female Percentage": "10.6%"
        },
        {
          "Year": 1960,
          "Continent": "Asia",
          "Female_Percentage": 0.129366106080207,
          "Female Percentage": "12.9%"
        },
        {
          "Year": 1964,
          "Continent": "Asia",
          "Female_Percentage": 0.14587593728698026,
          "Female Percentage": "14.6%"
        },
        {
          "Year": 1968,
          "Continent": "Asia",
          "Female_Percentage": 0.17119244391971666,
          "Female Percentage": "17.1%"
        },
        {
          "Year": 1972,
          "Continent": "Asia",
          "Female_Percentage": 0.14781746031746032,
          "Female Percentage": "14.8%"
        },
        {
          "Year": 1976,
          "Continent": "Asia",
          "Female_Percentage": 0.16761041902604756,
          "Female Percentage": "16.8%"
        },
        {
          "Year": 1980,
          "Continent": "Asia",
          "Female_Percentage": 0.1494661921708185,
          "Female Percentage": "14.9%"
        },
        {
          "Year": 1984,
          "Continent": "Asia",
          "Female_Percentage": 0.2409855769230769,
          "Female Percentage": "24.1%"
        },
        {
          "Year": 1988,
          "Continent": "Asia",
          "Female_Percentage": 0.3037466547725245,
          "Female Percentage": "30.4%"
        },
        {
          "Year": 1992,
          "Continent": "Asia",
          "Female_Percentage": 0.31186440677966104,
          "Female Percentage": "31.2%"
        },
        {
          "Year": 1996,
          "Continent": "Asia",
          "Female_Percentage": 0.3821571238348868,
          "Female Percentage": "38.2%"
        },
        {
          "Year": 2000,
          "Continent": "Asia",
          "Female_Percentage": 0.39642620780939775,
          "Female Percentage": "39.6%"
        },
        {
          "Year": 2004,
          "Continent": "Asia",
          "Female_Percentage": 0.4359058207979071,
          "Female Percentage": "43.6%"
        },
        {
          "Year": 2008,
          "Continent": "Asia",
          "Female_Percentage": 0.43423423423423424,
          "Female Percentage": "43.4%"
        },
        {
          "Year": 2012,
          "Continent": "Asia",
          "Female_Percentage": 0.4599396580623533,
          "Female Percentage": "46.0%"
        },
        {
          "Year": 2016,
          "Continent": "Asia",
          "Female_Percentage": 0.4653897849462366,
          "Female Percentage": "46.5%"
        },
        {
          "Year": 1896,
          "Continent": "Europe",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1900,
          "Continent": "Europe",
          "Female_Percentage": 0.012528473804100227,
          "Female Percentage": "1.3%"
        },
        {
          "Year": 1904,
          "Continent": "Europe",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1906,
          "Continent": "Europe",
          "Female_Percentage": 0.006905210295040804,
          "Female Percentage": "0.7%"
        },
        {
          "Year": 1908,
          "Continent": "Europe",
          "Female_Percentage": 0.01800076599004213,
          "Female Percentage": "1.8%"
        },
        {
          "Year": 1912,
          "Continent": "Europe",
          "Female_Percentage": 0.024897480960749854,
          "Female Percentage": "2.5%"
        },
        {
          "Year": 1920,
          "Continent": "Europe",
          "Female_Percentage": 0.03142943487458446,
          "Female Percentage": "3.1%"
        },
        {
          "Year": 1924,
          "Continent": "Europe",
          "Female_Percentage": 0.05149330587023687,
          "Female Percentage": "5.1%"
        },
        {
          "Year": 1928,
          "Continent": "Europe",
          "Female_Percentage": 0.0821664464993395,
          "Female Percentage": "8.2%"
        },
        {
          "Year": 1932,
          "Continent": "Europe",
          "Female_Percentage": 0.10588235294117647,
          "Female Percentage": "10.6%"
        },
        {
          "Year": 1936,
          "Continent": "Europe",
          "Female_Percentage": 0.06700091157702825,
          "Female Percentage": "6.7%"
        },
        {
          "Year": 1948,
          "Continent": "Europe",
          "Female_Percentage": 0.1073929961089494,
          "Female Percentage": "10.7%"
        },
        {
          "Year": 1952,
          "Continent": "Europe",
          "Female_Percentage": 0.20599325262949,
          "Female Percentage": "20.6%"
        },
        {
          "Year": 1956,
          "Continent": "Europe",
          "Female_Percentage": 0.20808451998162608,
          "Female Percentage": "20.8%"
        },
        {
          "Year": 1960,
          "Continent": "Europe",
          "Female_Percentage": 0.19808861859252824,
          "Female Percentage": "19.8%"
        },
        {
          "Year": 1964,
          "Continent": "Europe",
          "Female_Percentage": 0.19008009858287125,
          "Female Percentage": "19.0%"
        },
        {
          "Year": 1968,
          "Continent": "Europe",
          "Female_Percentage": 0.20454545454545456,
          "Female Percentage": "20.5%"
        },
        {
          "Year": 1972,
          "Continent": "Europe",
          "Female_Percentage": 0.22300968580203165,
          "Female Percentage": "22.3%"
        },
        {
          "Year": 1976,
          "Continent": "Europe",
          "Female_Percentage": 0.2362555720653789,
          "Female Percentage": "23.6%"
        },
        {
          "Year": 1980,
          "Continent": "Europe",
          "Female_Percentage": 0.257801108194809,
          "Female Percentage": "25.8%"
        },
        {
          "Year": 1984,
          "Continent": "Europe",
          "Female_Percentage": 0.2688271604938272,
          "Female Percentage": "26.9%"
        },
        {
          "Year": 1988,
          "Continent": "Europe",
          "Female_Percentage": 0.29081000743126084,
          "Female Percentage": "29.1%"
        },
        {
          "Year": 1992,
          "Continent": "Europe",
          "Female_Percentage": 0.3262682418346073,
          "Female Percentage": "32.6%"
        },
        {
          "Year": 1996,
          "Continent": "Europe",
          "Female_Percentage": 0.3664026677782409,
          "Female Percentage": "36.6%"
        },
        {
          "Year": 2000,
          "Continent": "Europe",
          "Female_Percentage": 0.38596989491621697,
          "Female Percentage": "38.6%"
        },
        {
          "Year": 2004,
          "Continent": "Europe",
          "Female_Percentage": 0.4022806004618938,
          "Female Percentage": "40.2%"
        },
        {
          "Year": 2008,
          "Continent": "Europe",
          "Female_Percentage": 0.4252481849162839,
          "Female Percentage": "42.5%"
        },
        {
          "Year": 2012,
          "Continent": "Europe",
          "Female_Percentage": 0.4477747502270663,
          "Female Percentage": "44.8%"
        },
        {
          "Year": 2016,
          "Continent": "Europe",
          "Female_Percentage": 0.4510353417406197,
          "Female Percentage": "45.1%"
        },
        {
          "Year": 1896,
          "Continent": "North America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1900,
          "Continent": "North America",
          "Female_Percentage": 0.05960264900662252,
          "Female Percentage": "6.0%"
        },
        {
          "Year": 1904,
          "Continent": "North America",
          "Female_Percentage": 0.013605442176870748,
          "Female Percentage": "1.4%"
        },
        {
          "Year": 1906,
          "Continent": "North America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1908,
          "Continent": "North America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1912,
          "Continent": "North America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1920,
          "Continent": "North America",
          "Female_Percentage": 0.03942652329749104,
          "Female Percentage": "3.9%"
        },
        {
          "Year": 1924,
          "Continent": "North America",
          "Female_Percentage": 0.05843071786310518,
          "Female Percentage": "5.8%"
        },
        {
          "Year": 1928,
          "Continent": "North America",
          "Female_Percentage": 0.11,
          "Female Percentage": "11.0%"
        },
        {
          "Year": 1932,
          "Continent": "North America",
          "Female_Percentage": 0.14641148325358852,
          "Female Percentage": "14.6%"
        },
        {
          "Year": 1936,
          "Continent": "North America",
          "Female_Percentage": 0.1221264367816092,
          "Female Percentage": "12.2%"
        },
        {
          "Year": 1948,
          "Continent": "North America",
          "Female_Percentage": 0.11932418162618795,
          "Female Percentage": "11.9%"
        },
        {
          "Year": 1952,
          "Continent": "North America",
          "Female_Percentage": 0.16042154566744732,
          "Female Percentage": "16.0%"
        },
        {
          "Year": 1956,
          "Continent": "North America",
          "Female_Percentage": 0.19484240687679086,
          "Female Percentage": "19.5%"
        },
        {
          "Year": 1960,
          "Continent": "North America",
          "Female_Percentage": 0.21568627450980396,
          "Female Percentage": "21.6%"
        },
        {
          "Year": 1964,
          "Continent": "North America",
          "Female_Percentage": 0.2101661779081134,
          "Female Percentage": "21.0%"
        },
        {
          "Year": 1968,
          "Continent": "North America",
          "Female_Percentage": 0.2272957889396245,
          "Female Percentage": "22.7%"
        },
        {
          "Year": 1972,
          "Continent": "North America",
          "Female_Percentage": 0.23755924170616116,
          "Female Percentage": "23.8%"
        },
        {
          "Year": 1976,
          "Continent": "North America",
          "Female_Percentage": 0.27378964941569284,
          "Female Percentage": "27.4%"
        },
        {
          "Year": 1980,
          "Continent": "North America",
          "Female_Percentage": 0.17372881355932204,
          "Female Percentage": "17.4%"
        },
        {
          "Year": 1984,
          "Continent": "North America",
          "Female_Percentage": 0.3223987698616094,
          "Female Percentage": "32.2%"
        },
        {
          "Year": 1988,
          "Continent": "North America",
          "Female_Percentage": 0.32998324958123953,
          "Female Percentage": "33.0%"
        },
        {
          "Year": 1992,
          "Continent": "North America",
          "Female_Percentage": 0.3336653386454183,
          "Female Percentage": "33.4%"
        },
        {
          "Year": 1996,
          "Continent": "North America",
          "Female_Percentage": 0.3953257086026852,
          "Female Percentage": "39.5%"
        },
        {
          "Year": 2000,
          "Continent": "North America",
          "Female_Percentage": 0.4241469816272966,
          "Female Percentage": "42.4%"
        },
        {
          "Year": 2004,
          "Continent": "North America",
          "Female_Percentage": 0.4470720720720721,
          "Female Percentage": "44.7%"
        },
        {
          "Year": 2008,
          "Continent": "North America",
          "Female_Percentage": 0.4338074398249453,
          "Female Percentage": "43.4%"
        },
        {
          "Year": 2012,
          "Continent": "North America",
          "Female_Percentage": 0.4791666666666667,
          "Female Percentage": "47.9%"
        },
        {
          "Year": 2016,
          "Continent": "North America",
          "Female_Percentage": 0.4955947136563877,
          "Female Percentage": "49.6%"
        },
        {
          "Year": 1896,
          "Continent": "Oceania",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1900,
          "Continent": "Oceania",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1904,
          "Continent": "Oceania",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1906,
          "Continent": "Oceania",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1908,
          "Continent": "Oceania",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1912,
          "Continent": "Oceania",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1920,
          "Continent": "Oceania",
          "Female_Percentage": 0.14285714285714285,
          "Female Percentage": "14.3%"
        },
        {
          "Year": 1924,
          "Continent": "Oceania",
          "Female_Percentage": 0.045454545454545456,
          "Female Percentage": "4.5%"
        },
        {
          "Year": 1928,
          "Continent": "Oceania",
          "Female_Percentage": 0.2857142857142857,
          "Female Percentage": "28.6%"
        },
        {
          "Year": 1932,
          "Continent": "Oceania",
          "Female_Percentage": 0.12244897959183673,
          "Female Percentage": "12.2%"
        },
        {
          "Year": 1936,
          "Continent": "Oceania",
          "Female_Percentage": 0.125,
          "Female Percentage": "12.5%"
        },
        {
          "Year": 1948,
          "Continent": "Oceania",
          "Female_Percentage": 0.17117117117117114,
          "Female Percentage": "17.1%"
        },
        {
          "Year": 1952,
          "Continent": "Oceania",
          "Female_Percentage": 0.1375,
          "Female Percentage": "13.8%"
        },
        {
          "Year": 1956,
          "Continent": "Oceania",
          "Female_Percentage": 0.1729957805907173,
          "Female Percentage": "17.3%"
        },
        {
          "Year": 1960,
          "Continent": "Oceania",
          "Female_Percentage": 0.18787878787878787,
          "Female Percentage": "18.8%"
        },
        {
          "Year": 1964,
          "Continent": "Oceania",
          "Female_Percentage": 0.2375,
          "Female Percentage": "23.8%"
        },
        {
          "Year": 1968,
          "Continent": "Oceania",
          "Female_Percentage": 0.25862068965517243,
          "Female Percentage": "25.9%"
        },
        {
          "Year": 1972,
          "Continent": "Oceania",
          "Female_Percentage": 0.2356020942408377,
          "Female Percentage": "23.6%"
        },
        {
          "Year": 1976,
          "Continent": "Oceania",
          "Female_Percentage": 0.2383419689119171,
          "Female Percentage": "23.8%"
        },
        {
          "Year": 1980,
          "Continent": "Oceania",
          "Female_Percentage": 0.29949238578680204,
          "Female Percentage": "29.9%"
        },
        {
          "Year": 1984,
          "Continent": "Oceania",
          "Female_Percentage": 0.2949640287769784,
          "Female Percentage": "29.5%"
        },
        {
          "Year": 1988,
          "Continent": "Oceania",
          "Female_Percentage": 0.2690972222222222,
          "Female Percentage": "26.9%"
        },
        {
          "Year": 1992,
          "Continent": "Oceania",
          "Female_Percentage": 0.3381712626995646,
          "Female Percentage": "33.8%"
        },
        {
          "Year": 1996,
          "Continent": "Oceania",
          "Female_Percentage": 0.3949801849405548,
          "Female Percentage": "39.5%"
        },
        {
          "Year": 2000,
          "Continent": "Oceania",
          "Female_Percentage": 0.4650934119960669,
          "Female Percentage": "46.5%"
        },
        {
          "Year": 2004,
          "Continent": "Oceania",
          "Female_Percentage": 0.4480286738351255,
          "Female Percentage": "44.8%"
        },
        {
          "Year": 2008,
          "Continent": "Oceania",
          "Female_Percentage": 0.4597839135654262,
          "Female Percentage": "46.0%"
        },
        {
          "Year": 2012,
          "Continent": "Oceania",
          "Female_Percentage": 0.4623115577889447,
          "Female Percentage": "46.2%"
        },
        {
          "Year": 2016,
          "Continent": "Oceania",
          "Female_Percentage": 0.4833141542002302,
          "Female Percentage": "48.3%"
        },
        {
          "Year": 1896,
          "Continent": "South America",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1900,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1904,
          "Continent": "South America",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1906,
          "Continent": "South America",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1908,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1912,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1920,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1924,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1928,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1932,
          "Continent": "South America",
          "Female_Percentage": 0.023809523809523808,
          "Female Percentage": "2.4%"
        },
        {
          "Year": 1936,
          "Continent": "South America",
          "Female_Percentage": 0.03205128205128205,
          "Female Percentage": "3.2%"
        },
        {
          "Year": 1948,
          "Continent": "South America",
          "Female_Percentage": 0.08225806451612902,
          "Female Percentage": "8.2%"
        },
        {
          "Year": 1952,
          "Continent": "South America",
          "Female_Percentage": 0.07068607068607069,
          "Female Percentage": "7.1%"
        },
        {
          "Year": 1956,
          "Continent": "South America",
          "Female_Percentage": 0.021428571428571432,
          "Female Percentage": "2.1%"
        },
        {
          "Year": 1960,
          "Continent": "South America",
          "Female_Percentage": 0.03523035230352303,
          "Female Percentage": "3.5%"
        },
        {
          "Year": 1964,
          "Continent": "South America",
          "Female_Percentage": 0.04132231404958678,
          "Female Percentage": "4.1%"
        },
        {
          "Year": 1968,
          "Continent": "South America",
          "Female_Percentage": 0.15560165975103735,
          "Female Percentage": "15.6%"
        },
        {
          "Year": 1972,
          "Continent": "South America",
          "Female_Percentage": 0.117096018735363,
          "Female Percentage": "11.7%"
        },
        {
          "Year": 1976,
          "Continent": "South America",
          "Female_Percentage": 0.2050561797752809,
          "Female Percentage": "20.5%"
        },
        {
          "Year": 1980,
          "Continent": "South America",
          "Female_Percentage": 0.14788732394366194,
          "Female Percentage": "14.8%"
        },
        {
          "Year": 1984,
          "Continent": "South America",
          "Female_Percentage": 0.13333333333333333,
          "Female Percentage": "13.3%"
        },
        {
          "Year": 1988,
          "Continent": "South America",
          "Female_Percentage": 0.2332155477031802,
          "Female Percentage": "23.3%"
        },
        {
          "Year": 1992,
          "Continent": "South America",
          "Female_Percentage": 0.2249560632688928,
          "Female Percentage": "22.5%"
        },
        {
          "Year": 1996,
          "Continent": "South America",
          "Female_Percentage": 0.2697095435684647,
          "Female Percentage": "27.0%"
        },
        {
          "Year": 2000,
          "Continent": "South America",
          "Female_Percentage": 0.366306027820711,
          "Female Percentage": "36.6%"
        },
        {
          "Year": 2004,
          "Continent": "South America",
          "Female_Percentage": 0.39811066126855604,
          "Female Percentage": "39.8%"
        },
        {
          "Year": 2008,
          "Continent": "South America",
          "Female_Percentage": 0.4339152119700748,
          "Female Percentage": "43.4%"
        },
        {
          "Year": 2012,
          "Continent": "South America",
          "Female_Percentage": 0.4207920792079208,
          "Female Percentage": "42.1%"
        },
        {
          "Year": 2016,
          "Continent": "South America",
          "Female_Percentage": 0.4156674660271783,
          "Female Percentage": "41.6%"
        }
      ]
    },
    {
      "name": "data_0",
      "source": "data-c9cd4958aa454941ccfb344427499b56",
      "transform": [
        {"type": "formula", "expr": "toNumber(datum[\"Year\"])", "as": "Year"}
      ]
    },
    {
      "name": "facet_domain",
      "source": "data_0",
      "transform": [{"type": "aggregate", "groupby": ["Continent"]}]
    },
    {
      "name": "facet_domain_row",
      "transform": [
        {
          "type": "sequence",
          "start": 0,
          "stop": {"signal": "ceil(length(data(\"facet_domain\")) / 3)"}
        }
      ]
    },
    {
      "name": "facet_domain_column",
      "transform": [
        {
          "type": "sequence",
          "start": 0,
          "stop": {"signal": "min(length(data(\"facet_domain\")), 3)"}
        }
      ]
    }
  ],
  "signals": [
    {"name": "child_width", "value": 200},
    {"name": "child_height", "value": 200},
    {
      "name": "unit",
      "value": {},
      "on": [
        {"events": "mousemove", "update": "isTuple(group()) ? group() : unit"}
      ]
    },
    {
      "name": "selector069",
      "update": "{\"Year\": selector069_Year, \"Female_Percentage\": selector069_Female_Percentage}"
    },
    {"name": "selector069_Year"},
    {"name": "selector069_Female_Percentage"}
  ],
  "layout": {"padding": 20, "bounds": "full", "align": "all", "columns": 3},
  "marks": [
    {
      "name": "facet-title",
      "type": "group",
      "role": "column-title",
      "title": {"text": "Continent", "style": "guide-title", "offset": 10}
    },
    {
      "name": "row_header",
      "type": "group",
      "role": "row-header",
      "from": {"data": "facet_domain_row"},
      "encode": {"update": {"height": {"signal": "child_height"}}},
      "axes": [
        {
          "scale": "y",
          "orient": "left",
          "grid": false,
          "title": "Female_Percentage",
          "labelOverlap": true,
          "tickCount": {"signal": "ceil(child_height/40)"},
          "zindex": 0
        }
      ]
    },
    {
      "name": "column_footer",
      "type": "group",
      "role": "column-footer",
      "from": {"data": "facet_domain_column"},
      "encode": {"update": {"width": {"signal": "child_width"}}},
      "axes": [
        {
          "scale": "x",
          "orient": "bottom",
          "grid": false,
          "title": "Year",
          "labelFlush": true,
          "labelOverlap": true,
          "tickCount": {"signal": "ceil(child_width/40)"},
          "zindex": 0
        }
      ]
    },
    {
      "name": "cell",
      "type": "group",
      "title": {
        "text": {
          "signal": "isValid(parent[\"Continent\"]) ? parent[\"Continent\"] : \"\"+parent[\"Continent\"]"
        },
        "style": "guide-label",
        "frame": "group",
        "offset": 10
      },
      "style": "cell",
      "from": {
        "facet": {"name": "facet", "data": "data_0", "groupby": ["Continent"]}
      },
      "sort": {"field": ["datum[\"Continent\"]"], "order": ["ascending"]},
      "encode": {
        "update": {
          "width": {"signal": "child_width"},
          "height": {"signal": "child_height"}
        }
      },
      "signals": [
        {
          "name": "facet",
          "value": {},
          "on": [
            {
              "events": [{"source": "scope", "type": "mousemove"}],
              "update": "isTuple(facet) ? facet : group(\"cell\").datum"
            }
          ]
        },
        {
          "name": "selector069_Year",
          "on": [
            {
              "events": {"signal": "selector069_translate_delta"},
              "update": "panLinear(selector069_translate_anchor.extent_x, -selector069_translate_delta.x / child_width)"
            },
            {
              "events": {"signal": "selector069_zoom_delta"},
              "update": "zoomLinear(domain(\"x\"), selector069_zoom_anchor.x, selector069_zoom_delta)"
            },
            {
              "events": [{"source": "scope", "type": "dblclick"}],
              "update": "null"
            }
          ],
          "push": "outer"
        },
        {
          "name": "selector069_Female_Percentage",
          "on": [
            {
              "events": {"signal": "selector069_translate_delta"},
              "update": "panLinear(selector069_translate_anchor.extent_y, selector069_translate_delta.y / child_height)"
            },
            {
              "events": {"signal": "selector069_zoom_delta"},
              "update": "zoomLinear(domain(\"y\"), selector069_zoom_anchor.y, selector069_zoom_delta)"
            },
            {
              "events": [{"source": "scope", "type": "dblclick"}],
              "update": "null"
            }
          ],
          "push": "outer"
        },
        {
          "name": "selector069_tuple",
          "on": [
            {
              "events": [
                {"signal": "selector069_Year || selector069_Female_Percentage"}
              ],
              "update": "selector069_Year && selector069_Female_Percentage ? {unit: \"child\" + '__facet_facet_' + (facet[\"Continent\"]), fields: selector069_tuple_fields, values: [selector069_Year,selector069_Female_Percentage]} : null"
            }
          ]
        },
        {
          "name": "selector069_tuple_fields",
          "value": [
            {"field": "Year", "channel": "x", "type": "R"},
            {"field": "Female_Percentage", "channel": "y", "type": "R"}
          ]
        },
        {
          "name": "selector069_translate_anchor",
          "value": {},
          "on": [
            {
              "events": [{"source": "scope", "type": "mousedown"}],
              "update": "{x: x(unit), y: y(unit), extent_x: domain(\"x\"), extent_y: domain(\"y\")}"
            }
          ]
        },
        {
          "name": "selector069_translate_delta",
          "value": {},
          "on": [
            {
              "events": [
                {
                  "source": "window",
                  "type": "mousemove",
                  "consume": true,
                  "between": [
                    {"source": "scope", "type": "mousedown"},
                    {"source": "window", "type": "mouseup"}
                  ]
                }
              ],
              "update": "{x: selector069_translate_anchor.x - x(unit), y: selector069_translate_anchor.y - y(unit)}"
            }
          ]
        },
        {
          "name": "selector069_zoom_anchor",
          "on": [
            {
              "events": [{"source": "scope", "type": "wheel", "consume": true}],
              "update": "{x: invert(\"x\", x(unit)), y: invert(\"y\", y(unit))}"
            }
          ]
        },
        {
          "name": "selector069_zoom_delta",
          "on": [
            {
              "events": [{"source": "scope", "type": "wheel", "consume": true}],
              "force": true,
              "update": "pow(1.001, event.deltaY * pow(16, event.deltaMode))"
            }
          ]
        },
        {
          "name": "selector069_modify",
          "on": [
            {
              "events": {"signal": "selector069_tuple"},
              "update": "modify(\"selector069_store\", selector069_tuple, true)"
            }
          ]
        }
      ],
      "marks": [
        {
          "name": "child_pathgroup",
          "type": "group",
          "from": {
            "facet": {
              "name": "faceted_path_child_main",
              "data": "facet",
              "groupby": ["Continent"]
            }
          },
          "encode": {
            "update": {
              "width": {"field": {"group": "width"}},
              "height": {"field": {"group": "height"}}
            }
          },
          "marks": [
            {
              "name": "child_marks",
              "type": "line",
              "clip": true,
              "style": ["line"],
              "sort": {"field": "datum[\"Year\"]"},
              "interactive": true,
              "from": {"data": "faceted_path_child_main"},
              "encode": {
                "update": {
                  "stroke": {"scale": "color", "field": "Continent"},
                  "tooltip": {
                    "signal": "{\"Year\": format(datum[\"Year\"], \"\"), \"Continent\": isValid(datum[\"Continent\"]) ? datum[\"Continent\"] : \"\"+datum[\"Continent\"], \"Female Percentage\": isValid(datum[\"Female Percentage\"]) ? datum[\"Female Percentage\"] : \"\"+datum[\"Female Percentage\"]}"
                  },
                  "description": {
                    "signal": "\"Continent\" + \": \" + (isValid(datum[\"Continent\"]) ? datum[\"Continent\"] : \"\"+datum[\"Continent\"]) + \"; \" + \"Year\" + \": \" + (format(datum[\"Year\"], \"\")) + \"; \" + \"Female Percentage\" + \": \" + (isValid(datum[\"Female Percentage\"]) ? datum[\"Female Percentage\"] : \"\"+datum[\"Female Percentage\"]) + \"; \" + \"Female_Percentage\" + \": \" + (format(datum[\"Female_Percentage\"], \"\"))"
                  },
                  "x": {"scale": "x", "field": "Year"},
                  "y": {"scale": "y", "field": "Female_Percentage"},
                  "strokeWidth": {"value": 5},
                  "defined": {
                    "signal": "isValid(datum[\"Year\"]) && isFinite(+datum[\"Year\"]) && isValid(datum[\"Female_Percentage\"]) && isFinite(+datum[\"Female_Percentage\"])"
                  }
                }
              }
            }
          ]
        }
      ],
      "axes": [
        {
          "scale": "x",
          "orient": "bottom",
          "gridScale": "y",
          "grid": true,
          "tickCount": {"signal": "ceil(child_width/40)"},
          "domain": false,
          "labels": false,
          "aria": false,
          "maxExtent": 0,
          "minExtent": 0,
          "ticks": false,
          "zindex": 0
        },
        {
          "scale": "y",
          "orient": "left",
          "gridScale": "x",
          "grid": true,
          "tickCount": {"signal": "ceil(child_height/40)"},
          "domain": false,
          "labels": false,
          "aria": false,
          "maxExtent": 0,
          "minExtent": 0,
          "ticks": false,
          "zindex": 0
        }
      ]
    }
  ],
  "scales": [
    {
      "name": "x",
      "type": "linear",
      "domain": {"data": "data_0", "field": "Year"},
      "domainRaw": {"signal": "selector069[\"Year\"]"},
      "range": [0, {"signal": "child_width"}],
      "nice": true,
      "zero": false
    },
    {
      "name": "y",
      "type": "linear",
      "domain": {"data": "data_0", "field": "Female_Percentage"},
      "domainRaw": {"signal": "selector069[\"Female_Percentage\"]"},
      "range": [{"signal": "child_height"}, 0],
      "nice": true,
      "zero": true
    },
    {
      "name": "color",
      "type": "ordinal",
      "domain": {"data": "data_0", "field": "Continent", "sort": true},
      "range": "category"
    }
  ],
  "legends": [
    {"stroke": "color", "symbolType": "stroke", "title": "Continent"}
  ],
  "config": {"style": {"group-title": {"fontSize": 18, "fill": "black"}}}
}

vegaEmbed('#figure28_2', figure28_2);
</script>

<script type="text/javascript">
var figure29 = {
  "$schema": "https://vega.github.io/schema/vega/v5.json",
  "background": "white",
  "padding": 5,
  "title": {
    "text": "Changes in female athletes participation in Summer Olympics",
    "anchor": "middle"
  },
  "data": [
    {"name": "selector072_store"},
    {
      "name": "data-c9cd4958aa454941ccfb344427499b56",
      "values": [
        {
          "Year": 1896,
          "Continent": "Global",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1900,
          "Continent": "Global",
          "Female_Percentage": 0.016045548654244308,
          "Female Percentage": "1.6%"
        },
        {
          "Year": 1904,
          "Continent": "Global",
          "Female_Percentage": 0.012307692307692308,
          "Female Percentage": "1.2%"
        },
        {
          "Year": 1906,
          "Continent": "Global",
          "Female_Percentage": 0.006489675516224189,
          "Female Percentage": "0.6%"
        },
        {
          "Year": 1908,
          "Continent": "Global",
          "Female_Percentage": 0.015568068896985756,
          "Female Percentage": "1.6%"
        },
        {
          "Year": 1912,
          "Continent": "Global",
          "Female_Percentage": 0.020242914979757085,
          "Female Percentage": "2.0%"
        },
        {
          "Year": 1920,
          "Continent": "Global",
          "Female_Percentage": 0.03247863247863248,
          "Female Percentage": "3.2%"
        },
        {
          "Year": 1924,
          "Continent": "Global",
          "Female_Percentage": 0.04917363803305448,
          "Female Percentage": "4.9%"
        },
        {
          "Year": 1928,
          "Continent": "Global",
          "Female_Percentage": 0.08397582829756199,
          "Female Percentage": "8.4%"
        },
        {
          "Year": 1932,
          "Continent": "Global",
          "Female_Percentage": 0.11859193438140808,
          "Female Percentage": "11.9%"
        },
        {
          "Year": 1936,
          "Continent": "Global",
          "Female_Percentage": 0.07177974434611603,
          "Female Percentage": "7.2%"
        },
        {
          "Year": 1948,
          "Continent": "Global",
          "Female_Percentage": 0.0974740932642487,
          "Female Percentage": "9.7%"
        },
        {
          "Year": 1952,
          "Continent": "Global",
          "Female_Percentage": 0.17301414581066374,
          "Female Percentage": "17.3%"
        },
        {
          "Year": 1956,
          "Continent": "Global",
          "Female_Percentage": 0.1704136690647482,
          "Female Percentage": "17.0%"
        },
        {
          "Year": 1960,
          "Continent": "Global",
          "Female_Percentage": 0.1761111111111111,
          "Female Percentage": "17.6%"
        },
        {
          "Year": 1964,
          "Continent": "Global",
          "Female_Percentage": 0.17183667580435724,
          "Female Percentage": "17.2%"
        },
        {
          "Year": 1968,
          "Continent": "Global",
          "Female_Percentage": 0.19755020652328728,
          "Female Percentage": "19.8%"
        },
        {
          "Year": 1972,
          "Continent": "Global",
          "Female_Percentage": 0.2010383965225791,
          "Female Percentage": "20.1%"
        },
        {
          "Year": 1976,
          "Continent": "Global",
          "Female_Percentage": 0.2333720592506535,
          "Female Percentage": "23.3%"
        },
        {
          "Year": 1980,
          "Continent": "Global",
          "Female_Percentage": 0.22398271516024487,
          "Female Percentage": "22.4%"
        },
        {
          "Year": 1984,
          "Continent": "Global",
          "Female_Percentage": 0.25244707489187346,
          "Female Percentage": "25.2%"
        },
        {
          "Year": 1988,
          "Continent": "Global",
          "Female_Percentage": 0.2830937035200793,
          "Female Percentage": "28.3%"
        },
        {
          "Year": 1992,
          "Continent": "Global",
          "Female_Percentage": 0.3129472457979697,
          "Female Percentage": "31.3%"
        },
        {
          "Year": 1996,
          "Continent": "Global",
          "Female_Percentage": 0.36325520654340493,
          "Female Percentage": "36.3%"
        },
        {
          "Year": 2000,
          "Continent": "Global",
          "Female_Percentage": 0.3939145299145299,
          "Female Percentage": "39.4%"
        },
        {
          "Year": 2004,
          "Continent": "Global",
          "Female_Percentage": 0.4132602893664841,
          "Female Percentage": "41.3%"
        },
        {
          "Year": 2008,
          "Continent": "Global",
          "Female_Percentage": 0.4284037558685446,
          "Female Percentage": "42.8%"
        },
        {
          "Year": 2012,
          "Continent": "Global",
          "Female_Percentage": 0.4500399100210435,
          "Female Percentage": "45.0%"
        },
        {
          "Year": 2016,
          "Continent": "Global",
          "Female_Percentage": 0.4535101729046594,
          "Female Percentage": "45.4%"
        },
        {
          "Year": 1896,
          "Continent": "Africa",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1900,
          "Continent": "Africa",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1904,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1906,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1908,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1912,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1920,
          "Continent": "Africa",
          "Female_Percentage": 0.01680672268907563,
          "Female Percentage": "1.7%"
        },
        {
          "Year": 1924,
          "Continent": "Africa",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1928,
          "Continent": "Africa",
          "Female_Percentage": 0.1411764705882353,
          "Female Percentage": "14.1%"
        },
        {
          "Year": 1932,
          "Continent": "Africa",
          "Female_Percentage": 0.25,
          "Female Percentage": "25.0%"
        },
        {
          "Year": 1936,
          "Continent": "Africa",
          "Female_Percentage": 0.1,
          "Female Percentage": "10.0%"
        },
        {
          "Year": 1948,
          "Continent": "Africa",
          "Female_Percentage": 0.009569377990430622,
          "Female Percentage": "1.0%"
        },
        {
          "Year": 1952,
          "Continent": "Africa",
          "Female_Percentage": 0.02735562310030395,
          "Female Percentage": "2.7%"
        },
        {
          "Year": 1956,
          "Continent": "Africa",
          "Female_Percentage": 0.0748663101604278,
          "Female Percentage": "7.5%"
        },
        {
          "Year": 1960,
          "Continent": "Africa",
          "Female_Percentage": 0.04456824512534819,
          "Female Percentage": "4.5%"
        },
        {
          "Year": 1964,
          "Continent": "Africa",
          "Female_Percentage": 0.045454545454545456,
          "Female Percentage": "4.5%"
        },
        {
          "Year": 1968,
          "Continent": "Africa",
          "Female_Percentage": 0.039886039886039885,
          "Female Percentage": "4.0%"
        },
        {
          "Year": 1972,
          "Continent": "Africa",
          "Female_Percentage": 0.056985294117647065,
          "Female Percentage": "5.7%"
        },
        {
          "Year": 1976,
          "Continent": "Africa",
          "Female_Percentage": 0.0707070707070707,
          "Female Percentage": "7.1%"
        },
        {
          "Year": 1980,
          "Continent": "Africa",
          "Female_Percentage": 0.1524590163934426,
          "Female Percentage": "15.2%"
        },
        {
          "Year": 1984,
          "Continent": "Africa",
          "Female_Percentage": 0.09419354838709676,
          "Female Percentage": "9.4%"
        },
        {
          "Year": 1988,
          "Continent": "Africa",
          "Female_Percentage": 0.13974799541809851,
          "Female Percentage": "14.0%"
        },
        {
          "Year": 1992,
          "Continent": "Africa",
          "Female_Percentage": 0.22341568206229864,
          "Female Percentage": "22.3%"
        },
        {
          "Year": 1996,
          "Continent": "Africa",
          "Female_Percentage": 0.2462077012835473,
          "Female Percentage": "24.6%"
        },
        {
          "Year": 2000,
          "Continent": "Africa",
          "Female_Percentage": 0.3296370967741936,
          "Female Percentage": "33.0%"
        },
        {
          "Year": 2004,
          "Continent": "Africa",
          "Female_Percentage": 0.33407572383073497,
          "Female Percentage": "33.4%"
        },
        {
          "Year": 2008,
          "Continent": "Africa",
          "Female_Percentage": 0.3874734607218684,
          "Female Percentage": "38.7%"
        },
        {
          "Year": 2012,
          "Continent": "Africa",
          "Female_Percentage": 0.399581589958159,
          "Female Percentage": "40.0%"
        },
        {
          "Year": 2016,
          "Continent": "Africa",
          "Female_Percentage": 0.3836772983114447,
          "Female Percentage": "38.4%"
        },
        {
          "Year": 1896,
          "Continent": "Asia",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1900,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1904,
          "Continent": "Asia",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1906,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1908,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1912,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1920,
          "Continent": "Asia",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1924,
          "Continent": "Asia",
          "Female_Percentage": 0.033707865168539325,
          "Female Percentage": "3.4%"
        },
        {
          "Year": 1928,
          "Continent": "Asia",
          "Female_Percentage": 0.015873015873015872,
          "Female Percentage": "1.6%"
        },
        {
          "Year": 1932,
          "Continent": "Asia",
          "Female_Percentage": 0.11203319502074688,
          "Female Percentage": "11.2%"
        },
        {
          "Year": 1936,
          "Continent": "Asia",
          "Female_Percentage": 0.057620817843866176,
          "Female Percentage": "5.8%"
        },
        {
          "Year": 1948,
          "Continent": "Asia",
          "Female_Percentage": 0.0069124423963133645,
          "Female Percentage": "0.7%"
        },
        {
          "Year": 1952,
          "Continent": "Asia",
          "Female_Percentage": 0.065439672801636,
          "Female Percentage": "6.5%"
        },
        {
          "Year": 1956,
          "Continent": "Asia",
          "Female_Percentage": 0.1060126582278481,
          "Female Percentage": "10.6%"
        },
        {
          "Year": 1960,
          "Continent": "Asia",
          "Female_Percentage": 0.129366106080207,
          "Female Percentage": "12.9%"
        },
        {
          "Year": 1964,
          "Continent": "Asia",
          "Female_Percentage": 0.14587593728698026,
          "Female Percentage": "14.6%"
        },
        {
          "Year": 1968,
          "Continent": "Asia",
          "Female_Percentage": 0.17119244391971666,
          "Female Percentage": "17.1%"
        },
        {
          "Year": 1972,
          "Continent": "Asia",
          "Female_Percentage": 0.14781746031746032,
          "Female Percentage": "14.8%"
        },
        {
          "Year": 1976,
          "Continent": "Asia",
          "Female_Percentage": 0.16761041902604756,
          "Female Percentage": "16.8%"
        },
        {
          "Year": 1980,
          "Continent": "Asia",
          "Female_Percentage": 0.1494661921708185,
          "Female Percentage": "14.9%"
        },
        {
          "Year": 1984,
          "Continent": "Asia",
          "Female_Percentage": 0.2409855769230769,
          "Female Percentage": "24.1%"
        },
        {
          "Year": 1988,
          "Continent": "Asia",
          "Female_Percentage": 0.3037466547725245,
          "Female Percentage": "30.4%"
        },
        {
          "Year": 1992,
          "Continent": "Asia",
          "Female_Percentage": 0.31186440677966104,
          "Female Percentage": "31.2%"
        },
        {
          "Year": 1996,
          "Continent": "Asia",
          "Female_Percentage": 0.3821571238348868,
          "Female Percentage": "38.2%"
        },
        {
          "Year": 2000,
          "Continent": "Asia",
          "Female_Percentage": 0.39642620780939775,
          "Female Percentage": "39.6%"
        },
        {
          "Year": 2004,
          "Continent": "Asia",
          "Female_Percentage": 0.4359058207979071,
          "Female Percentage": "43.6%"
        },
        {
          "Year": 2008,
          "Continent": "Asia",
          "Female_Percentage": 0.43423423423423424,
          "Female Percentage": "43.4%"
        },
        {
          "Year": 2012,
          "Continent": "Asia",
          "Female_Percentage": 0.4599396580623533,
          "Female Percentage": "46.0%"
        },
        {
          "Year": 2016,
          "Continent": "Asia",
          "Female_Percentage": 0.4653897849462366,
          "Female Percentage": "46.5%"
        },
        {
          "Year": 1896,
          "Continent": "Europe",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1900,
          "Continent": "Europe",
          "Female_Percentage": 0.012528473804100227,
          "Female Percentage": "1.3%"
        },
        {
          "Year": 1904,
          "Continent": "Europe",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1906,
          "Continent": "Europe",
          "Female_Percentage": 0.006905210295040804,
          "Female Percentage": "0.7%"
        },
        {
          "Year": 1908,
          "Continent": "Europe",
          "Female_Percentage": 0.01800076599004213,
          "Female Percentage": "1.8%"
        },
        {
          "Year": 1912,
          "Continent": "Europe",
          "Female_Percentage": 0.024897480960749854,
          "Female Percentage": "2.5%"
        },
        {
          "Year": 1920,
          "Continent": "Europe",
          "Female_Percentage": 0.03142943487458446,
          "Female Percentage": "3.1%"
        },
        {
          "Year": 1924,
          "Continent": "Europe",
          "Female_Percentage": 0.05149330587023687,
          "Female Percentage": "5.1%"
        },
        {
          "Year": 1928,
          "Continent": "Europe",
          "Female_Percentage": 0.0821664464993395,
          "Female Percentage": "8.2%"
        },
        {
          "Year": 1932,
          "Continent": "Europe",
          "Female_Percentage": 0.10588235294117647,
          "Female Percentage": "10.6%"
        },
        {
          "Year": 1936,
          "Continent": "Europe",
          "Female_Percentage": 0.06700091157702825,
          "Female Percentage": "6.7%"
        },
        {
          "Year": 1948,
          "Continent": "Europe",
          "Female_Percentage": 0.1073929961089494,
          "Female Percentage": "10.7%"
        },
        {
          "Year": 1952,
          "Continent": "Europe",
          "Female_Percentage": 0.20599325262949,
          "Female Percentage": "20.6%"
        },
        {
          "Year": 1956,
          "Continent": "Europe",
          "Female_Percentage": 0.20808451998162608,
          "Female Percentage": "20.8%"
        },
        {
          "Year": 1960,
          "Continent": "Europe",
          "Female_Percentage": 0.19808861859252824,
          "Female Percentage": "19.8%"
        },
        {
          "Year": 1964,
          "Continent": "Europe",
          "Female_Percentage": 0.19008009858287125,
          "Female Percentage": "19.0%"
        },
        {
          "Year": 1968,
          "Continent": "Europe",
          "Female_Percentage": 0.20454545454545456,
          "Female Percentage": "20.5%"
        },
        {
          "Year": 1972,
          "Continent": "Europe",
          "Female_Percentage": 0.22300968580203165,
          "Female Percentage": "22.3%"
        },
        {
          "Year": 1976,
          "Continent": "Europe",
          "Female_Percentage": 0.2362555720653789,
          "Female Percentage": "23.6%"
        },
        {
          "Year": 1980,
          "Continent": "Europe",
          "Female_Percentage": 0.257801108194809,
          "Female Percentage": "25.8%"
        },
        {
          "Year": 1984,
          "Continent": "Europe",
          "Female_Percentage": 0.2688271604938272,
          "Female Percentage": "26.9%"
        },
        {
          "Year": 1988,
          "Continent": "Europe",
          "Female_Percentage": 0.29081000743126084,
          "Female Percentage": "29.1%"
        },
        {
          "Year": 1992,
          "Continent": "Europe",
          "Female_Percentage": 0.3262682418346073,
          "Female Percentage": "32.6%"
        },
        {
          "Year": 1996,
          "Continent": "Europe",
          "Female_Percentage": 0.3664026677782409,
          "Female Percentage": "36.6%"
        },
        {
          "Year": 2000,
          "Continent": "Europe",
          "Female_Percentage": 0.38596989491621697,
          "Female Percentage": "38.6%"
        },
        {
          "Year": 2004,
          "Continent": "Europe",
          "Female_Percentage": 0.4022806004618938,
          "Female Percentage": "40.2%"
        },
        {
          "Year": 2008,
          "Continent": "Europe",
          "Female_Percentage": 0.4252481849162839,
          "Female Percentage": "42.5%"
        },
        {
          "Year": 2012,
          "Continent": "Europe",
          "Female_Percentage": 0.4477747502270663,
          "Female Percentage": "44.8%"
        },
        {
          "Year": 2016,
          "Continent": "Europe",
          "Female_Percentage": 0.4510353417406197,
          "Female Percentage": "45.1%"
        },
        {
          "Year": 1896,
          "Continent": "North America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1900,
          "Continent": "North America",
          "Female_Percentage": 0.05960264900662252,
          "Female Percentage": "6.0%"
        },
        {
          "Year": 1904,
          "Continent": "North America",
          "Female_Percentage": 0.013605442176870748,
          "Female Percentage": "1.4%"
        },
        {
          "Year": 1906,
          "Continent": "North America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1908,
          "Continent": "North America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1912,
          "Continent": "North America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1920,
          "Continent": "North America",
          "Female_Percentage": 0.03942652329749104,
          "Female Percentage": "3.9%"
        },
        {
          "Year": 1924,
          "Continent": "North America",
          "Female_Percentage": 0.05843071786310518,
          "Female Percentage": "5.8%"
        },
        {
          "Year": 1928,
          "Continent": "North America",
          "Female_Percentage": 0.11,
          "Female Percentage": "11.0%"
        },
        {
          "Year": 1932,
          "Continent": "North America",
          "Female_Percentage": 0.14641148325358852,
          "Female Percentage": "14.6%"
        },
        {
          "Year": 1936,
          "Continent": "North America",
          "Female_Percentage": 0.1221264367816092,
          "Female Percentage": "12.2%"
        },
        {
          "Year": 1948,
          "Continent": "North America",
          "Female_Percentage": 0.11932418162618795,
          "Female Percentage": "11.9%"
        },
        {
          "Year": 1952,
          "Continent": "North America",
          "Female_Percentage": 0.16042154566744732,
          "Female Percentage": "16.0%"
        },
        {
          "Year": 1956,
          "Continent": "North America",
          "Female_Percentage": 0.19484240687679086,
          "Female Percentage": "19.5%"
        },
        {
          "Year": 1960,
          "Continent": "North America",
          "Female_Percentage": 0.21568627450980396,
          "Female Percentage": "21.6%"
        },
        {
          "Year": 1964,
          "Continent": "North America",
          "Female_Percentage": 0.2101661779081134,
          "Female Percentage": "21.0%"
        },
        {
          "Year": 1968,
          "Continent": "North America",
          "Female_Percentage": 0.2272957889396245,
          "Female Percentage": "22.7%"
        },
        {
          "Year": 1972,
          "Continent": "North America",
          "Female_Percentage": 0.23755924170616116,
          "Female Percentage": "23.8%"
        },
        {
          "Year": 1976,
          "Continent": "North America",
          "Female_Percentage": 0.27378964941569284,
          "Female Percentage": "27.4%"
        },
        {
          "Year": 1980,
          "Continent": "North America",
          "Female_Percentage": 0.17372881355932204,
          "Female Percentage": "17.4%"
        },
        {
          "Year": 1984,
          "Continent": "North America",
          "Female_Percentage": 0.3223987698616094,
          "Female Percentage": "32.2%"
        },
        {
          "Year": 1988,
          "Continent": "North America",
          "Female_Percentage": 0.32998324958123953,
          "Female Percentage": "33.0%"
        },
        {
          "Year": 1992,
          "Continent": "North America",
          "Female_Percentage": 0.3336653386454183,
          "Female Percentage": "33.4%"
        },
        {
          "Year": 1996,
          "Continent": "North America",
          "Female_Percentage": 0.3953257086026852,
          "Female Percentage": "39.5%"
        },
        {
          "Year": 2000,
          "Continent": "North America",
          "Female_Percentage": 0.4241469816272966,
          "Female Percentage": "42.4%"
        },
        {
          "Year": 2004,
          "Continent": "North America",
          "Female_Percentage": 0.4470720720720721,
          "Female Percentage": "44.7%"
        },
        {
          "Year": 2008,
          "Continent": "North America",
          "Female_Percentage": 0.4338074398249453,
          "Female Percentage": "43.4%"
        },
        {
          "Year": 2012,
          "Continent": "North America",
          "Female_Percentage": 0.4791666666666667,
          "Female Percentage": "47.9%"
        },
        {
          "Year": 2016,
          "Continent": "North America",
          "Female_Percentage": 0.4955947136563877,
          "Female Percentage": "49.6%"
        },
        {
          "Year": 1896,
          "Continent": "Oceania",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1900,
          "Continent": "Oceania",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1904,
          "Continent": "Oceania",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1906,
          "Continent": "Oceania",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1908,
          "Continent": "Oceania",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1912,
          "Continent": "Oceania",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1920,
          "Continent": "Oceania",
          "Female_Percentage": 0.14285714285714285,
          "Female Percentage": "14.3%"
        },
        {
          "Year": 1924,
          "Continent": "Oceania",
          "Female_Percentage": 0.045454545454545456,
          "Female Percentage": "4.5%"
        },
        {
          "Year": 1928,
          "Continent": "Oceania",
          "Female_Percentage": 0.2857142857142857,
          "Female Percentage": "28.6%"
        },
        {
          "Year": 1932,
          "Continent": "Oceania",
          "Female_Percentage": 0.12244897959183673,
          "Female Percentage": "12.2%"
        },
        {
          "Year": 1936,
          "Continent": "Oceania",
          "Female_Percentage": 0.125,
          "Female Percentage": "12.5%"
        },
        {
          "Year": 1948,
          "Continent": "Oceania",
          "Female_Percentage": 0.17117117117117114,
          "Female Percentage": "17.1%"
        },
        {
          "Year": 1952,
          "Continent": "Oceania",
          "Female_Percentage": 0.1375,
          "Female Percentage": "13.8%"
        },
        {
          "Year": 1956,
          "Continent": "Oceania",
          "Female_Percentage": 0.1729957805907173,
          "Female Percentage": "17.3%"
        },
        {
          "Year": 1960,
          "Continent": "Oceania",
          "Female_Percentage": 0.18787878787878787,
          "Female Percentage": "18.8%"
        },
        {
          "Year": 1964,
          "Continent": "Oceania",
          "Female_Percentage": 0.2375,
          "Female Percentage": "23.8%"
        },
        {
          "Year": 1968,
          "Continent": "Oceania",
          "Female_Percentage": 0.25862068965517243,
          "Female Percentage": "25.9%"
        },
        {
          "Year": 1972,
          "Continent": "Oceania",
          "Female_Percentage": 0.2356020942408377,
          "Female Percentage": "23.6%"
        },
        {
          "Year": 1976,
          "Continent": "Oceania",
          "Female_Percentage": 0.2383419689119171,
          "Female Percentage": "23.8%"
        },
        {
          "Year": 1980,
          "Continent": "Oceania",
          "Female_Percentage": 0.29949238578680204,
          "Female Percentage": "29.9%"
        },
        {
          "Year": 1984,
          "Continent": "Oceania",
          "Female_Percentage": 0.2949640287769784,
          "Female Percentage": "29.5%"
        },
        {
          "Year": 1988,
          "Continent": "Oceania",
          "Female_Percentage": 0.2690972222222222,
          "Female Percentage": "26.9%"
        },
        {
          "Year": 1992,
          "Continent": "Oceania",
          "Female_Percentage": 0.3381712626995646,
          "Female Percentage": "33.8%"
        },
        {
          "Year": 1996,
          "Continent": "Oceania",
          "Female_Percentage": 0.3949801849405548,
          "Female Percentage": "39.5%"
        },
        {
          "Year": 2000,
          "Continent": "Oceania",
          "Female_Percentage": 0.4650934119960669,
          "Female Percentage": "46.5%"
        },
        {
          "Year": 2004,
          "Continent": "Oceania",
          "Female_Percentage": 0.4480286738351255,
          "Female Percentage": "44.8%"
        },
        {
          "Year": 2008,
          "Continent": "Oceania",
          "Female_Percentage": 0.4597839135654262,
          "Female Percentage": "46.0%"
        },
        {
          "Year": 2012,
          "Continent": "Oceania",
          "Female_Percentage": 0.4623115577889447,
          "Female Percentage": "46.2%"
        },
        {
          "Year": 2016,
          "Continent": "Oceania",
          "Female_Percentage": 0.4833141542002302,
          "Female Percentage": "48.3%"
        },
        {
          "Year": 1896,
          "Continent": "South America",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1900,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1904,
          "Continent": "South America",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1906,
          "Continent": "South America",
          "Female_Percentage": null,
          "Female Percentage": "nan%"
        },
        {
          "Year": 1908,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1912,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1920,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1924,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1928,
          "Continent": "South America",
          "Female_Percentage": 0,
          "Female Percentage": "0.0%"
        },
        {
          "Year": 1932,
          "Continent": "South America",
          "Female_Percentage": 0.023809523809523808,
          "Female Percentage": "2.4%"
        },
        {
          "Year": 1936,
          "Continent": "South America",
          "Female_Percentage": 0.03205128205128205,
          "Female Percentage": "3.2%"
        },
        {
          "Year": 1948,
          "Continent": "South America",
          "Female_Percentage": 0.08225806451612902,
          "Female Percentage": "8.2%"
        },
        {
          "Year": 1952,
          "Continent": "South America",
          "Female_Percentage": 0.07068607068607069,
          "Female Percentage": "7.1%"
        },
        {
          "Year": 1956,
          "Continent": "South America",
          "Female_Percentage": 0.021428571428571432,
          "Female Percentage": "2.1%"
        },
        {
          "Year": 1960,
          "Continent": "South America",
          "Female_Percentage": 0.03523035230352303,
          "Female Percentage": "3.5%"
        },
        {
          "Year": 1964,
          "Continent": "South America",
          "Female_Percentage": 0.04132231404958678,
          "Female Percentage": "4.1%"
        },
        {
          "Year": 1968,
          "Continent": "South America",
          "Female_Percentage": 0.15560165975103735,
          "Female Percentage": "15.6%"
        },
        {
          "Year": 1972,
          "Continent": "South America",
          "Female_Percentage": 0.117096018735363,
          "Female Percentage": "11.7%"
        },
        {
          "Year": 1976,
          "Continent": "South America",
          "Female_Percentage": 0.2050561797752809,
          "Female Percentage": "20.5%"
        },
        {
          "Year": 1980,
          "Continent": "South America",
          "Female_Percentage": 0.14788732394366194,
          "Female Percentage": "14.8%"
        },
        {
          "Year": 1984,
          "Continent": "South America",
          "Female_Percentage": 0.13333333333333333,
          "Female Percentage": "13.3%"
        },
        {
          "Year": 1988,
          "Continent": "South America",
          "Female_Percentage": 0.2332155477031802,
          "Female Percentage": "23.3%"
        },
        {
          "Year": 1992,
          "Continent": "South America",
          "Female_Percentage": 0.2249560632688928,
          "Female Percentage": "22.5%"
        },
        {
          "Year": 1996,
          "Continent": "South America",
          "Female_Percentage": 0.2697095435684647,
          "Female Percentage": "27.0%"
        },
        {
          "Year": 2000,
          "Continent": "South America",
          "Female_Percentage": 0.366306027820711,
          "Female Percentage": "36.6%"
        },
        {
          "Year": 2004,
          "Continent": "South America",
          "Female_Percentage": 0.39811066126855604,
          "Female Percentage": "39.8%"
        },
        {
          "Year": 2008,
          "Continent": "South America",
          "Female_Percentage": 0.4339152119700748,
          "Female Percentage": "43.4%"
        },
        {
          "Year": 2012,
          "Continent": "South America",
          "Female_Percentage": 0.4207920792079208,
          "Female Percentage": "42.1%"
        },
        {
          "Year": 2016,
          "Continent": "South America",
          "Female_Percentage": 0.4156674660271783,
          "Female Percentage": "41.6%"
        }
      ]
    },
    {
      "name": "data_0",
      "source": "data-c9cd4958aa454941ccfb344427499b56",
      "transform": [
        {"type": "formula", "expr": "toNumber(datum[\"Year\"])", "as": "Year"},
        {"type": "filter", "expr": "(datum.symbol !== 'GOOG')"}
      ]
    },
    {
      "name": "row_domain",
      "source": "data_0",
      "transform": [{"type": "aggregate", "groupby": ["Continent"]}]
    }
  ],
  "signals": [
    {"name": "child_width", "value": 550},
    {"name": "child_height", "value": 80},
    {
      "name": "unit",
      "value": {},
      "on": [
        {"events": "mousemove", "update": "isTuple(group()) ? group() : unit"}
      ]
    },
    {
      "name": "selector072",
      "update": "{\"Year\": selector072_Year, \"Female_Percentage\": selector072_Female_Percentage}"
    },
    {"name": "selector072_Year"},
    {"name": "selector072_Female_Percentage"}
  ],
  "layout": {
    "padding": 20,
    "offset": {"rowTitle": 10},
    "columns": 1,
    "bounds": "full",
    "align": "all"
  },
  "marks": [
    {
      "name": "row-title",
      "type": "group",
      "role": "row-title",
      "title": {
        "text": "Continent",
        "orient": "left",
        "style": "guide-title",
        "offset": 10
      }
    },
    {
      "name": "row_header",
      "type": "group",
      "role": "row-header",
      "from": {"data": "row_domain"},
      "sort": {"field": "datum[\"Continent\"]", "order": "ascending"},
      "title": {
        "text": {
          "signal": "isValid(parent[\"Continent\"]) ? parent[\"Continent\"] : \"\"+parent[\"Continent\"]"
        },
        "orient": "left",
        "style": "guide-label",
        "frame": "group",
        "offset": 10
      },
      "encode": {"update": {"height": {"signal": "child_height"}}},
      "axes": [
        {
          "scale": "y",
          "orient": "left",
          "grid": false,
          "title": "Percentage",
          "labelOverlap": true,
          "tickCount": {"signal": "ceil(child_height/40)"},
          "zindex": 0
        }
      ]
    },
    {
      "name": "column_footer",
      "type": "group",
      "role": "column-footer",
      "encode": {"update": {"width": {"signal": "child_width"}}},
      "axes": [
        {
          "scale": "x",
          "orient": "bottom",
          "grid": false,
          "title": "Year",
          "labelFlush": true,
          "labelOverlap": true,
          "tickCount": {"signal": "ceil(child_width/40)"},
          "zindex": 0
        }
      ]
    },
    {
      "name": "cell",
      "type": "group",
      "style": "cell",
      "from": {
        "facet": {"name": "facet", "data": "data_0", "groupby": ["Continent"]}
      },
      "sort": {"field": ["datum[\"Continent\"]"], "order": ["ascending"]},
      "encode": {
        "update": {
          "width": {"signal": "child_width"},
          "height": {"signal": "child_height"}
        }
      },
      "signals": [
        {
          "name": "facet",
          "value": {},
          "on": [
            {
              "events": [{"source": "scope", "type": "mousemove"}],
              "update": "isTuple(facet) ? facet : group(\"cell\").datum"
            }
          ]
        },
        {
          "name": "selector072_Year",
          "on": [
            {
              "events": {"signal": "selector072_translate_delta"},
              "update": "panLinear(selector072_translate_anchor.extent_x, -selector072_translate_delta.x / child_width)"
            },
            {
              "events": {"signal": "selector072_zoom_delta"},
              "update": "zoomLinear(domain(\"x\"), selector072_zoom_anchor.x, selector072_zoom_delta)"
            },
            {
              "events": [{"source": "scope", "type": "dblclick"}],
              "update": "null"
            }
          ],
          "push": "outer"
        },
        {
          "name": "selector072_Female_Percentage",
          "on": [
            {
              "events": {"signal": "selector072_translate_delta"},
              "update": "panLinear(selector072_translate_anchor.extent_y, selector072_translate_delta.y / child_height)"
            },
            {
              "events": {"signal": "selector072_zoom_delta"},
              "update": "zoomLinear(domain(\"y\"), selector072_zoom_anchor.y, selector072_zoom_delta)"
            },
            {
              "events": [{"source": "scope", "type": "dblclick"}],
              "update": "null"
            }
          ],
          "push": "outer"
        },
        {
          "name": "selector072_tuple",
          "on": [
            {
              "events": [
                {"signal": "selector072_Year || selector072_Female_Percentage"}
              ],
              "update": "selector072_Year && selector072_Female_Percentage ? {unit: \"child\" + '__facet_row_' + (facet[\"Continent\"]), fields: selector072_tuple_fields, values: [selector072_Year,selector072_Female_Percentage]} : null"
            }
          ]
        },
        {
          "name": "selector072_tuple_fields",
          "value": [
            {"field": "Year", "channel": "x", "type": "R"},
            {"field": "Female_Percentage", "channel": "y", "type": "R"}
          ]
        },
        {
          "name": "selector072_translate_anchor",
          "value": {},
          "on": [
            {
              "events": [{"source": "scope", "type": "mousedown"}],
              "update": "{x: x(unit), y: y(unit), extent_x: domain(\"x\"), extent_y: domain(\"y\")}"
            }
          ]
        },
        {
          "name": "selector072_translate_delta",
          "value": {},
          "on": [
            {
              "events": [
                {
                  "source": "window",
                  "type": "mousemove",
                  "consume": true,
                  "between": [
                    {"source": "scope", "type": "mousedown"},
                    {"source": "window", "type": "mouseup"}
                  ]
                }
              ],
              "update": "{x: selector072_translate_anchor.x - x(unit), y: selector072_translate_anchor.y - y(unit)}"
            }
          ]
        },
        {
          "name": "selector072_zoom_anchor",
          "on": [
            {
              "events": [{"source": "scope", "type": "wheel", "consume": true}],
              "update": "{x: invert(\"x\", x(unit)), y: invert(\"y\", y(unit))}"
            }
          ]
        },
        {
          "name": "selector072_zoom_delta",
          "on": [
            {
              "events": [{"source": "scope", "type": "wheel", "consume": true}],
              "force": true,
              "update": "pow(1.001, event.deltaY * pow(16, event.deltaMode))"
            }
          ]
        },
        {
          "name": "selector072_modify",
          "on": [
            {
              "events": {"signal": "selector072_tuple"},
              "update": "modify(\"selector072_store\", selector072_tuple, true)"
            }
          ]
        }
      ],
      "marks": [
        {
          "name": "child_pathgroup",
          "type": "group",
          "from": {
            "facet": {
              "name": "faceted_path_child_main",
              "data": "facet",
              "groupby": ["Continent"]
            }
          },
          "encode": {
            "update": {
              "width": {"field": {"group": "width"}},
              "height": {"field": {"group": "height"}}
            }
          },
          "marks": [
            {
              "name": "child_marks",
              "type": "area",
              "clip": true,
              "style": ["area"],
              "sort": {"field": "datum[\"Year\"]"},
              "interactive": true,
              "from": {"data": "faceted_path_child_main"},
              "encode": {
                "update": {
                  "orient": {"value": "vertical"},
                  "fill": {"scale": "color", "field": "Continent"},
                  "tooltip": {
                    "signal": "{\"Year\": format(datum[\"Year\"], \"\"), \"Continent\": isValid(datum[\"Continent\"]) ? datum[\"Continent\"] : \"\"+datum[\"Continent\"], \"Female Percentage\": isValid(datum[\"Female Percentage\"]) ? datum[\"Female Percentage\"] : \"\"+datum[\"Female Percentage\"]}"
                  },
                  "description": {
                    "signal": "\"Continent\" + \": \" + (isValid(datum[\"Continent\"]) ? datum[\"Continent\"] : \"\"+datum[\"Continent\"]) + \"; \" + \"Year\" + \": \" + (format(datum[\"Year\"], \"\")) + \"; \" + \"Female Percentage\" + \": \" + (isValid(datum[\"Female Percentage\"]) ? datum[\"Female Percentage\"] : \"\"+datum[\"Female Percentage\"]) + \"; \" + \"Percentage\" + \": \" + (format(datum[\"Female_Percentage\"], \"\"))"
                  },
                  "x": {"scale": "x", "field": "Year"},
                  "y": {"scale": "y", "field": "Female_Percentage"},
                  "y2": {"scale": "y", "value": 0},
                  "defined": {
                    "signal": "isValid(datum[\"Year\"]) && isFinite(+datum[\"Year\"]) && isValid(datum[\"Female_Percentage\"]) && isFinite(+datum[\"Female_Percentage\"])"
                  }
                }
              }
            }
          ]
        }
      ],
      "axes": [
        {
          "scale": "x",
          "orient": "bottom",
          "gridScale": "y",
          "grid": true,
          "tickCount": {"signal": "ceil(child_width/40)"},
          "domain": false,
          "labels": false,
          "aria": false,
          "maxExtent": 0,
          "minExtent": 0,
          "ticks": false,
          "zindex": 0
        },
        {
          "scale": "y",
          "orient": "left",
          "gridScale": "x",
          "grid": true,
          "tickCount": {"signal": "ceil(child_height/40)"},
          "domain": false,
          "labels": false,
          "aria": false,
          "maxExtent": 0,
          "minExtent": 0,
          "ticks": false,
          "zindex": 0
        }
      ]
    }
  ],
  "scales": [
    {
      "name": "x",
      "type": "linear",
      "domain": {"data": "data_0", "field": "Year"},
      "domainRaw": {"signal": "selector072[\"Year\"]"},
      "range": [0, {"signal": "child_width"}],
      "nice": true,
      "zero": false
    },
    {
      "name": "y",
      "type": "linear",
      "domain": {"data": "data_0", "field": "Female_Percentage"},
      "domainRaw": {"signal": "selector072[\"Female_Percentage\"]"},
      "range": [{"signal": "child_height"}, 0],
      "nice": true,
      "zero": true
    },
    {
      "name": "color",
      "type": "ordinal",
      "domain": {"data": "data_0", "field": "Continent", "sort": true},
      "range": "category"
    }
  ],
  "legends": [{"fill": "color", "symbolType": "circle", "title": "Continent"}],
  "config": {
    "legend": {
      "cornerRadius": 10,
      "fillColor": "#EEEEEE",
      "labelFontSize": 14,
      "padding": 10,
      "strokeColor": "gray"
    },
    "style": {"group-title": {"fontSize": 18, "fill": "black"}},
    "axis": {"labelFontSize": 15, "titleFontSize": 12}
  }
}
vegaEmbed('#figure29', figure29);
</script>

### Home-Field Advantage
As discussed above, we first tried scatter plot with jitter. The x-axis is the countries that have ever hosted the Olympics and y-axis denotes the percentage of a medals earned by a country against the total number of medals in that year. Blue dots represent data when the country were not the host and the orange ones for when it was the host. See Figure 30.

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis-data/master/output/vis/g-2-7.png"  caption="Figure30: Scatter plot with jittering for home-field advantage" class="wide">}}

The blue dots were too packed. We later tried beeswarm plot coupled with box plot. Dots were shown much more clearly but one drawback is that we could not see the density distribution of all the dots very well. Density distribution was important in this case because it would allow an easier comparison between the medal percentage when a country was a host and that when it was not. See Figure 31. 

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis-data/master/output/vis/g-2-8.png" class="wide">}}
<div class="caption-up-a-little">Figure 31: Beeswarm plot for home-field advantage</div>

To show density distribution of medal percentages, we used kernel density estimation in a small multiple. The x-axis is the medal percentage and the y-axis is the probability density. We used a red arrow to denote when the country was a Olympics host. An arrow located at the tail would indicate the existence of home-field advantage. See Figure 32.

{{<figure src="/pics/g-2-9.png"  caption="Figure 32: KDE in small multiple for home-field advantage" class="wide">}}

### Medal Efficiency
As planned, first of all, we did data manipulation before plotting. Golds were given four points, Silver 2, and Bronze 1. Attendance without any medals was assigned to 0 point. A country’s “medal efficiency” was calculated as the quotient of total medal points and the total number of athletes participating over 120 years. Therefore, if a country / region has a medal efficiency of 0.5, it means that on average, each athlete of that country / region earned half a Bronze. 

We then plotted a choropleth map using orthographic projection. We applied Viridis color map where darker shades denote higher medal efficiency. To ensure interactivity, we made this map with the Plotly package. See Figure 33.

<div>                            <div id="1d1de98f-fc08-420a-a7cf-a4ec1d6de5dc" class="plotly-graph-div" style="height:660px; width:100%;"></div>            <script type="text/javascript">                                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("1d1de98f-fc08-420a-a7cf-a4ec1d6de5dc")) {                    Plotly.newPlot(                        "1d1de98f-fc08-420a-a7cf-a4ec1d6de5dc",                        [{"autocolorscale": false, "colorbar": {"tickprefix": "", "title": {"text": "Medal Efficiency"}}, "colorscale": [[0.0, "#440154"], [0.1111111111111111, "#482878"], [0.2222222222222222, "#3e4989"], [0.3333333333333333, "#31688e"], [0.4444444444444444, "#26828e"], [0.5555555555555556, "#1f9e89"], [0.6666666666666666, "#35b779"], [0.7777777777777778, "#6ece58"], [0.8888888888888888, "#b5de2b"], [1.0, "#fde725"]], "locationmode": "ISO-3", "locations": ["AFG", "BES", "ALB", "DZA", "AND", "AGO", "ATG", null, "ARG", "ARM", "ABW", "ASM", "AUS", "AUT", "AZE", "BHS", "BGD", "BRB", "BDI", "BEL", "BEN", "BMU", "BTN", "BIH", "BLZ", "BLR", null, "BOL", "BWA", "BRA", "BHR", "BRN", "BGR", "BFA", "CAF", "KHM", "CAN", "CYM", "COG", "TCD", "CHL", "CHN", "CIV", "CMR", "COD", "COK", "COL", "COM", "CPV", "CRI", "HRV", null, "CUB", "CYP", "CZE", "DNK", "DJI", "DMA", "DOM", "ECU", "EGY", "ERI", "SLV", "ESP", "EST", "ETH", null, "FJI", "FIN", "FRA", null, "FSM", "GAB", "GMB", "GBR", "GNB", null, "GEO", "GNQ", "DEU", "GHA", "GRC", "GRD", "GTM", "GIN", "GUM", "GUY", "HTI", "HKG", "HND", "HUN", "IDN", "IND", null, "IRN", "IRL", "IRQ", "ISL", "ISR", "VIR", "ITA", "VGB", "JAM", "JOR", "JPN", "KAZ", "KEN", "KGZ", "KIR", "KOR", null, "SAU", "KWT", "LAO", "LVA", "LBY", "LBR", "LCA", "LSO", "LBN", "LIE", "LTU", "LUX", "MDG", null, "MAR", "MYS", "MWI", "MDA", "MDV", "MEX", "MNG", null, "MKD", "MLI", "MLT", null, "MCO", "MOZ", "MUS", "MRT", "MMR", "NAM", null, "NIC", "NLD", "NPL", null, "NGA", "NER", "NOR", "NRU", "NZL", "OMN", "PAK", "PAN", "PRY", "PER", "PHL", "PSE", "PLW", "PNG", "POL", "PRT", "PRK", "PRI", "QAT", null, null, "ROU", "ZAF", "RUS", "RWA", null, "WSM", null, "SEN", "SYC", null, "KNA", "SLE", "SVN", "SMR", "SLB", "SOM", "SRB", "LKA", null, "STP", "SDN", "CHE", "SUR", "SVK", "SWE", "SWZ", "SYR", "TZA", null, "TON", "THA", "TJK", "TKM", "TLS", "TGO", "TWN", "TTO", "TUN", "TUR", "TUV", "ARE", null, "UGA", "UKR", null, null, "URY", "USA", "UZB", "VUT", "VEN", "VNM", "VCT", null, null, null, "YEM", null, null, "ZMB", "ZWE"], "marker": {"line": {"color": "rgb(0,0,0)", "width": 0.5}}, "reversescale": true, "text": ["Afghanistan", "Bonaire, Sint Eustatius", "Albania", "Algeria", "Andorra", "Angola", "Antigua and Barbuda", null, "Argentina", "Armenia", "Aruba", "American Samoa", "Australia", "Austria", "Azerbaijan", "Bahamas", "Bangladesh", "Barbados", "Burundi", "Belgium", "Benin", "Bermuda", "Bhutan", "Bosnia and Herzegovina", "Belize", "Belarus", null, "Bolivia", "Botswana", "Brazil", "Bahrain", "Brunei Darussalam", "Bulgaria", "Burkina Faso", "Central African Republic", "Cambodia", "Canada", "Cayman Islands", "Congo (Brazzaville)", "Chad", "Chile", "China", "C\\u00f4te d\'Ivoire", "Cameroon", "Congo (Kinshasa)", "Cook Islands", "Colombia", "Comoros", "Cape Verde", "Costa Rica", "Croatia", null, "Cuba", "Cyprus", "Czech Republic", "Denmark", "Djibouti", "Dominica", "Dominican Republic", "Ecuador", "Egypt", "Eritrea", "El Salvador", "Spain", "Estonia", "Ethiopia", null, "Fiji", "Finland", "France", null, "Micronesia", "Gabon", "Gambia", "United Kingdom", "Guinea-Bissau", null, "Georgia", "Equatorial Guinea", "Germany", "Ghana", "Greece", "Grenada", "Guatemala", "Guinea", "Guam", "Guyana", "Haiti", "Hong Kong", "Honduras", "Hungary", "Indonesia", "India", null, "Iran", "Ireland", "Iraq", "Iceland", "Israel", "Virgin Islands, U.S.", "Italy", "Virgin Islands, British", "Jamaica", "Jordan", "Japan", "Kazakhstan", "Kenya", "Kyrgyzstan", "Kiribati", "Korea, South", null, "Saudi Arabia", "Kuwait", "Laos", "Latvia", "Libya", "Liberia", "Saint Lucia", "Lesotho", "Lebanon", "Liechtenstein", "Lithuania", "Luxembourg", "Madagascar", null, "Morocco", "Malaysia", "Malawi", "Moldova", "Maldives", "Mexico", "Mongolia", null, "Macedonia", "Mali", "Malta", null, "Monaco", "Mozambique", "Mauritius", "Mauritania", "Myanmar", "Namibia", null, "Nicaragua", "Netherlands", "Nepal", null, "Nigeria", "Niger", "Norway", "Nauru", "New Zealand", "Oman", "Pakistan", "Panama", "Paraguay", "Peru", "Philippines", "Palestine", "Palau", "Papua New Guinea", "Poland", "Portugal", "Korea, North", "Puerto Rico", "Qatar", null, null, "Romania", "South Africa", "Russian Federation", "Rwanda", null, "Samoa", null, "Senegal", "Seychelles", null, "Saint Kitts and Nevis", "Sierra Leone", "Slovenia", "San Marino", "Solomon Islands", "Somalia", "Serbia", "Sri Lanka", null, "Sao Tome and Principe", "Sudan", "Switzerland", "Suriname", "Slovakia", "Sweden", "Swaziland", "Syria", "Tanzania", null, "Tonga", "Thailand", "Tajikistan", "Turkmenistan", "Timor-Leste", "Togo", "Chinese Taipei", "Trinidad and Tobago", "Tunisia", "Turkey", "Tuvalu", "United Arab Emirates", null, "Uganda", "Ukraine", null, null, "Uruguay", "United States of America", "Uzbekistan", "Vanuatu", "Venezuela", "Vietnam", "Saint Vincent and the", null, null, null, "Yemen", null, null, "Zambia", "Zimbabwe"], "type": "choropleth", "z": [0.02, 0.03, 0.0, 0.07, 0.0, 0.0, 0.0, 1.08, 0.22, 0.16, 0.0, 0.0, 0.39, 0.12, 0.29, 0.25, 0.0, 0.0, 0.15, 0.26, 0.0, 0.0, 0.0, 0.0, 0.0, 0.17, 0.08, 0.0, 0.02, 0.26, 0.06, 0.0, 0.22, 0.0, 0.0, 0.0, 0.21, 0.0, 0.0, 0.0, 0.07, 0.52, 0.04, 0.27, 0.0, 0.0, 0.05, 0.0, 0.0, 0.03, 0.49, 0.0, 0.42, 0.01, 0.15, 0.39, 0.03, 0.0, 0.06, 0.02, 0.03, 0.02, 0.0, 0.22, 0.18, 0.34, 0.86, 0.23, 0.28, 0.34, 0.43, 0.0, 0.03, 0.0, 0.42, 0.0, 1.02, 0.25, 0.0, 0.54, 0.07, 0.18, 0.11, 0.0, 0.0, 0.0, 0.01, 0.1, 0.01, 0.0, 0.45, 0.22, 0.44, 0.1, 0.2, 0.06, 0.0, 0.08, 0.02, 0.01, 0.42, 0.0, 0.42, 0.05, 0.29, 0.18, 0.32, 0.02, 0.0, 0.34, 0.5, 0.03, 0.01, 0.0, 0.09, 0.0, 0.0, 0.0, 0.0, 0.03, 0.0, 0.16, 0.02, 0.0, 0.0, 0.07, 0.05, 0.0, 0.06, 0.0, 0.08, 0.09, 0.0, 0.02, 0.0, 0.0, 0.31, 0.01, 0.06, 0.01, 0.0, 0.0, 0.1, 0.0, 0.0, 0.38, 0.0, 0.0, 0.22, 0.06, 0.56, 0.0, 0.26, 0.0, 0.52, 0.04, 0.25, 0.06, 0.02, 0.0, 0.0, 0.0, 0.22, 0.04, 0.19, 0.02, 0.03, 0.0, 0.0, 0.36, 0.16, 0.58, 0.0, 0.0, 0.0, 0.42, 0.01, 0.0, 0.05, 0.0, 0.0, 0.11, 0.0, 0.0, 0.0, 0.44, 0.03, 0.0, 0.0, 0.02, 0.22, 0.07, 0.19, 0.42, 0.0, 0.04, 0.02, 0.21, 0.04, 0.09, 0.13, 0.0, 0.0, 0.02, 0.09, 0.17, 0.04, 0.21, 0.0, 0.03, 0.02, 0.06, 0.18, 0.0, 1.12, 0.27, 0.91, 0.14, 0.0, 0.03, 0.06, 0.0, 0.0, 0.25, 0.0, 0.0, 0.0, 0.46, 0.02, 0.25]}],                        {"geo": {"projection": {"type": "orthographic"}, "showcoastlines": true, "showframe": true, "showlakes": false}, "height": 660, "template": {"data": {"bar": [{"error_x": {"color": "#2a3f5f"}, "error_y": {"color": "#2a3f5f"}, "marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "bar"}], "barpolar": [{"marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "barpolar"}], "carpet": [{"aaxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "baxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "type": "carpet"}], "choropleth": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "choropleth"}], "contour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "contour"}], "contourcarpet": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "contourcarpet"}], "heatmap": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmap"}], "heatmapgl": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmapgl"}], "histogram": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "histogram"}], "histogram2d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2d"}], "histogram2dcontour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2dcontour"}], "mesh3d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "mesh3d"}], "parcoords": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "parcoords"}], "pie": [{"automargin": true, "type": "pie"}], "scatter": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter"}], "scatter3d": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter3d"}], "scattercarpet": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattercarpet"}], "scattergeo": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergeo"}], "scattergl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergl"}], "scattermapbox": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattermapbox"}], "scatterpolar": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolar"}], "scatterpolargl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolargl"}], "scatterternary": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterternary"}], "surface": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "surface"}], "table": [{"cells": {"fill": {"color": "#EBF0F8"}, "line": {"color": "white"}}, "header": {"fill": {"color": "#C8D4E3"}, "line": {"color": "white"}}, "type": "table"}]}, "layout": {"annotationdefaults": {"arrowcolor": "#2a3f5f", "arrowhead": 0, "arrowwidth": 1}, "coloraxis": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "colorscale": {"diverging": [[0, "#8e0152"], [0.1, "#c51b7d"], [0.2, "#de77ae"], [0.3, "#f1b6da"], [0.4, "#fde0ef"], [0.5, "#f7f7f7"], [0.6, "#e6f5d0"], [0.7, "#b8e186"], [0.8, "#7fbc41"], [0.9, "#4d9221"], [1, "#276419"]], "sequential": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "sequentialminus": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]]}, "colorway": ["#636efa", "#EF553B", "#00cc96", "#ab63fa", "#FFA15A", "#19d3f3", "#FF6692", "#B6E880", "#FF97FF", "#FECB52"], "font": {"color": "#2a3f5f"}, "geo": {"bgcolor": "white", "lakecolor": "white", "landcolor": "#E5ECF6", "showlakes": true, "showland": true, "subunitcolor": "white"}, "hoverlabel": {"align": "left"}, "hovermode": "closest", "mapbox": {"style": "light"}, "paper_bgcolor": "white", "plot_bgcolor": "#E5ECF6", "polar": {"angularaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "radialaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "scene": {"xaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "yaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "zaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}}, "shapedefaults": {"line": {"color": "#2a3f5f"}}, "ternary": {"aaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "baxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "caxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "title": {"x": 0.05}, "xaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}, "yaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}}}, "title": {"text": "An interactive choropleth map of Medal efficiency"}},                        {"responsive": true}                    )                };                            </script>        </div>

<div class="caption">Figure 33: Interactive choropleth for medal efficiency</div>

{{< block class="reminder" >}}
If you mess it up, just mouse over the figure, and in the menu shown on top of it, click the third last button to "Reset". And yes, you can rotate the globe!
{{< end >}}

We found this index both more accurate and intuitive. The reasons why it is more accurate have been outlined above. We believe that it is also more intuitive because, for example, for countries that still exist today, the highest medal efficiency is 0.91 for the United States of America. The fact that the highest is close to one makes it easier to compare between countries. 

### Ranking Sports
To rank sports according to the number of athletes, we first plotted a bar chart, each bar representing a category. As can be seen below, since there were too many categories, the names of sports overlapped to a degree that most of them were indistinguishable. Since there are around thirty sports, using colors is not an ideal option. 

We then thought about word cloud. In word cloud, the size of words is associated with the frequencies. This would make our ranking clearer. We did this visualization with the wordcloud package. See Figure 34.

{{<figure src="https://raw.githubusercontent.com/hongtaoh/olymvis/master/static/pics/g-4-2.png"  caption="Figure 34: Word cloud of sports ranking by number of participants in all past Summer Olympics" class="wide">}}

## Conclusion
### Research Question Recap
This paper answered four major questions:

- How does female participation at the Olympics, both overall and in each continent, change over time?
- Is there a home-field advantage at the Olympics?
- What is the medal efficiency for each country and region?
- Which sports have the highest number of participating athletes at the Olympics?

### Major Findings
Our visualizations demonstrated that:
- Both the total number of participating athletes and the percentage of female athletes in the Olympics has been increase. Female participation started from 0\% in Athens 1896 to 45\% in Rio 2016. 

- However, this growth in the rate of participation of women various across continents. The rate in Africa has always been lower than the global average except for during the 1930s. The rate in Asia and South America had also been always lower than the global average but caught up during the 1980s and 2000s, respectively. The rate in Europe, North America and Oceania has always been the same as or higher than the global mean.

- A country is more likely to have a higher degree of medal share when it hosts the Olympics. In other words, home-field advantage does seem to exist in the Olympics. 

- Among today’s countries and regions, the United States of America has the highest medal efficiency, 0.91. This means that on average, every American athlete almost earned a Bronze medal in the past Olympic Games. Medal efficiency for Russia, China, Pakistan, India, Germany, and Australia is also very high. We also found that medal efficiency had a high correlation with countries economic development. 

- Athletics, gymnastics, swimming, shooting and football are among the sports with the highest number of participating athletes. This might be because these sports have greater shares of total medals. It might also because there are many sub-categories within them.

### Reflections & Future Work
First, when visualizing changes in female participation, we found that stacked bar chart is effective in showing the comparisons between male and female. Stacked area chart does not provide very accurate percentage change, but it is good if we also want to show how the total number of athletes has been increasing. Seaborn FacetGrid function is useful for visualizing female participation by continent. Reference information set in grey in the background and highlighting the global average helps us make comparisons between continent and with the global average much clearer. Our next step is to do this graph with Altair so as to enable interactivity when we post it online. 

In our study into the home-field advantage, we realized that even with jittering, scatter plot is not effective at showing a large number of data points. Beeswarm plot with box plot is good at displaying all the points without overlapping, but its representation of density distribution is not very intuitive and direct. KDE in a small multiple is a much better method for showing the distribution clearly. KDE in this case is especially useful for examining home-field advantage because it shows the level of probability that a country gets a certain share of medals. 

Our introduction of “medal efficiency” contributes to the assessment of a country’s efficiency at obtaining Olympic medals. The choropleth we used allows to show all the countries and regions interactively. However, we acknowledged that it would have been better if it were a cartogram.  This might be our next step. 

Using word cloud is a very unique way to show the relative size of participation in various sports. The drawback is that some sports have two or more words in their names, and our processing of word clouds might not have been rendering their frequencies very accurately. That is why we see “water”, “art” and “competition” in the word cloud. We will fix this problem in our next step. 

We will publish it online as our profolio later. 

## References
Abrams, O. (2019, June 23). Why Female Athletes Earn Less Than Men Across Most Sports. Retrieved from [https://www.forbes.com/sites/oliviaabrams/2019/06/23/why-female-athletes-earn-less-than-men-across-most-sports/\#646f8eeb40fb](https://www.forbes.com/sites/oliviaabrams/2019/06/23/why-female-athletes-earn-less-than-men-across-most-sports/\#646f8eeb40fb).

Baker, C. N., Seymour, E., \&Zimbalist, A. (2019, April 18). Less Money, Less Media: How Female Athletes are Undervalued. Retrieved from https://msmagazine.com/2019/04/18/less-money-less-media-how-female-athletes-are-undervalued/.

Bian, X. (2005). Predicting Olympic medal counts: The effects of economic development on Olympic performance. *The park place economist, 13*(1), 37-44. 

Beutler, I. (2008). Sport serving development and peace: Achieving the goals of the United Nations through sport. *Sport in society, 11*(4), 359-369.

Bernard, A. B., \& Busse, M. R. (2004). Who wins the Olympic Games: Economic resources and medal totals. *Review of economics and statistics, 86*(1), 413-417.

COC. (2014, March 27). 10th-15th Olympic Games: 1936-1952. Retrieved from http://en.olympic.cn/games/summer/2004-03-27/121663.html. 

Cooky, C., Messner, M. A., \& Musto, M. (2015). “It’s dude time!” A quarter century of excluding women’s sports in televised news and highlight shows. *Communication \& Sport, 3*(3), 261-287.

Cottrell, M. P., & Nelson, T. (2011). Not just the Games? Power, protest and politics at the Olympics. *European Journal of International Relations, 17*(4), 729-753.

Darnell, S. C. (2012). Olympism in action, Olympic hosting and the politics of ‘sport for development and peace’: Investigating the development discourses of Rio 2016. *Sport in Society, 15*(6), 869-887.

Dutta, D. (2018). Analysing the Olympics (for last 120 yrs.). Retrieved from https://www.kaggle.com/duttadebadri/analysing-the-olympics-for-last-120-yrs.

Farmer, I. (2017, December 18). Why are female athletes paid less than male athletes? Retrieved from https://news.jrn.msu.edu/2017/12/why-are-female-athletes-paid-less-than-male-athletes/.

Forbes (2019). World's Highest Paid Athletes. Retrieved from https://www.forbes.com/athletes/list/\#tab:overall.

Ghildiyal, R. (2015). Role of sports in the development of an individual and role of psychology in sports. Retrieved from https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4381313/.

Giulianotti, R. (2015). The Beijing 2008 Olympics: Examining the interrelations of China, globalization, and soft power. *European Review, 23*(2), 286-296.

Goldblatt, D. (2016, August 4). Nobody wants to host the Olympic Games anymore. Can you blame them? Retrieved from https://qz.com/748894/nobody-wants-to-host-the-olympic-games-anymore-can-you-blame-them/.

Good, A. (2015, June 5). When it comes to women in sports, TV news tunes out. Retrieved from https://news.usc.edu/82382/when-it-comes-to-women-in-sports-tv-news-tunes-out/.

Grix, J. (2013). Sport politics and the Olympics. *Political studies review, 11*(1), 15-25.

Center for Strategic International Studies (n.d.). How dominant is China at the Olympic Games? Retrieved from https://chinapower.csis.org/dominant-china-olympic-games/.

International Table Tennis Federation. (2018). Tyko 2020 Qualification System Table Tennis (Eng). Retrieved from https://www.ittf.com/wp-content/uploads/2018/05/2018-05-14-Tokyo-2020-Qualification-system-Table-Tennis-eng.pdf

Johnson, I. (2008, August 13). Who's on First in Medals Race? Retrieved from https://www.wsj.com/articles/SB121856271893833843?ns=prod/accounts-wsj.

Klein, J. Z. (2008, August 23). The Medal Rankings: Which Country Leads the Olympics? [FINAL UPDATE]. Retrieved from https://beijing2008.blogs.nytimes.com/2008/08/23/the-medal-rankings-which-country-leads-the-olympics/.

Ludacer, R. (2018, February 6). No one wants to host the Olympics anymore - will they go away? Retrieved from https://www.businessinsider.com/future-olympics-no-country-wants-to-host-games-2018-2.

MacAloon, J. (1995). Politics and the Olympics: some new dimensions. Received from https://www.recercat.cat/bitstream/handle/2072/10632/WP053_eng.pdf?sequence=1

MacKenzie, M. (2019, July 16). Female Athletes Receive Only 4\% of Sports Media Coverage-Adidas Wants to Change That. Retrieved from https://www.glamour.com/story/female-athletes-receive-only-4-of-sports-media-coverage-adidas-wants-to-change-that.

Malfas, M., Theodoraki, E., \& Houlihan, B. (2004, September). Impacts of the Olympic Games as mega-events. In *Proceedings of the Institution of Civil Engineers-Municipal Engineer} (Vol. 157, No. 3, pp. 209-220*. Thomas Telford Ltd.

Mervosh, S., \& Caron, C. (2019, March 8). 8 Times Women in Sports Fought for Equality. Retrieved from https://www.nytimes.com/2019/03/08/sports/women-sports-equality.html.

Mower, J. (2012, January 1). London 2012: Olympic success is key to national pride. Retrieved from https://www.bbc.com/news/world-16245075.

Nunes, R.A. (2019). Women athletes in the Olympic Games. *Journal of Human Sport and Exercise. 2019, 14*(3): 674-683. doi:10.14198/jhse.2019.143.17

Osada, M., Ojima, M., Kurachi, Y., Miura, K., \& Kawamoto, T. (2016). Economic impact of the Tokyo 2020 Olympic games. Bank of Japan Reports and Research Paper, Tokyo, January. Retrieved from http://www.trustfu.com/Uploads/image/20180827/20180827212024_95674.pdf 

Rathke, A., \& Woitek, U. (2007). Economics and Olympics: An efficiency analysis. Available at SSRN 967629.

Sandercock, G., Beedie, C., \& Mann, S. (2016). Is Olympic inspiration associated with fitness and physical activity in English schoolchildren? A repeated cross-sectional comparison before and 18 months after London 2012. *British Medical Journal Open, 6*(11).

Soós, I., Martínez, J. C. F., \& Szabo, A. (2017). Before the Rio Games: A retrospective evaluation of the effects of the population size, GDP and national temperature on winning medals at the 2012 London Olympic Games. *Journal of Human Sport and Exercise, 12*(1), 246-250.

Wikipedia (n.d.). Retrieved from  https://en.wikipedia.org/wiki/Table_tennis_at_the_2020_Summer_Olympics_–_Qualification.

Warburton, D. E., Nicol, C. W., \& Bredin, S. S. (2006). Health benefits of physical activity: the evidence. *Cmaj, 174*(6), 801-809.

World Bank (2018). Population 2018. Retrieved from https://databank.worldbank.org/data/download/POP.pdf 