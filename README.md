# Movie-similarity-based-on-plot-summaries

Applied Text and Natural Language Analytics course project, Columbia University(2019 Fall)

Teammates: @Zoe0409; Yingyi Lang


## Problems to solve: 
In terms of calculating movie similarities, both genres and users’ ratings have some limitations
First, films within a genre sometimes share common intuition-based base parameters, but that would be too broad. 
For example, comedy, it contains different subtypes and even movies within the same comedy subgroup may not be the most similar movies for each other.
Another problem is often referred to as “new item cold start problem”. 
The number of ratings for new released movies would be very limited, making it hard to find similar ones for this movie. 
Facing the above two problems of current movie recommender systems, we proposed to find movie similarity from plot summaries using k-means and we will visualize the result.

## Data Source: 
1. Scrape IMDB’s movie name, genre and plot summaries. [code](Collect data from IMDB.ipynb)

## Research Design: 
1. Data Collection: [dataset](dataset.csv)

2. Exploratory Data Analysis: [code](IMDB movies exploratory data analysis.ipynb)

3. Topic Modeling: (Saved in analysis folder -- [code](IMDB Movies topic modeling using sklearn.ipynb)

4. Similarity Calculation: We used two bases to calculate similarity

* Key words: [code](IMDB Movies similarity from key words.ipynb)

* Plot summaries: [code](IMDB Movies similarity from plot summaries.ipynb)


## Evaluation Metrics: 
To evaluate model performance, we can use MAE and RMSE. In terms of similarity itself, here are a few ways to evaluate but all these approaches would be based on subjective judgement:

* Spot check: pick our familiar movies and TVs, check the top 50 most similar items for each of them, and see if the result makes sense;

* Baseline from other platforms: get the similar movies/TVs list from other platform as baseline and compare that with our result.

## Spot check: 
There are a lot of movies with "Christmas" topic in plot.
>  Send out notifications about these movies to users during Christmas season.

Keywords and plot similarity gave different results.
>  Movie recommendation platforms can display both results and allow users to make their own choices.

Similarity score between movies can be based on different metrics.
> Construct an aggregated similarity score to reflect the real similarity between two movies and use it to generate predicted ratings through KNN.

Movie platforms can send out recommendations generated from different methods to users to test which one is favored by them.

