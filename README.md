# imdb-top-250-analysis
Analysis of IMDb top 250 movies for Python final project.

## About the Data
This dataset comes from Kaggle user mohamedasak and contains data about the top movies on IMDb.

Video Game Sales Dataset contains 11 columns, which are:

1. Rank - IMDb rank (1 to 250)
2. Title - Movie title

3. Year - Release year

4. Rating - IMDb rating (out of 10)

5. Duration - Movie runtime (e.g., “2h 22m”)
6. Genres - Movie genres (e.g., Drama, Action, Crime)
7. Certificate - Age rating or viewing restriction (e.g., PG-13, R)
8. Description - Short movie summary or plot
9. IMDb URL - Direct link to the movie’s IMDb page
10. Image URL - Poster or cover image link
(https://www.kaggle.com/datasets/mohamedasak/imdb-top-250-movies)

## Data Cleaning
I checked for duplicates and null values. I found no duplicates and 5 cells with null values. I determined that the null values would not significantly affect the analysis.

## Data Manipulation
The questions I wanted to answer and the steps I took for data manipulation in this exploration/analysis are:
* Which genres tend to have the highest average IMDb rating?
  - To be able to answer this question, I separate the genres listed in the "Genres" column into individual columns (Genre1, Genre2, Genre3). Then I created new DataFrames using each of these new columns and the average Rating for each genre. Then I combined the three new DataFrames into "genres_rating" and added a new "TotalAvgRating" column. Finally, I sorted the values of the DataFrame by "TotalAvgRating" in ascending order.
* Are older movies more likely to appear in the top 250 than newer ones?
  - To be able to answer this question, I added a new column to the original DataFrame called "Decade" which used data from the "Year" column to find the decade a movie released.
* Which certificate category has the highest-rated films?
  - To be able to answer this question, I created a new DataFrame called "certificate_rating" that contained the average rating for each certificate category.

 ## Visualizations
 I created the following visualizations to address the guiding questions:
 * Which genres tend to have the highest average IMDb rating?
![Genre vs. Rating Chart](assets/charts/genre_rating.png "Genre vs. Rating Chart")
* Are older movies more likely to appear in the top 250 than newer ones?
![Movies Per Decade Chart](assets/charts/movies_decade.png "Movies Per Decade Chart")
* Which certificate category has the highest-rated films?
![Certificate vs Rating Chart](assets/charts/certificate_rating.png "Certificate vs Rating Chart")

## Statistical Analysis
I conducted descriptive statistics on the data from the "Rating" and "Year" columns to explore what rating and year the top 250 movies are clustered around. I found that the top 250 movies are clustered around a mean rating of 8.3 and the year 1988. Most of the movies were released within 30 years. The movies in the top 250 are within 1.3 points on the IMBd rating scale.
