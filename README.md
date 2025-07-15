# Streaming Platform Movie Analysis: Netflix vs Amazon Prime Video

## Project Overview  
This project analyzes a comprehensive dataset of nearly 25,000 movies available on Netflix and Amazon Prime Video. The dataset contains detailed data including Movie Title, IMDb and Rotten Tomatoes ratings, genres, year released, minimum age rating, and platform availability.  
The goal is to clean and preprocess the raw data, then perform exploratory and comparative analyses to uncover insights about movie ratings, genres, audience age groups, and platform-specific trends.

---

## Dataset Description  
- Single raw table with movie fields:
  - Title  
  - Year released  
  - Minimum recommended age (MinAge)  
  - IMDb score, Rotten Tomatoes score  
  - Genre(s) (multi-label, comma separated)  
  - Platform availability flags (Netflix, Amazon Prime Video)  

---

## Data Cleaning & Preparation  
- Cleaned textual data by trimming whitespace and standardizing genre names.  
- Handled missing or null values in key rating and age columns.  
- Used SQL Server’s `STRING_SPLIT` function to normalize multi-genre data into individual genres for flexible analysis.  
- Cast rating columns to `FLOAT` to ensure safe numerical calculations.  
- Created views and CTEs to support complex queries without modifying original data.

---

## Technologies Used  
- Microsoft SQL Server for data cleaning and analysis  
- Azure Data Studio, Docker  
- Advanced SQL features like `STRING_SPLIT`, CTEs, joins, and aggregate functions  

---

## Files Included  
- `SQQuery_1.sql` — All SQL queries used for cleaning, transformation, and analysis  
- `moviesdb.csv` — Cleaned dataset used for analysis  
- `README.md` — Project overview and insights  

---

## How to Use  
1. Load your raw movie dataset into SQL Server.  
2. Run the provided cleaning and transformation SQL scripts.  
3. Execute analysis queries to reproduce insights or customize for your needs.  

---

## Key Insights  

### Platform Ratings  
- Netflix generally has higher average ratings than Amazon Prime Video:  
  - Netflix: Avg IMDb ≈ 6.2, Rotten Tomatoes ≈ 51%  
  - Amazon Prime Video: Avg IMDb ≈ 5.8, Rotten Tomatoes ≈ 42%  
- Netflix’s content is perceived as higher quality, while Amazon Prime offers more titles overall, especially in genres like Action and Drama.

### Genre-Specific Findings  
- Drama, Comedy, and Documentary consistently have higher average ratings on both platforms.  
- Horror, Mystery, and Thriller genres tend to have lower average ratings, especially on Amazon Prime Video.  
- Some genres, like Biography (≈6.82 avg IMDb) and Anime (≈6.67 avg IMDb), are well-rated but underrepresented in terms of the number of titles.  
- High volatility genres (Fantasy, Action, Adventure) show wide variation in ratings, suggesting mixed quality.  
- Documentary and Biography genres show more consistent quality with lower rating volatility.

### Audience vs. Critic Perception  
- Some movies are hidden gems — high IMDb ratings (8+) but low Rotten Tomatoes scores (~30), often in Documentary, Drama, and Comedy genres.  
- Some overhyped movies, mostly Action and Adventure, have high critic scores (RT 70+) but low audience ratings (IMDb ~5.4–5.9).  
- Most movies cluster around mid-level ratings (IMDb 5–6), indicating many average-quality films.

### Time Trends  
- Movie production increases steadily over decades, peaking in the 2000s and 2010s.  
- Drama and Comedy show strong growth, with spikes in production volume in years like 2015 and 2017.  
- Documentary, Anime, and Biography genres remain smaller but steadily grow over time.

---

## Recommendations  

### For Streaming Platforms  

**Netflix**  
- Continue emphasizing quality over quantity, which resonates well with viewers.  
- Promote strengths in genres like Horror, Action, and Adventure.  
- Use high ratings as a marketing tool to differentiate from competitors.

**Amazon Prime Video**  
- Improve content quality in lower-rated genres like Horror, Thriller, and Mystery.  
- Promote well-rated titles more effectively to enhance viewer perception.  
- Consider focusing less on sheer volume and more on curated, higher-quality offerings.

**Both Platforms**  
- Invest in underrepresented but high-rated genres like Biography and Anime to capture niche audiences.  
- Highlight hidden gems that audiences love but critics underrate.  
- Balance recommendations between critic and audience ratings, especially in high-volatility genres like Fantasy and Action.  
- Monitor genre production trends to anticipate shifts in viewer interests.

### For Viewers  
- Use both critic and audience scores when choosing movies for a fuller perspective.  
- Explore hidden gems in niche genres for fresh viewing experiences.  
- Be cautious of overhyped titles, especially in Action and Adventure genres.

---

If you have any questions or want to contribute, feel free to open an issue or submit a pull request!

---

**Author:** Ramreddy Arolla  
**Contact:** rarolla@asu.edu  
