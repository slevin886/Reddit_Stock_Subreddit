# Examining the virality of Reddit posts
## How choosing the right post title can (or can't) help drive engagement

Like it or not, most books are judged by their cover. A catchy title or graphic can be the difference between the best sellers' list and the literary wilderness. If you want to sell a lot of books (or get a lot of clicks for that matter), it is vital to know beforehand if you've picked the right title. 

In that light, I looked at two Reddit subreddits- [Stocks](https://www.reddit.com/r/stocks/) and [Funny](https://www.reddit.com/r/funny/) -to see what language patterns (if any) drive popularity. Looking separately at each subreddit's post titles, I applied several natural language proccessing (NLP) and machine learning techniques to identify the drivers of *virality- as measured by the number of comments elicited.

*(*I define 'virality'  loosely to be the difference between a post with comments below the 24th percentile (< 3 comments) and above the 75th percentile (> 14 comments))*

### Reddit Stocks
Using Reddit's API alongside the PRAW wrapper, I web scraped every post from the 'Stocks' subreddit between September 1st 2017 and February 19 2018 (a total 5566 posts). After cleaning the data and selecting meaningful features, I accurately classified 73% of posts as viral or not viral (from a 50% baseline). 

The  words/stock symbols below were the best indicators of virality (left side = more likely to go viral, right side = less likely).
<p align="center">
  <img src="https://github.com/slevin886/Reddit_Stock_Subreddit/blob/master/images/Picture2.png" height="500" width="500">
</p>
On Reddit, if not elsewhere, some compaines garner **more interest** (*ge*:General Electric, *xxii*:Twenty Second Century Group, etc.)and others **less interest** (*orcl*: Oracle, etc.). Overall, however, it is advantageous to include specific company names in your post's title. On the other hand, the words that drive down the likelihood of virality (like *curious* and *decent*) are vague or likely form part of a question.  

In general, superlatives (like *massive* above) and active verbs drive traffic and can increase the likelihood of virality.  Although as you can see below, sentence structure ( measurued by parts of speech) is not dramatically different between the two groups. 

*(the lighter blue/aqua on the bar peaks represents greater presence in viral titles, whereas brown at the peak represents greater presence in non-viral titles)*
<p align="center">
  <img src="https://github.com/slevin886/Reddit_Stock_Subreddit/blob/master/images/Picture6.png" height="300" width="700">
</p>
In addition to language features, I looked at how the time of day and the day of the week a user decides to post affected the  probability of virality.
<p align="center">
  <img src="https://github.com/slevin886/Reddit_Stock_Subreddit/blob/master/images/Picture4.png" height="350" width="400">
</p>
As you can see, posts submitted on Sunday and Monday had higher mean values for both comments and upvotes (the equivalent to 'liking' on facebook) as compared to other days of the week.
<p align="center">
  <img src="https://github.com/slevin886/Reddit_Stock_Subreddit/blob/master/images/Picture1.png" height="350" width="400">
</p>
In terms of time of day, posting at night- *particularly around 8pm* -is associated with large spikes in both the average number of comments received and number of upvotes. 

Interestingly, there was only very weak correlation between the length of a given title and its probabiltiy of going viral. 
<p align="center">
  <img src="https://github.com/slevin886/Reddit_Stock_Subreddit/blob/master/images/Picture15.png" height="350" width="400">
</p>
It is evident from the graphic above that both very short lengths and very long lengths have viral instances and that virality is pretty evenly dispersed across lengths. 

### Reddit Funny

Despite pulling a much larger dataset from the funny subreddit (32,789 observations), I was unable to predict virality at a significantly different rate from the baseline. Given the complexity of humor/sarcasm/irony, it is perhaps not surprising to find this result. Performing topic analysis, some of the more prevalent viral topics included, Logan Paul (a famous YouTube personality), Dads, and Pranks. Viral posts also were slightly *less* subjective and slightly *more* polarizing than non-viral posts. Why this may or not be the case will have to wait for a future analysis. 
