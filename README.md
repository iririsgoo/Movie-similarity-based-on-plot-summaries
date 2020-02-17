# Movie-similarity-based-on-plot-summaries

Applied Text and Natural Language Analytics course project, Columbia University(2019 Fall)

Teammates: @Zoe0409; Yingyi Lang

## Background: 



## Problems to solve: 
However, both genres and users’ ratings have some limitations. 
First, films within a genre sometimes share common intuition-based base parameters, but that would be too broad. 
For example, comedy, it contains different subtypes and even movies within the same comedy subgroup may not be the most similar movies for each other.
Another problem is often referred to as “new item cold start problem”. 
The number of ratings for new released movies would be very limited, making it hard to find similar ones for this movie. 
Facing the above two problems of current movie recommender systems, we proposed to find movie similarity from plot summaries using k-means and we will visualize the result.

## Data Source: 
1. scrape IMDB’s movie name, genre and plot summaries. 


## Research Design: 
Our project includes four parts:
1. Data Collection: (Saved in dataset folder)

2. Exploratory Data Analysis: [code](IMDB movies exploratory data analysis.ipynb)

3. Topic Modeling: (Saved in analysis folder -- [code](IMDB Movies topic modeling using sklearn.ipynb)

4. Similarity Calculation: We used two bases to calculate similarity

* Key words: [code](IMDB Movies similarity from key words.ipynb)

* Plot summaries: [code](IMDB Movies similarity from plot summaries.ipynb)


## Expected Output: 
We will get the quantified similarity of each movie based on their plot summaries. We also expect to divide movies into clusters according to the similarity of plot. 
To visualize the result, we'll create a dendrogram to represent how closely the movies are related to each other. 


## Evaluation Metrics: 
To evaluate model performance, we can use MAE and RMSE. In terms of similarity itself, here are a few ways to evaluate but all these approaches would be based on subjective judgement:

## Spot check: 
pick our familiar movies and TVs, check the top 50 most similar items for each of them, and see if the result makes sense;
Baseline from other platforms: get the similar movies/TVs list from other platforms as baseline and compare that with our result.

