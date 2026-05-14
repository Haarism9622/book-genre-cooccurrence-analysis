# Co-occurrence Analysis of Book Genres in Goodreads Dataset

## Objective
The objective was to analyze co-occurrence relationships between book genres in a large Goodreads dataset to find common genre combinations and reading patterns

## Dataset
[GoodReads 100k Dataset](https://www.kaggle.com/datasets/mdhamani/goodreads-books-100k)

## Data Preprocessing/Data Cleaning
**Converting Genre Column to Lists**
The Genre column was initially stored in  string format with most books contained more than one genre.
- Ex: Couture,Fashion,Historical,Art,Nonfiction

To prepare the data for analysis, the column was converted into list format where each genre is a separate element.   
- Ex: [Couture, Fashion, Historical, Art, Nonfiction]


## Model: Co-occurrence Analysis
Why this Model?
- Identifies relationship between genres
- Detects frequent Genre combinations
- Effective for multi-label categorical data

## Methodology
**4-Step Algorithm**
1. Count Singles: The first step is to find how many unique genres can be found across all books. 
  - 1176 Unique Genres across 89,533
2. Count Pairs: Count how often two genres appear together in the same book.
  - 94,277 Unique genre pairs
3. Compute Metrics: Calculate the Support, Confidence and Lift metrics for each genre pair
4. Filter & Rank: Remove weak or rare genre pairs. Rank strongest genre associations for analysis.
 


## Key Findings
- Fiction and Nonfiction are the most dominant genres, acting as broad categories that overlap with many subgenres.
- Strong thematic relationships were identified between genres, such as fiction and romance, as well as fiction and science fiction
- The co-occurrence heatmap showed clear clusters, indicating that related genres frequently appear together
- Most genre pairs appeared to have low support indicating many genre relationships were niche and loosely connected
- A small number of genre pairs showed extremely high lift values, representing strongly associated genre combinations
- Popularity related features such as ratings and reviews contain significant outliers, with a small number of books dominating reader engagement. 

