# Netflix Content Analysis

Exploratory data analysis (EDA) of 8,807 Netflix titles (movies and TV shows) to understand what the catalog contains and how it has grown.

**Tools:** Python, Pandas, Matplotlib, Seaborn (Google Colab / Jupyter)
**Dataset:** [Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows) on Kaggle (`netflix_titles.csv`, 8,807 rows, 12 columns)

## Questions answered
1. How much of the catalog is movies vs TV shows?
2. How has content added per year changed over time?
3. What are the most common genres?
4. Which countries produce the most content?
5. How long are movies?

## Data cleaning
- Filled missing `director`, `cast`, `country` and `rating` values with "Unknown".
- Converted `date_added` to a date and created a `year_added` column. 10 rows have no date and were left empty.
- Removed duplicate rows.
- Split `duration` into a number (minutes for movies, seasons for TV shows). 3 rows have no duration and were left empty.

## Key findings
- **Movies are 69.6%** of the catalog and TV shows are 30.4%.
- **Titles added per year grew from 82 in 2015 to a peak of 2,016 in 2019.** The data ends on 25 Sep 2021, so 2021 (1,498 titles) is a partial year and isn't directly comparable.
- **Most common genre tags:** International Movies (2,752), Dramas (2,427) and Comedies (1,674). A title can carry several tags, so the counts overlap.
- **Top producing countries** (among titles with a listed country): United States (3,689) and India (1,046), followed by the United Kingdom, Canada and France. Co-productions count once per country.
- **The median movie runs 98 minutes.**

## Limitations
- 831 titles have no listed country, so country results cover only titles with one.
- The dataset is a snapshot ending in September 2021, so it doesn't show later changes.

## How to run
1. Download `netflix_titles.csv` from the Kaggle link above, or use the copy in this repo.
2. Open `Netflix_Content_Analysis.ipynb` in Google Colab or Jupyter.
3. Upload the CSV next to the notebook and run all cells.

## Next steps
- Build a Power BI dashboard from the cleaned data.
- Add a ratings analysis.
