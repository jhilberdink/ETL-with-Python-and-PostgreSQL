# Movies_ETL
This project creates an automated pipeline that extracts, transforms, and loads movie metadata into a PostgreSQL database. The function contained in [ETL_create_database](ETL_create_database) loads raw data from [Wikipedia Movies](Resources/wikipedia-movies.json), [Kaggle Movies Metadata](Resources/movies_metadata.csv), and [MovieLens Ratings](Resources/ratings.csv) into Pandas dataframes and performs cleanup operations. Data cleanup steps include:
- dropping columns with null values
- removing duplicate entries
- standardizing box office data, budget data, runtime, and release dates using regular expressions
- merging the Wikipedia Movies and Kaggle Movies dataframes
After data cleanup is complete, the function exports the data into a two tables in a PostgreSQL database, a movies table and a ratings table.

### Technologies Used
- Python
- Pandas
- Jupyter Notebooks
- Regular Expressions
- PostgreSQL
