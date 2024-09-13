# SQL-Netflix-Dataset-Analysis
"A collection of SQL queries and insights derived from the Netflix dataset."
![image](https://github.com/user-attachments/assets/a99968e6-f186-4b03-ba77-7aaef0be456c)
**Overview**
This project involves a comprehensive analysis of Netflix's movies and TV shows data using SQL. The goal is to extract valuable insights and answer various business questions based on the dataset. The following README provides a detailed account of the project's objectives, business problems, solutions, findings, and conclusions.

**Objectives**
Analyze the distribution of content types (movies vs TV shows).
Identify the most common ratings for movies and TV shows.
List and analyze content based on release years, countries, and durations.
Explore and categorize content based on specific criteria and keywords.

**Schema
**
DROP TABLE IF EXISTS netflix;
CREATE TABLE netflix
(
    show_id      VARCHAR(5),
    type         VARCHAR(10),
    title        VARCHAR(250),
    director     VARCHAR(550),
    casts        VARCHAR(1050),
    country      VARCHAR(550),
    date_added   VARCHAR(55),
    release_year INT,
    rating       VARCHAR(15),
    duration     VARCHAR(15),
    listed_in    VARCHAR(250),
    description  VARCHAR(550)
);

# SQL Netflix Dataset Analysis 🎥

## Overview
This project showcases SQL queries performed on a Netflix dataset (`chase_.netflix`). The aim is to practice data manipulation, filtering, and aggregation using SQL, focusing on retrieving insights from Netflix data.

## Dataset Description
The `chase_.netflix` dataset includes information such as:
- **Title**: Name of the movie or TV show
- **Type**: Movie or TV Show
- **Duration**: Length of the movie or show
- **Director**: Name of the director
- **Release Year**: Year the content was released
- **Rating**: Audience rating (e.g., PG-13, R)
- **Date Added**: Date when the content was added to Netflix

## Key SQL Queries
Here are some key queries used in this project:

### 1. **Retrieve All Data from the Dataset**
```sql
SELECT *  
FROM chase_.netflix;
2. List Movies and Their Durations
SELECT title, duration  
FROM chase_.netflix  
WHERE type = 'Movie';
3. Count TV Shows

SELECT COUNT(*)  
FROM chase_.netflix  
WHERE type = 'TV Show';
4. Find the Most Common Genre

SELECT listed_in, COUNT(*) AS genre_count
FROM chase_.netflix
GROUP BY listed_in
ORDER BY genre_count DESC
LIMIT 1;


**Conclusion
**
This project aimed to explore and analyze the chase_.netflix dataset using SQL, focusing on gaining insights into the types of content available, release years, genres, and more. Through a series of queries, I was able to uncover some interesting findings:

**Key Insights:
**
The majority of titles in the dataset are movies, with a smaller percentage being TV shows.
Drama is the most common genre, with a significant number of titles listed under this category.
A notable portion of the content was added in recent years, showing a strong trend toward new releases.
These insights demonstrate the value of SQL in retrieving, filtering, and summarizing large datasets. Through this project, I practiced a range of SQL techniques, including SELECT, WHERE, GROUP BY, and COUNT to manipulate and analyze data effectively.

In the real world, platforms like Netflix can utilize this data to make informed decisions about content acquisition, audience preferences, and regional trends. By analyzing viewer behavior and content popularity, companies can tailor their offerings to enhance user experience.

Moving forward, this analysis could be expanded by exploring more complex queries or integrating other datasets to find correlations between ratings and viewership trends.

Overall, this project has been an excellent opportunity to deepen my understanding of SQL and data analysis. I encourage anyone interested in data science to continue practicing and experimenting with different datasets.

