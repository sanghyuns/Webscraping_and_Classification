# Project 3: Web Scraping & Classification

## Introduction

Reddit is a website that is a collection of interest-based communities also known as subreddits. Within each subreddit, users are able to create text, image, or video posts and others can upvote or downvote to express approval or disapproval regarding the content of the post. The upvotes and downvotes are the fed into an algorithm to determine an internal score for the post, which is then projected to the `hot` section of the homepage, if popular enough.

The goal of this project was to webscrape data from a website and determine which characteristics of a post on Reddit are most predictive of overall interaction on a thread (as measured by number of comments).

For this project, I chose the subreddit, `r/NBA` which focuses on the National Basketball Association held in the United States, where most of the best basketball players around the globe play.

## Executive Summary

To get the necessary posts for this project, I scrapped 10,000 'hot' posts using PMAW which is a pushshift multithread API Wrapper which gives access to a large amount of data from Reddit.

I then cleaned up the data by removing the null values, the URL and HTML tags where necessary, and vectorized each post and tested out two classification models before settling on a combination of CountVectorizer and Random Forest Classifier which was able to accurately classify about 0.75% of posts correctly.

Some of the limitations to our model would be that the number of comments is severely impacted on whether or not the NBA is in season, especially come playoff time. There is a more dedicated fanbase during playoffs that posts discussions of each game that is more indepth and may contain a different type of language compared to the off-season, where there are more meme-type posts. There are also some misclassification on whether or not a post has above the mean number of comments, which in this case was 9. Lastly, due to some of the subreddit rules, there may be heavy bias in title structure, which may have affected our overall outcome.

## Recommendations

My Recommendations to Nate Silver and co. at FiveThirtyEight to create a Reddit post that will get the most engagement from Reddit users are to use words that are highly associated with r/NBA including names. Some names included Kevin Durant, Michael Jordan, and Lebron James. By utilizing their popularity in the post, it would have a better effect in attracting engagement from users. 

Highlights also seemed to have high usage in titles, partly due to the subreddit posting rules. With video clips of highlights of various games throughout the week, users may be able to catch up to the games they were unable to see live, increasing the engagment in the post.
