# Wikipedia Movie Searcher

## Overview
Wikipedia Movie Searcher is a search tool that allows users to find information about movies by querying a database built from Wikipedia movie articles. The system retrieves results based on keyword searches and allows users to navigate to the corresponding Wikipedia articles.

## Features
- **Keyword Search:** Users can input keywords, and the system will return relevant movie results.
- **Advanced Search:** Allows filtering based on various fields such as title, director, year, genre, and more.
- **Search History:** Stores past searches in a text file for quick access.
- **Result Ranking:** Results are sorted by relevance, release year, or IMDb rating-to-count ratio.
- **Highlighted Keywords:** Keywords used in the search are highlighted in the results.
- **Direct Wikipedia Access:** Clicking on a movie title opens its Wikipedia page in the default web browser.

## Data Collection
- Movie data was extracted from the Wikipedia dataset available on Kaggle (`wiki_movie_plots_deduped.csv`).
- Additional metadata, including IMDb ratings and review counts, was collected using web scraping (BeautifulSoup).
- The dataset contains **34,873** movie entries.

## Indexing and Search Implementation
- **Lucene Indexing:** The system uses Apache Lucene to build an **inverted index** for fast retrieval.
- **Fields Indexed:** Title, release date, origin, director, cast, genre, URL, and IMDb rating count.
- **Search Query Handling:** Implemented using Lucene's `QueryParser` and `MultiFieldQueryParser`.
- **Stopword Removal & Tokenization:** Applied using `EnglishAnalyzer` for optimal text processing.

## Search Functionalities
### 1. Simple Search
- Users enter keywords in a search bar.
- The system returns the top results ranked by **relevance**.

### 2. Advanced Search
- Users can search using multiple fields (e.g., title, director, year, cast, etc.).
- Results can be sorted by:
  - **Relevance** (default)
  - **Release Year**
  - **IMDb Rating-to-Count Ratio**

### 3. Search History
- Previous search queries are stored in a `.txt` file.
- Users can view their past searches when reopening the application.

## User Interface
- Simple and easy-to-use UI with:
  - A **search bar** for keyword queries.
  - A **search button** to execute queries.
  - A **search history panel** for quick access to previous searches.
  - An **Advanced Search button** for filtered searches.
  - Results presented with **highlighted keywords** and clickable Wikipedia links.

## Tools
- Python 3.x
- Dependencies:
  - `BeautifulSoup` (for web scraping IMDb data)
  - `Lucene` (for indexing and searching)
    
## Credits
Eleni Mouzaki

Panagiotis Papaioannou
