# _Mask-Free vs. Mask-Up Tweets and COVID Cases by County in the U.S._

For our project, we use three major sources of data: 
(1) Twitter data collected from the free Twitter API 
([TweePy](https://docs.tweepy.org/en/latest/)), (2) the 
[Johns Hopkins COVID-19 data map](https://coronavirus.jhu.edu/us-map), 
which lists COVID-19 cases and testing rates on a county 
basis, and (3) the 
[New York Times Mask Usage Data](https://github.com/nytimes/covid-19-data/tree/master/mask-use),
which provides estimates of mask usage by county.
The goal of the project is to study the link 
between following CDC recommended protocol of wearing a 
mask, and the rate of COVID-19 cases in a given county. 

For each county, we collected the percentage of the population
who have completed college. This information is used to explore
the effects of the education rate based on the county.

In this project, we graphically represent user beliefs 
on mask compliance by following the use of "mask free" and
the hashtag #maskfree on Twitter, which is generally 
used to indicate that a person does not wear a facial 
covering outside. We also look at the use of "mask up" and
the hashtag #maskup on Twitter to look at users who likely
wear a facial covering outside. We supplement the collected
Twitter data with the [New York Times Mask Usage by County
dataset](https://github.com/nytimes/covid-19-data/tree/master/mask-use)
from GitHub.

The geotag information was scraped from users who 
include these phrases and/or hashtags in their tweets in 
order to relate mask compliance to the amount of cases 
during a specified period of time (two-week intervals) 
as reported by the Johns Hopkins database. Lastly, 
we use data visualization techniques
(Seaborn, Pandas, MatPlotLib) to visually map the 
density of "mask free" and "mask up" usage by location, 
and supplement the Twitter data with charts that display 
the relationship between mask compliance and COVID-19 cases.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/)
to install TweePy.

```bash
pip install tweepy
```
You can also use the package manager to install Seaborn.
```bash
pip install seaborn
```

## Link to Google Drive

Some of our files are too large to upload to Github.
We used Google Drive to upload some of these files.

[Google Drive Folder](https://drive.google.com/drive/u/1/folders/1EXtgLpPaTqfppwBEWyIJsrbgVAsv4Xew)

## Instructions on Usage
**INCLUDE INSTRUCTIONS HERE**

(INCLUDE STEP BY STEP HOW TO ARRIVE TO THE ANALYSIS)

## Files

**1. county_info_new.csv** 

This csv file contains the information of all the 
counties used in the project. In this csv file, there 
is a column for the county name, the state where the 
county resides, the population density, the education rate,
the tier of the county based on education rate, the latitude
and longitude location, and the FIPS county code.

**2. mask-use-by-county.csv**

This csv file contains the estimated percentages of mask use
by county in the U.S. In this csv file, there is a column for
the FIPS county code and columns for how often the population
wears a mask (Never, Rarely, Sometimes, Frequently, or Always).
This csv file is used to supplement the Twitter data.

**3. time_series_covid19_confirmed_US.csv**

This csv file contains information about time series data for 
all counties within the U.S. In this csv file, there are 
columns for the FIPS county code, the county name, the state
where the county is located, the latitude and longitude, and 
COVID-19 cases in each county between the dates 1/22/20 and
3/16/21. This csv file is used to analyze the number of
COVID-19 cases by county.

**4. twitter_scraping.ipynb**

This ipynb file produces a dataframe of tweets for both 'mask free'
and 'mask up' tweets published on Twitter. The file also deletes
duplicates within the dataframe, leaving one copy of the duplicate
tweet behind in the first county it appeared in. After deleting
duplicates, the file then cleans the remaining tweets in the
dataframe and saves the output into a csv file 
(cleaned_tweets.csv).

**5. cleaned_maskfree_tweets.csv**

This csv file contains all the information scraped from
Twitter (using TweePy) using the search 'mask free'. 
In this csv file, there are columns for the county name,
the original tweet, the tweets list, the tweet as a string,
a slice of the tweet, and the tweet as text. This csv file
is merged with the New York Times Mask Usage data and the
Johns Hopkins COVID-19 data.

**6. cleaned_maskup_tweets.csv**

This csv file contains all the information scraped from
Twitter (using TweePy) using the search 'mask up'.
In this csv file, there are columns for the county name,
the original tweet, the tweets list, the tweet as a string,
a slice of the tweet, and the tweet as text. This csv file
is merged with the New York Times Mask Usage data and the
Johns Hopkins COVID-19 data.

**7. data_cleaning_for_analysis.ipynb**

This ipynb file merges together the 'mask-free' and
'mask-up' Twitter data collected 
(cleaned_maskfree_tweets.csv and cleaned_maskup_tweets.csv)
with the county data (county_info_new.csv) in order to gather 
the FIPS county codes and map education rates. 
The file then merges together the 
dataframe with the Johns Hopkins COVID-19 data 
(time_series_covid19_confirmed_US.csv) in order to map
COVID-19 cases to each county and each Tweet. Finally, the
file merges the dataframe with the New York Times Mask Usage
data (mask-use-by-county.csv), which looks at mask usage by 
county. The final dataframe helps with the analysis of 
'mask free' versus 'mask up' tweets against COVID-19 cases
and county mask usage. 

**8. finalproj_dataviz.ipynb**

This ipynb file uses pandas, matplotlib, numpy, and seaborn to 
help create visualizations of our final dataset. Our visualizations 
include bar graphs comparing number of 'mask free' versus 'mask up'
tweets, graphs and tables comparing education levels to number 
of 'mask free' versus 'mask up' Tweets, comparing the number of
'mask free' versus 'mask up' tweets to COVID-19 cases in 
each county, and comparing mask usage in each county compared
to COVID-19 cases in each county.


## Links to Data Sources
[TweePy](https://docs.tweepy.org/en/latest/)

[Johns Hopkins COVID-19 Data Map](https://coronavirus.jhu.edu/us-map)

[Johns Hopkins Time Series Data](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series)

[Density by County](https://en.wikipedia.org/wiki/County_statistics_of_the_United_States?fbclid=IwAR0zDzgZUOOdi4MkaWOu2MBOth7gOTqflmRgqePkPm-ZFh-NigKllrq7YgA)

[U.S. County Boundaries](https://public.opendatasoft.com/explore/dataset/us-county-boundaries/table/?disjunctive.statefp&disjunctive.countyfp&disjunctive.name&disjunctive.namelsad&disjunctive.stusab&disjunctive.state_name&fbclid=IwAR1bdkKaU6G0TLlCf2D4JhMfBxil_OuiOjTHZhZBFLksVixS8NKhFQ31SC4)

[Education Level by County](https://data.ers.usda.gov/reports.aspx?ID=17829)

[New York Times Mask Usage Data](https://github.com/nytimes/covid-19-data/tree/master/mask-use)