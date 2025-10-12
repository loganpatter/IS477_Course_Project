**Overview**

The main goal of this project is to determine what kind of relationships exist, if any, between items such as income, unemployment rate or poverty rate with crime rate in a given area. The population in question will be the state of Texas, with samples of individual county data in order to attempt to come to relationship conclusions. 

**Research Questions**

The research questions for this project may change as I am able to find more available data to analyze, but at the moment the two research questions I absolutely aim to answer are:
1. How does the unemployment rate of an area impact the crime rate for said area?
2. How does the median household income of an area impact the crime rate for the area?

I know public data for unemployment rates and median household income exists for Texas counties through the FRED of St. Louis, but as stated previously, if I am able to find sufficient data for other economic indicators for Texas counties, I may add questions that pertain to that new available data.

**Team**

I am completing this project on my own, which was approved by the teaching staff. Thus, I’ll be carrying out each part of this project on my own.

**Datasets**

data.texas.gov hosts a dataset of the “Currently incarcerated inmate population with relevant demographic, offense, and parole information” for the state of Texas. This dataset is further delineated by the County where the offense occurred. Through their website, I was able to download this dataset as a CSV, which I will pull into my coding environment using pandas. https://data.texas.gov/dataset/High-Value-Dataset-August-2025/9b32-yeu6/about_data

As discussed previously, through the FRED (the Federal Reserve Bank of St. Louis) API I have thus far been able to find several available datasets for economic data for Texas counties including median household income and unemployment rate. As this project progresses, if other economic data catches my attention, I may add its use to this section as well. Below is a list of datasets I believe I will use as of now, though this list may change over the next couple of weeks.

1. Estimate of Median Household Income for Dallas County, TX (MHITX48113A052NCEN)
2. Estimate of Median Household Income for Harris County, TX (MHITX48201A052NCEN)
3. Estimate of Median Household Income for Austin County, TX (MHITX48015A052NCEN)
4. Estimate of Median Household Income for El Paso County, TX (MHITX48141A052NCEN)
5. Unemployment Rate in Dallas County, TX (LAUCN481130000000003A)
6. Unemployment Rate in Harris County, TX (LAUCN482010000000003A)
7. Unemployment Rate in El Paso County, TX (LAUCN481410000000003A)

https://fred.stlouisfed.org/tags/series?t=county%3Btx%3Busa

Each of these datasets is rather small, which is why I will be using so many of them. I will use API pull requests through the requests library in Python to get the data. I also believe, since each of these datasets is so small, I will likely combine the different economic indicators into a larger dataframe to allow for easier analysis.

**Timeline**

The data lifecycle relation and ethical data handling have both already been started as I have been looking for the data to use in the first place. The data collection is also currently underway, as is the storage and organization of said data. Data extraction, enrichment and integration will be handled over the next couple of weeks to ensure my research questions and project plan can be fully finalized before the end of the month. As we go over modules 9-15 in class, I will carry out the proper procedures within the week we learn it or the following week in order to stay on pace with project deadlines and requirements. Again, as I am doing this project without a partner, I will be responsible for each task in the project timeline.

**Constraints**

The main constraint I anticipate for this project relates to my ability to complete tasks on time. As I will be doing everything myself, I’ll need to stay disciplined with my work scheduling to ensure I don’t leave everything to the last minute and overwhelm myself with work. I would also like to ensure that the Texas county data I use covers the same counties for each economic indicator to help keep outside factors to a minimum, which will require more research on my part over the course of the next week or two. I should be able to figure out my datasets relatively easily, I’ll just need to pick a number of counties which have the proper datasets available which will take time to determine.

**Gaps**

I have no known gaps as of now.
