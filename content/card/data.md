---
title: Data Processing
style: 'background: #f7f9fb;'
weight: 2
---
The main data set used in this project is the awesome [Olympic_history](https://github.com/rgriff23/Olympic_history) by [rgriff23](https://github.com/rgriff23).

Other complementary data sets:

- [continent.csv](https://github.com/hongtaoh/olymvis-data/blob/master/data_sources/continent.csv) is used for extracting the ISO-3166 three letter country code and the corresponding continent name.

- [host_countries.csv](https://github.com/hongtaoh/olymvis-data/blob/master/data_sources/host_countries.csv) is used in [vis 3](https://olymvis.netlify.app/vis3/).

- [continent_4.xlsx](https://github.com/hongtaoh/olymvis-data/blob/master/data_sources/continent_4.xlsx) is used to extract the IOC (International Olympic Committee) country codes and the ISO-3166 three letter country codes. We merge `continent_4` with `continent` to get the corresponding continent name of each IOC code. We then merge this with [summer.csv](https://github.com/hongtaoh/olymvis-data/blob/master/output/summer.csv) to produce [continent_percentage_tidy](https://github.com/hongtaoh/olymvis-data/blob/master/output/continent_percentage_tidy.csv) and [continent_percentage_untidy](https://github.com/hongtaoh/olymvis-data/blob/master/output/continent_percentage_untidy.csv), two of which we used to visualize [changes in female particiation in the Olympics in different continents](https://olymvis.netlify.app/vis2/).

For more detailed information about our data sources, and our codes for data manipulation and visualization, please check out our <a href = "https://github.com/hongtaoh/olymvis-data" style="padding-bottom: 1px;border-bottom: 1px solid;">olymvis-data</a> repository on GitHub.