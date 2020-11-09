# About
This project was completed by [Zihui (Chris) Fang](https://github.com/zihfang/) and [Hongtao Hao](https://hongtaoh.com/), with **Equal Contribution**, as the final paper for Professor [Yong-Yeol Ahn](http://yongyeol.com/)'s [Data Visualization](https://yyahn.com/dviz-course/) course in 2019 Fall. 

## Summary

From the first modern Olympics in 1896 to Rio 2016, the Summer Olympic Games has been through 120 years. This study analyzed the [historical data](https://github.com/rgriff23/Olympic_history) about the Olympics and tried to answer four questions, i.e., 

- how female participation changed over the years and how these changes differed between continents,
- whether there is a home-field advantage at the Olympics,
- how "efficient" is each participating country and region to get medals, and 
- which sports had the highest number of participants. 

Results showed that both total number of athletes and the rate of female participation have been increasing in the past 120 years. Also, there seems to exist a home-field advantage. Third, medal efficiency is highly correlated with participating country or region's economic development. Finally, athletics, gymnastics, and swimming have the highest number of athletes.

## Our Contributions
Based on the above discussions of the previous visualizations on the topics we are addressing, our contributions are:

- One of first few attempts to explore female participation in the Summer Olympics over 120 years by continent. This new insight will be important because although data shows that overall female participation in the Olympics has been increasing dramatically, this might have been the case for each continent. Further investigation into the percentage of female athletes in each of the six continents (Asia, Europe, Africa, South America, North America, and Oceania) will reveal deeper information about the trend of female athletes participation. 
    
- Introducing KDE in examining home-field advantage in the Olympics. This method makes it possible to show the density of each host country’s performance distribution, which makes the comparison between “home” and “away” performance clearer. 
    
- Introduction of the concept of “medal efficiency”. Earlier attempts either lacked taking into account of “medal points” or unfairly included GDP and population in their formula. Our way of calculating medal efficiency, i.e., weighted medal points per athlete participating, can more accurately estimate each country’s efficiency of producing medals in the Summer Olympics. 

## Workflow

See [olymvis-data](https://github.com/hongtaoh/olymvis-data) for more details. 

## PDF & Tex
If you prefer reading in PDF: [Here](https://github.com/hongtaoh/olymvis/blob/master/static/tex-pdf/fang_hao_olymvis.pdf) is our study in PDF, and [here](https://github.com/hongtaoh/olymvis/blob/master/static/tex-pdf/fang_hao_olymvis.tex) is the tex source code for the PDF. 

## About the Website
This website is built with [Hugo](https://gohugo.io/). The theme is [XMin](https://themes.gohugo.io/hugo-xmin/) by [Yihui Xie](https://yihui.org/). 