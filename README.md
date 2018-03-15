# Examining the virality of Reddit posts
## How choosing the right post title can (or can't) help drive engagement

Like it or not, most books (or articles/posts for that matter) are judged by their covers. A catchy title or graphic can be the difference between the best sellers' list and the literary wilderness. In that light, I looked at two Reddit subreddits [Stocks](https://www.reddit.com/r/stocks/) and [Funny](https://www.reddit.com/r/funny/) to see what language patterns (if any) drive popularity. Separately looking at the titles from the posts on each subreddit, I applied several natural language proccessing (NLP) and machine learning techniques to identify the drivers of 'virality'- as measured by the number of comments elicited.

*(NOTE: 'virality' is in quotes above because I defined it loosely to be the difference between a post being below the 24th percentile (< 3 comments) and above the 75th percentile (> 14 comments))*

Using Reddit's API alongside the PRAW wrapper, I web scraped every post from the 'Stocks' subreddit between September 1st 2017 and February 19 2018 (a total 5566 posts). After cleaning the data and selecting meaningful features, I used a logistic regression model to predict whether a post would go viral with 73% accuracy. 

<img src="https://github.com/slevin886/Reddit_Stock_Subreddit/blob/master/images/Picture2.png" height="500" width="500">

The  words/stock symbols above were the best indicators of virality (left side = more likely to go viral, right side = less likely).
