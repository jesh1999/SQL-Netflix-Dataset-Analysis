---

# 🎬 **SQL Netflix Dataset Analysis** | *Insights from the Streamverse*

![SQL Netflix Analysis](https://github.com/user-attachments/assets/a99968e6-f186-4b03-ba77-7aaef0be456c)

---

## 💡 *Why this project?*

In a world where binge-watching is the new normal, I was curious to dive deep into what Netflix offers — *and what better way to explore than through data?*

This project was all about flexing my SQL muscles while uncovering some cool insights from Netflix’s content library. 📺🍿

---

## 📦 Dataset at a Glance

I worked with a dataset containing information like:
- 🎥 **Title**, **Type** (Movie or TV Show)  
- 🌍 **Country**, **Release Year**, **Date Added**  
- 🎭 **Genre**, ⏱️ **Duration**, and 🎯 **Rating**  

Here’s the SQL schema I used to store the data:

```sql
CREATE TABLE netflix (
    show_id VARCHAR(5),
    type VARCHAR(10),
    title VARCHAR(250),
    director VARCHAR(550),
    casts VARCHAR(1050),
    country VARCHAR(550),
    date_added VARCHAR(55),
    release_year INT,
    rating VARCHAR(15),
    duration VARCHAR(15),
    listed_in VARCHAR(250),
    description VARCHAR(550)
);
```

---

## 🔎 What I Explored

### 1. 🎬 **Movie vs. TV Show Breakdown**
How much content is actually movies vs. TV shows?  
→ *Spoiler*: Movies dominate.

### 2. 📏 **Duration Insights**  
I filtered for movies to check how long they typically run.

### 3. 📊 **Genre Popularity**  
Which genres are ruling the Netflix library?  
→ *Drama* is Netflix’s absolute favorite.

### 4. 🌐 **Content by Country & Year**  
I checked which countries produce the most content and how recent most uploads are.

---

## 🔍 Sample SQL Queries

```sql
-- All records
SELECT * FROM chase_.netflix;

-- Movies and their durations
SELECT title, duration  
FROM chase_.netflix  
WHERE type = 'Movie';

-- TV Show count
SELECT COUNT(*)  
FROM chase_.netflix  
WHERE type = 'TV Show';

-- Most common genre
SELECT listed_in, COUNT(*) AS genre_count  
FROM chase_.netflix  
GROUP BY listed_in  
ORDER BY genre_count DESC  
LIMIT 1;
```

---

## 📈 Key Insights

- 🟣 **Movies** form the majority of Netflix’s content.
- 🎭 **Drama** is the most common genre.
- 📅 A huge chunk of content was added **in the last few years**—Netflix keeps it fresh!
- 🗺️ The platform is becoming more **globally diverse**, with content from all over the world.

---

## 🚀 Final Thoughts

This project wasn’t just about SQL—  
It was about storytelling with data 🎯

I explored, queried, analyzed, and walked away with:
✅ A deeper understanding of Netflix's content strategy  
✅ Sharpened SQL skills  
✅ A growing love for data exploration!

> 💬 Curious how platforms like Netflix make data-driven decisions?  
This is just the tip of the iceberg. 📊

---

