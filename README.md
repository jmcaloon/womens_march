# Women's March Twitter Analysis
Data science project analyzing Women's March tweets on twitter and scores given by folks over in [Status Of Women](https://statusofwomendata.org/)

## The Problem
#### Introduction and Motivation  
<ul>
    <li> The overall goal of the project is to analyze the tweets with the hashtag #WomensMarch to see if trends occur with the more common issues that face women and the locations of the people tweeting. The motivation of this project is to see which clusters in areas tweet about the most issues in an attempt to find where the most help could possibly be needed. We are going to use webscraping and the Twitter API to gain our information and use linear regression and kmeans to analyze and compile the data.</li>
    <li> The datasets we will use will be the Twitter API for tweets about issues surrounding women using the hashtag #WomensMarch which was used for the event earlier this year. We will also use [Status Of Women](https://statusofwomendata.org/), a website run by the Institute for Women's Policy Research to gain data for each state’s score on women’s issues. We will use webscraping techniques to gain this information and store it in a CSV for further use.</li>
</ul>

#### Our Process
<ul>
    <li> For each tweet with #WomensMarch, we’ll extract the ID of the tweets, the text, location (coordinates of where the tweet was sent from), and some other information that could be useful to us in our analysis and store them in a CSV. The scores will be used along with the location data from Twitter to see if a correlation exists. We will then write this data to a csv. Using the coordinates of the tweet and the text of the tweet, we can run k-means to cluster closeness and find the top issue tweeted about per cluster. Some examples of issues are birth control, wage gap, glass ceiling, discrimination, and assault. </li>
    <li> Once we have these clusters, we can scrape each state’s report card on https://statusofwomendata.org/ for the state’s score on a number of different women’s issues and write this data to another csv. (For example, we can check Iowa’s score using the link: https://statusofwomendata.org/explore-the-data/state-data/iowa/). We will run a linear regression algorithm to see if a low or high average score correlates to the frequency of tweets with #WomensMarch in that area. </li>
    <li> For the results, we will have the clusters on the tweets in a graph and find the top issue(s) within each cluster. We will have one figure for these clusters, using the tweets and the texts as the coordinates and another figure for the top issues (a chart or some other representation). We will have several tables containing the scores of a variety of women’s issues and a sample of the actual data for each table (will put more relevant topics on top). Another figure will be a graph of the linear regression done on the scores and the frequency of tweets. In addition to all of these, for a stark, side-by-side comparison, we will include a top tweet and the corresponding score and data facts. </li>
</ul>

#### Team Members
* Monica Chiu .........mcsmocha@bu.edu
* Jess McAloon ........mcaloonj@bu.edu
* Joseph McMahan ......jmcmahan@bu.edu
