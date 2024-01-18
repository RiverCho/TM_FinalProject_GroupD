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

File1: “oscars_cast_node.csv”

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


File2: "oscars_cast_edge.csv"

| Variable | Description                                  | DataType |
|----------|----------------------------------------------|----------|
| source   | Name of the source cast                      | String   |
| target   | Name of the target cast                      | String   |
| weight   | Cooperation frequencies between two casts   | Numeric  |
| label    | Film name of cooperating                     | String   |

File3: "HK_cast_node.csv"

| Variable   | Description                                                   | DataType |
|------------|---------------------------------------------------------------|----------|
| Id         | Name of the awarded individuals                               | String   |
| Role       | Actors (Actress) or Director                                  | String   |
| Gender     | Gender of the awarded individuals                             | String   |
| Nationality| Nationality of the awarded individuals                        | String   |
| Category   | Award name                                                    | String   |
| Year       | Award year                                                    | Integer  |
| Film       | Film name                                                     | String   |

File4: "HK_cast_edge.csv"

| Variable | Description                                           | DataType |
|----------|-------------------------------------------------------|----------|
| source   | Name of the source cast                               | String   |
| target   | Name of the target cast                               | String   |
| weight   | Cooperation frequencies between two casts            | Numeric  |


File5: "oscars_genre_node.csv"

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

File6: "oscars_genre_weight.csv"

| Variable | Description                                   | DataType  |
|----------|-----------------------------------------------|-----------|
| source   | Name of the source film                       | String    |
| target   | Name of the target film                       | String    |
| weight   | Genre Similarity between two films            | Numeric   |

*Note: Genre Similarity is calculated by counting the common genres and adding corresponding weights. For example, if one film has “Drama”, “Romance”, and “Comedy”, and the other has “Romance” and “Comedy”, the weight will be 2.*

File7: "HK_genre_node.csv"

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


File8: "HK_genre_edge.csv"

| Variable | Description                                   | DataType  |
|----------|-----------------------------------------------|-----------|
| source   | Name of the source film                       | String    |
| target   | Name of the target film                       | String    |
| weight   | Genre Similarity between two films            | Numeric   |

*Note: Genre Similarity is calculated by counting the common genres and adding corresponding weights. For example, if one film has “Drama”, “Romance”, and “Comedy”, and the other has “Romance” and “Comedy”, the weight will be 2.*

## Source
https://www.kaggle.com/datasets/unanimad/the-oscar-award

https://www.kaggle.com/datasets/carolzhangdc/imdb-5000-movie-dataset
