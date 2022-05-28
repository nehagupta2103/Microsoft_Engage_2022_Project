# MOVIEFLIX- Movie Recommendation Engine: Genre-based and Content-based 

>This project is a fully functional prototype of a Movie Recommendation Engine: Movieflix, based on Content-based filtering, where a user can also get recommendations on the basis of a specified genre or a combination of multiple genres.
</br>

![Home_Page](https://github.com/nehagupta2103/Movieflix/blob/main/Screenshots/Home-Page.png)

## Demo Version
A demo version is automatically deployed for this repository:
</br>
- Deployment -
- Demo Video - 

## Local Installation
</br>

### Steps
- `git clone <repository-url>` where `<repository-url>`is the link to the forked repository
- `cd Movieflix`

Note : If you want to contribute, first fork the original repository and clone the forked repository into your local machine followed by `cd` into the directory

```
git clone https://github.com/USERNAME/Microsoft-Engage-21-Project.git
cd Movieflix
```

#### Steps to run the project on your local machine

- Install all the dependencies mentioned in the [requirements.txt](https://github.com/nehagupta2103/Movieflix/blob/main/requirements.txt) file with the command `pip install -r requirements.txt` 
- Open terminal from the project directory and run the file `main.py` by executing the command `python main.py`.
- Visit your app at [http://127.0.0.1:5000/](http://127.0.0.1:5000/) :tada:

>Home Page
<img alt=" " src="https://github.com/nehagupta2103/Movieflix/blob/main/Screenshots/Home-Page.png">

>Light Theme of the Home Page
<img alt=" " src="https://github.com/nehagupta2103/Movieflix/blob/main/Screenshots/Light%20Theme.png">

>Movie Search Box
<img alt=" " src="https://github.com/nehagupta2103/Movieflix/blob/main/Screenshots/Movie%20Search%20Box.png">

>Movie Suggestions
<img alt=" " src="https://github.com/nehagupta2103/Movieflix/blob/main/Screenshots/Movie%20Suggestions.png">

>Genre-based Recommendation Engine
<img alt=" " src="https://github.com/nehagupta2103/Movieflix/blob/main/Screenshots/Genre-Based%20Recommender.png">

>Overview Hover of Movies
<img alt=" " src="https://github.com/nehagupta2103/Movieflix/blob/main/Screenshots/Overview%20Hover.png">

>Fetched video clips of movies
<img alt=" " src="https://github.com/nehagupta2103/Movieflix/blob/main/Screenshots/Video%20Clips%20of%20Movies.png">

>Loader
<img alt=" " src="https://github.com/nehagupta2103/Movieflix/blob/main/Screenshots/Loader.png">

>Searched Movie for Recommendation
<img alt=" " src="https://github.com/nehagupta2103/Movieflix/blob/main/Screenshots/Avatar_2_2022Movie.png">

>Content Based Recommendations
<img alt=" " src="https://github.com/nehagupta2103/Movieflix/blob/main/Screenshots/Content_based%20Recommendation.png">

>Top 3 Cast of the searched movie
<img alt=" " src="https://github.com/nehagupta2103/Movieflix/blob/main/Screenshots/Top%203%20Cast.png">

>Sentiment Analysis on Reviews
<img alt=" " src="https://github.com/nehagupta2103/Movieflix/blob/main/Screenshots/Sentiment%20Analysis.png">

## Features
</br>

1. Genre-Based Recommendation Engine:
   1. const genresGet movies by clickig on one or multiple genres 
   2. highlightSelection(): Selected genre gets highlighted
   3. Color coded the IMDB ratings using function getColor(): (green (good), orange(neutral), red(bad)) 
   4. Overview Hover: Overview of the movie appears as the cursor is moved on it
   5. "Click to watch clips button": Youtube video clips of the selected movie is fetched from youtube.com, and opens on the same page in another frame, uses showMovies() function
   6. openNav function: oepns when someone clicks on the span eleent, fetches video clips and opens up a new frame to showcase the videos
   7. closeNav function:  closes when someone clciks on the 'x'(close) symbol inside the overlay
   
2. Content-Based Recommendation Engine:
   1. Extracted movies of the year 2018, 2019, 2020, 2021 and 2022 from wikipedia, pre-processed the fetched data and combined it with the older dataset using pandas, numpy, tmdbv3api and json.
   2. Built a Machine Learning Algorithm to recommend similar movies using `Similarity Matrix` and used `Cosine Similarity Algorithm` to do so.
   3. Features used to find the similarity and train the ML Model: director_name, actor_1_name, actor_2_name,actor_3_name, genres, movie_title
   4. Used Scikit-learn's `CountVectorizer` to convert text file into a vector of term/token counts
   5. Combined_features: Combined all the features into a single string 'comb'
   6. Used `CountVectorizer's fit.tranform` to count the number of texts, then printed the transformed 'count_matrix' to array.
   7. Used Cosine Similarity to find similarity between two movies, output value ranged from 0 to 1, here, ) means no similarity and 1 means both the movies are 100% similar.
   8. Used movie_index of the searched movie to generate a list of similar movies with the similarity score of each index.
   9. `Sorting Similar Movies`: Used the parameter 'reverse=True' since we want the list in the descending order, with the most similar item at the top.
   10. Used `Python's flask`  and called load_details function to fetch details of the similar movies using their movie ids.
   
3. Sentiment Analysis:
   1. Scrapped reviews of the searched movies from tmdb's site using a Python Library `Beautiful Soup` to pull data out of XML files.
   2. Used `TfidfVectorizer` to map the most frequent words to feature indices, and computed a frequency matrix.
   3. Used `Multinomial Naive Bayes` Classification Algorithm to guess the tag (in this case: Positive or Negative Reviews) of the text by calculating each tag's likelihood.
   4. Achieved an accuracy score of `98.7716` after applying `NLP's` Multinomial Naive Bayes for classification.
   5. Pickled the python file to store the database and unpickled it in main.py file.

4. Other features:
   1. Dark/Light Theme: Created a functional toggle to change theme of the page from dark to light and vice-versa.
   2. Carousel Component: Built a Movie Slider on the homepage
   3. Search Box/Placeholder: Gives suggestions of movies while typing
   4. Top-3 Cast: Fetches details of top 3 cast of the searched movie from tmdb's API
   5. Siderbar and NavBar: Built a non-functional siderbar and navbar to contain toggle, profile and other menu_list items.






