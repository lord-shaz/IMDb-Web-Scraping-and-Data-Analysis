![logo](https://github.com/ShehzadaAlam/IMDb-Web-Scraping-and-Data-Analysis/blob/master/logo.png "imdb logo")
# IMDb-Web-Scraping-and-Data-Analysis:
-----

# Problem Statement:
------
- The Internet Movie Database (IMDb) is one of the world’s most popular sources for movie, TV and celebrity content with more than 100 million unique visitors per month.
- IMDb has huge collection of movies database that includes various details of movies along with different ratings and user reviews.
- This movie reviews affects everyone from audience, film critics to the production company.
- Idea of our project is to scarp the data from  IMDb and form an analysis that will help data analyst or production company to decide how they are going to proceed with making a new movie, second is to form a model to predict what are the sentiments of movies based on user reviews.

# Dataset: 
-----
- 3500+ records and has 10 columns.

# Solution Details:
-----
- Extracting all the details of movies like IMDBID,Title,Genre, Year, Audience rating, Critics rating, Budget and Reviews using 'OMDB API' and webscrapping.
- Established the Database Connection as we are storing this movie data in MySQL.
- While searching the movie detail if the entry is not present then fetch the detail from imdb through webscraping and with API, insert the record in database and display result back to the user.
- For analysis extract the data from database into dataframe and visualize the data to get some insights.

# Sentiment Analysis Approach:
---
- “Sentiment analysis is an important research area that identifies the people’s sentiments, opinions and emotions underlying a text.”
- Sentiment Analysis based on User Reviews and created a new column(polarity) which includes this Labels (Positive and Negative).
- We have used “Unsupervised lexicon based method”, which are dictionaries or vocabularies of polar words specially constructed for  sentiment classification task.
- The system uses VADER (Valence Aware Dictionary and sEntiment Reasoner) based lexicon method for sentiment analysis that not only tells about the positive,negative, neutral and compound score between -1 to +1 but gives positive or negative sentiment of reviews based on this score.
- To extract this sentiments we have computed the polarity of the given reviews (whether the text is positive or negative).

# Model Building:
-----
- In order to make sense to our machine learning algorithm we have converted each review to a numeric representation which is called 'Vectorization'.
- The system uses TF-IDF Vectorizer (Term Frequency-Inverse document frequency) that transforms a count matrix to a normalized frequency representation in float.
- Splitting the movie data into Train and Test set (80-20 ratio).
- SVM: The objective of a Linear SVC (Support Vector Classifier) is to fit the data, returning a best fit hyperplane that divides or classifies the data. 
**Accuracy= 79.61%**
![accuracy](https://github.com/ShehzadaAlam/IMDb-Web-Scraping-and-Data-Analysis/blob/master/Accuracy%20Measure.PNG "accuracy")

# Challenges:
-----
- Using omdb API we were not able to fetch Budget and User Reviews hence we have scrapped the data from imdb website using imdb id.
- While fetching 'Budget' from imdb website the amount were present in different currency format so we have converted the currencies in USD by using CurrencyConverter package.
- After getting polarity for all the user reviews, this reviews was needed to be converted in numerical representation to fit the classification model.
- While rendering seaborn graphs on Django Framework we were getting several response errors and were not able to display the plots. 

# Frontend:
----
![fron1](https://github.com/ShehzadaAlam/IMDb-Web-Scraping-and-Data-Analysis/blob/master/frontend1.png "front1")
![front2](https://github.com/ShehzadaAlam/IMDb-Web-Scraping-and-Data-Analysis/blob/master/frontend2.png "front2")
![front3](https://github.com/ShehzadaAlam/IMDb-Web-Scraping-and-Data-Analysis/blob/master/frontend3.png "front3")
![front4](https://github.com/ShehzadaAlam/IMDb-Web-Scraping-and-Data-Analysis/blob/master/frontend4.png "front4")
----
<p>Thank You!	
<p><!-- Place this tag where you want the button to render. -->
<a class="github-button" href="https://github.com/ShehzadaAlam" aria-label="Follow @ShehzadaAlam on GitHub">Follow @ShehzadaAlam</a>
