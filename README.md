# Mask-Free vs. Mask-Up Tweets and COVID Cases by County in the U.S.

For our project, we use two sources of data: 
(1) Twitter data collected from the free Twitter API 
(TweePy), and (2) the Johns Hopkins COVID-19 data map, 
which lists COVID-19 cases and testing rates on a county 
basis. The goal of the project is to study the link 
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
wear a facial covering outside.


The geotag information was scraped from users who 
include these phrases and/or hashtags in their tweets in 
order to relate mask compliance to the amount of cases 
during a specified period of time (two-week intervals) 
as reported by the Johns Hopkins database. Lastly, 
we use Geopandas/folium to visually map the 
density of "mask free" and "mask up" usage by location, 
and supplement the Twitter data with charts that display 
the relationship between mask compliance and COVID-19 cases.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install TweePy.

```bash
!pip install tweepy
```

## Files
1. cleaned_maskfree_tweets.csv

2. cleaned_maskup_tweets.csv

3. cleaned_tweets_finalquery.csv

4. county_info.csv

5. twitter_maskfree.ipynb

6. twitter_maskup.ipynb

7. time_series_covid19_confirmed_US.csv


## Links to Data Sources
[TweePy](https://docs.tweepy.org/en/latest/)

[Johns Hopkins COVID-19 data map](https://coronavirus.jhu.edu/us-map)

[Density by County](https://en.wikipedia.org/wiki/County_statistics_of_the_United_States?fbclid=IwAR0zDzgZUOOdi4MkaWOu2MBOth7gOTqflmRgqePkPm-ZFh-NigKllrq7YgA)

[U.S. County Boundaries](https://public.opendatasoft.com/explore/dataset/us-county-boundaries/table/?disjunctive.statefp&disjunctive.countyfp&disjunctive.name&disjunctive.namelsad&disjunctive.stusab&disjunctive.state_name&fbclid=IwAR1bdkKaU6G0TLlCf2D4JhMfBxil_OuiOjTHZhZBFLksVixS8NKhFQ31SC4)

[Education Level by County](https://data.ers.usda.gov/reports.aspx?ID=17829)