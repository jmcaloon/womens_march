# Women's March Twitter Analysis
Data science project analyzing Women's March tweets on twitter and scores given by folks over in <a href="https://statusofwomendata.org/" target="_blank">Status Of Women</a>

#### Team Members
* Monica Chiu .........mcsmocha@bu.edu
* Jess McAloon ........mcaloonj@bu.edu
* Joseph McMahan ......jmcmahan@bu.edu

## Part 1
The overall goal of the project is to analyze the tweets with the hashtag #WomensMarch to see if trends occur with the more common issues that face women and the locations of the people tweeting. The motivation of this project is to cluster tweets by location and similarity in order to see which areas tweet about which issues and which areas tweet the most, in order to determine which areas need more assistance with womens issues. We are going to use webscraping and the Twitter API to gain our information and use linear regression and kmeans to analyze and compile the data. We have webscraped <a href="https://statusofwomendata.org/" target="_blank">Status Of Women</a>,  a website run by the Institute for Women's Policy Research, which gives each state a report card based on how well it meets womens needs. By the end of our project, we hope to answer the following questions:
* Does a state's number of tweets with #womensmarch correlate at all with a state's report card score? In other words, do states that rank lower in terms of womens rights tend to have more tweets about womens issues?
* What are the most common topics/issues in tweets related to #womensmarch?
* Which cities were tweeting about #womensmarch?
* Do topics tweeted about differ by city?
* Overall, how do trends in the content and location of tweets relate to data from the Status of Women website and issues that affect women?

## Part 2

We are retrieving the tweets from Twitter using tweepy and modified code from Jefferson Henrique’s GetOldTweets (MIT License). We are getting 10,000 top tweets between the period from January 1st to January 31st of this year 2017 that has #WomensMarch in the tweets. We decided to get tweets from January since that’s when the movement started and hashtags were most common. We've retrieved the user, date, tweet text, location, and hashtags of each tweet, which can be found in output_got.csv. We currently have 1,000 tweets for testing purposes, but will use 10,000 tweets for our final project.

We will then cluster the tweets by location and similarity. Then, we'll plot these centroids by location and analyze to see if there’s a correlation between the number of tweets in a location and the scores available from web scraping report cards information on https://statusofwomendata.org/. We scraped that website and got each state's ranking in a number of issue areas: Employment, Health & Wellness, Political Participation, Poverty and Opportunity, Reproductive Rights, and Work & Family. Our scraping results can be found in state_rankings.csv.

## Part 3

For our preprocessing, we used the Twitter API to get all the tweets with #WomensMarch and extracted the ID, text, coordinates, and other hashtags used in the tweets. For the querysearch, we’re only getting the top 1,000 tweets so that the tweets we get should be better well thought out and more useful. For the locations, we’re going to clean the geo attribute by extracting only the state names from the location attribute since there are some without text or extraneous text. Then we'll translate the states into coordinates so we can plot the tweet clusters on a map. The state report cards on https://statusofwomendata.org/ have a number for each issue area and don't require any further cleaning.

We have began initial exploration of data analysis. We ran LDA on the tweet's text to extract the top 20 topics, and the 5 keywords that make up each topic. Our initial goal was to cluster by the topics we found, but we decided that clustering by hashtags (other than #womensmarch) would be more accurate, so we began implementing k-means to cluster by hashtag. So far we have only clustered by similarity, not location. All of our code is in the notebook in this repo.

## Part 4

We will continue tweaking our LDA and looking into other classification methods, and compare clusterings of topics vs clusterings of hashtags. We'll choose the most accurate and most feasible method. 

We will then also use linear regression to determine the correlation of a state's report card scores and number of tweets from that state. The issue areas in state_rankings.csv (or a subset of those areas) will be the independent variables, and the number of tweets from that state is the dependent variable that we're trying to predict.



## Part 5

#### ~~Milestone 1: Nov 17~~
* ~~Data retrieval~~
#### Milestone 2: Dec 1
*  Complete location cleaning (Monica)
*  Complete clustering (Jess)
#### Milestone 3: Dec 8
* Complete linear regression (Joe)
* Complete edit of kmeans clustering (Jess + Monica)
* Complete lda on cluster (Jess + Monica)

#### Milestone 4: Dec 12 
* Complete writeup and poster (all)






















