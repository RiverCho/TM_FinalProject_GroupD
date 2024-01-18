# Oscar and Hong Kong Film Awards Analysis

This GitHub repository comprises a comprehensive analysis project focused on Oscar-winning films and Hong Kong Film Awards (HKFA) winning films from the years 2001 to 2010. The primary objective of this project is to delve into the relationships between film genres, explore connections among actors and directors within these acclaimed films, and identify distinctive features of the scripts of Oscar-winning films during this specific period.

## Repository Contents:

1. **Dataset:**
   - The `dataset` directory contains the datasets used for the analysis. These datasets are meticulously collected, curated, and cleaned to ensure accuracy and relevance to the project's objectives.

2. **Jupyter Notebook:**
   - The `2001-2010OscarsCastAndWorksDataCollecting.ipynb` file is a Jupyter Notebook that provides a step-by-step breakdown of how the data was collected, organized, and cleaned.

3. **Research Report:**
   - The `Report.pdf` document encapsulates the findings and insights derived from the analysis. It offers a comprehensive overview of the relationships explored, patterns identified, and key takeaways from the study.

## Dataset Description:

File1: Gephi/oscars_cast_node.csv

| Variable   | Description                                    | DataType |
|------------|------------------------------------------------|----------|
| ID         | Name of the awarded individuals                | String   |
| BirthYear  | Birth year of the awarded individuals           | Integer  |
| Gender     | Gender of the awarded individuals               | String   |
| Nationality| Nationality of the awarded individuals          | String   |
| Category   | Award name                                     | String   |
| AwardYear  | Award year                                     | Integer  |
| Film       | Film name                                      | String   |
| Type       | Actors (Actress) or Director                   | String   |


File2: Gephi/oscars_cast_edge.csv

| Variable | Description                                  | DataType |
|----------|----------------------------------------------|----------|
| source   | Name of the source cast                      | String   |
| target   | Name of the target cast                      | String   |
| weight   | Cooperation frequencies between two casts   | Numeric  |
| label    | Film name of cooperating                     | String   |

File3: Gephi/HK_cast_node.csv

| Variable   | Description                                                   | DataType |
|------------|---------------------------------------------------------------|----------|
| Id         | Name of the awarded individuals                               | String   |
| Role       | Actors (Actress) or Director                                  | String   |
| Gender     | Gender of the awarded individuals                             | String   |
| Nationality| Nationality of the awarded individuals                        | String   |
| Category   | Award name                                                    | String   |
| Year       | Award year                                                    | Integer  |
| Film       | Film name                                                     | String   |

File4: Gephi/HK_cast_edge.csv

| Variable | Description                                           | DataType |
|----------|-------------------------------------------------------|----------|
| source   | Name of the source cast                               | String   |
| target   | Name of the target cast                               | String   |
| weight   | Cooperation frequencies between two casts            | Numeric  |


File5: Gephi/oscars_genre_node.csv

| Variable              | Description                                    | DataType  |
|-----------------------|------------------------------------------------|-----------|
| ID                    | Name of the movie                              | String    |
| year_film             | Releasing year                                 | Integer   |
| year_ceremony         | Awarded year                                   | Integer   |
| imdb_score            | IMDb score                                     | Integer   |
| num_voted_users       | Number of voted users                          | Integer   |
| budget                | Budget of the film                              | Integer   |
| language              | Language of the film                            | String    |
| country               | Country or region of film production           | String    |
| gross                 | Gross of the film                               | Integer   |
| genres                | Genre of the film                               | String    |
| num_user_for_reviews  | Number of reviewers on IMDb                     | Integer   |
| duration              | Duration of the film                            | Integer   |
| director_name         | Director's name of the film                     | String    |

File6: Gephi/oscars_genre_weight.csv

| Variable | Description                                   | DataType  |
|----------|-----------------------------------------------|-----------|
| source   | Name of the source film                       | String    |
| target   | Name of the target film                       | String    |
| weight   | Genre Similarity between two films            | Numeric   |

