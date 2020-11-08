---
title: Recap
author: Chris Fang & Hongtao Hao
---
## Research Question Recap
This paper answered four major questions:

- How does female participation at the Olympics, both overall and in each continent, change over time?
- Is there a home-field advantage at the Olympics?
- What is the medal efficiency for each country and region?
- Which sports have the highest number of participating athletes at the Olympics?

## Major Finding
Our visualizations demonstrated that:
- Both the total number of participating athletes and the percentage of female athletes in the Olympics has been increase. Female participation started from 0\% in Athens 1896 to 45\% in Rio 2016. 

- However, this growth in the rate of participation of women various across continents. The rate in Africa has always been lower than the global average except for during the 1930s. The rate in Asia and South America had also been always lower than the global average but caught up during the 1980s and 2000s, respectively. The rate in Europe, North America and Oceania has always been the same as or higher than the global mean.

- A country is more likely to have a higher degree of medal share when it host the Olympics. In other words, home-field advantage does seem to exist in the Olympics. 

- Among today’s countries and regions, the United States of America has the highest medal efficiency, 0.91. This means that on average, every American athlete almost earned a Bronze medal in the past Olympic Games. Medal efficiency for Russia, China, Pakistan, India, Germany, and Australia is also very high. We also found that medal efficiency had a high correlation with countries economic development. 

- Athletics, gymnastics, swimming, shooting and football are among the sports with the highest number of participating athletes. This might be because these sports have greater shares of total medals. It might also because there are many sub-categories within them.

## Reflection & Future Work
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


