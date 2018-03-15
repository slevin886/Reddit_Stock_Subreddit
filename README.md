# Examining the virality of Reddit posts
## How choosing the right post title can (or can't) help drive engagement

Like it or not, most books are judged by their cover. A catchy title or graphic can be the difference between the best sellers' list and the literary wilderness. If you want to sell a lot of books (or get a lot of clicks for that matter), it is vital to know beforehand if you've picked the right title. 

In that light, I looked at two Reddit subreddits [Stocks](https://www.reddit.com/r/stocks/) and [Funny](https://www.reddit.com/r/funny/) to see what language patterns (if any) drive popularity. Looking separately at each subreddit's post titles, I applied several natural language proccessing (NLP) and machine learning techniques to identify the drivers of *virality- as measured by the number of comments elicited.

*(*I define 'virality'  loosely to be the difference between a post with comments below the 24th percentile (< 3 comments) and above the 75th percentile (> 14 comments))*

Using Reddit's API alongside the PRAW wrapper, I web scraped every post from the 'Stocks' subreddit between September 1st 2017 and February 19 2018 (a total 5566 posts). After cleaning the data and selecting meaningful features, I accurately classified 73% of posts as viral or not viral (from a 50% baseline). 

<img src="https://github.com/slevin886/Reddit_Stock_Subreddit/blob/master/images/Picture2.png" height="500" width="500">

The  words/stock symbols above were the best indicators of virality (left side = more likely to go viral, right side = less likely).