*Note: Genre Similarity is calculated by counting the common genres and adding corresponding weights. For example, if one film has “Drama”, “Romance”, and “Comedy”, and the other has “Romance” and “Comedy”, the weight will be 2.*

File7: Gephi/HK_genre_node.csv

| Variable                   | Description                                  | DataType  |
|----------------------------|----------------------------------------------|-----------|
| ID                         | Name of the movie                             | String    |
| Awarded_Year               | When the awards were given                    | Integer   |
| Number_of_Awards           | Number of awards received                     | Integer   |
| Category                   | Specific genre of the film                    | String    |
| Main_Category              | Main genre of the film                        | String    |
| Douban_Score               | Score on Douban platform                      | Integer   |
| Production Country/Region  | Country or region of film production          | String    |
| Duration                   | Duration of the film                          | Integer   |
| Language                   | Language of the film                          | String    |
| Reviewer_Number            | Number of reviewers on Douban                 | Integer   |


File8: Gephi/HK_genre_edge.csv

| Variable | Description                                   | DataType  |
|----------|-----------------------------------------------|-----------|
| source   | Name of the source film                       | String    |
| target   | Name of the target film                       | String    |
| weight   | Genre Similarity between two films            | Numeric   |

*Note: Genre Similarity is calculated by counting the common genres and adding corresponding weights. For example, if one film has “Drama”, “Romance”, and “Comedy”, and the other has “Romance” and “Comedy”, the weight will be 2.*

File9 Source/the_oscar_award.csv

| Variable         | Description                               | DataType |
|------------------|-------------------------------------------|-----------|
| `year_film`      | Filming year                              | Integer   |
| `year_ceremony`  | Awarding year                             | Integer   |
| `ceremony`       | The edition of the Academy Awards          | Integer   |
| `category`       | The name of the awards                     | String    |
| `name`           | The name of the winner or nominee          | String    |
| `film`           | Film name                                  | String    |
| `winner`         | Boolean indicating if the nominee is the winner | Boolean      |

File10 Source/movie_metadata.csv

| Variable                     | Description                                   | DataType  |
|------------------------------|-----------------------------------------------|-----------|
| director_name                | Name of the movie director                    | Text      |
| num_critic_for_reviews       | Number of critic reviews                      | Numeric   |
| duration                     | Duration of the movie (in minutes)           | Numeric   |
| director_facebook_likes      | Number of Facebook likes for the director     | Numeric   |
| actor_3_facebook_likes       | Number of Facebook likes for actor 3          | Numeric   |
| actor_2_name                 | Name of actor 2                               | Text      |
| actor_1_facebook_likes       | Number of Facebook likes for actor 1          | Numeric   |
| gross                        | Gross earnings of the movie                   | Numeric   |
| genres                       | Movie genres                                  | Text      |
| actor_1_name                 | Name of actor 1                               | Text      |
| movie_title                  | Title of the movie                            | Text      |
| num_voted_users              | Number of users who voted for the movie       | Numeric   |
| cast_total_facebook_likes    | Total Facebook likes for the movie cast       | Numeric   |
| actor_3_name                 | Name of actor 3                               | Text      |
| facenumber_in_poster         | Number of faces in the movie poster           | Numeric   |
| plot_keywords                | Keywords describing the movie plot           | Text      |
| movie_imdb_link              | IMDB link for the movie                       | Text      |
| num_user_for_reviews         | Number of user reviews                        | Numeric   |
| language                     | Movie language                                | Text      |
| country                      | Country where the movie was produced          | Text      |
| content_rating               | Movie content rating                          | Text      |
| budget                       | Budget of the movie                           | Numeric   |
| title_year                   | Release year of the movie                     | Numeric   |
| actor_2_facebook_likes       | Number of Facebook likes for actor 2          | Numeric   |
| imdb_score                   | IMDB score of the movie                       | Numeric   |
| aspect_ratio                 | Aspect ratio of the movie                     | Numeric   |
| movie_facebook_likes         | Number of Facebook likes for the movie        | Numeric   |

## Source
https://www.kaggle.com/datasets/unanimad/the-oscar-award

https://www.kaggle.com/datasets/carolzhangdc/imdb-5000-movie-dataset
