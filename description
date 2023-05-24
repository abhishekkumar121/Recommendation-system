This repository is for anime recommendation system. It contains anime.ipynb file and app.py, anime.ipynb is jupyter notebook file where I have made the content based recommendation system using cosine similarity. App.py file is the frontend of the recomeendation system based on streamlit.

Recommendation System
Recommender systems are the systems that are designed to recommend things to the user based on many different factors. These systems predict the most likely product that the users are most likely to purchase and are of interest to. Companies like Netflix, Amazon, etc. use recommender systems to help their users to identify the correct product or movies for them.

Types of recommender systems

There are three primary types of recommender systems.

Content-based filtering uses similarities in products, services, or content features, as well as information accumulated about the user to make recommendations.
Collaborative filtering relies on the preferences of similar users to offer recommendations to a particular user.
Hybrid recommender systems combine two or more recommender strategies, using the advantages of each in different ways to make recommendations.
Cosine Similarity

Cosine similarity is one of the metric to measure the text-similarity between two documents irrespective of their size in Natural language Processing. A word is represented into a vector form. The text documents are represented in n-dimensional vector space.

Mathematically, Cosine similarity metric measures the cosine of the angle between two n-dimensional vectors projected in a multi-dimensional space. The Cosine similarity of two documents will range from 0 to 1. If the Cosine similarity score is 1, it means two vectors have the same orientation. The value closer to 0 indicates that the two documents have less similarit

About Dataset
Context
This data set contains information on user preference data from 73,516 users on 12,294 anime. Each user is able to add anime to their completed list and give it a rating and this data set is a compilation of those ratings.

Content

Anime.csv

anime_id - myanimelist.net's unique id identifying an anime.

name - full name of anime.

genre - comma separated list of genres for this anime.

type - movie, TV, OVA, etc.

episodes - how many episodes in this show. (1 if movie).

rating - average rating out of 10 for this anime.

members - number of community members that are in this anime's "group".

Rating.csv

user_id - non identifiable randomly generated user id. anime_id - the anime that this user has rated. rating - rating out of 10 this user has assigned (-1 if the user watched it but didn't assign a rating).

Imports

import pandas

from sklearn.feature_extraction.text import CountVectorizer

from nltk.stem.porter import PorterStemmer

import bz2

import pickle

from sklearn.metrics.pairwise import cosine_similarity

I did the basic preprocessing like (dropping null rows, dropping unwanted columns and removing anomalities for the string type columns ) but the main focus was on strings so that I can apply the cosine similarity. For that I made a new column named "tags" which is the concatenation of "title", "synopsis" and "genre". After aapplyting NLP on "tags" column and applied cosine similarity on the column and using this column we can recommend the anime.

At the end I have compressed and saved the cosine similarity score as similarity.pbz2 so that I can use it in frontend to recommend.

Make a virtual enviroment for the app and paste the similarity.pbz2 in that folder and run the code streamlit run app.py using terminal. Your app will start running.

Now search the name of anime, it will show you all the information about that anime with a link and below that some to recommended anime.
