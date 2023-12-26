# IMDb Movie Review Scraper and Sentiment Analysis

This project revolves around automating the extraction of user reviews for the movie "The Sound of Music" from IMDb. Leveraging Selenium WebDriver, it navigates the IMDb page, loads all available reviews, and then performs sentiment analysis on the collected data.

## Setup

### Prerequisites
- Python 3 installed
- Required libraries: Selenium, BeautifulSoup, NLTK, pandas, Matplotlib
- Chrome WebDriver installed (for Selenium)

### Installation Steps

1. **Install Python 3**: Download and install Python 3 from the [official website](https://www.python.org/downloads/).
   
2. **Install Required Libraries**: Use pip, the Python package manager, to install the necessary libraries.
   ```bash
   pip install selenium beautifulsoup4 nltk pandas matplotlib
   ```
    
Chrome WebDriver Installation:

Download the Chrome WebDriver matching your Chrome browser version from Chrome WebDriver Downloads.
Place the WebDriver executable in a directory accessible from your system's PATH.
Run the Script: Execute the provided Python script to automate the data extraction and sentiment analysis.


## Overview of the project   
## **Data Acquisition**

The script initiates a Chrome WebDriver session using Selenium and directs it to the IMDb page containing the movie reviews. It simulates user interactions by clicking the "Load More" button repeatedly until all reviews are visible. Once all reviews are loaded, the HTML content of the page is extracted for further processing before closing the WebDriver session.

## **Data Extraction**

The obtained HTML content undergoes parsing using BeautifulSoup to extract crucial information from individual review containers. It captures reviewer names, review dates, and review texts, ensuring a comprehensive extraction while handling potential cases where certain data might be missing.

---

### **Sentiment Analysis**

Following the data extraction phase, the script performs sentiment analysis on the collected reviews using VADER (Valence Aware Dictionary and sEntiment Reasoner) from the NLTK library. VADER's SentimentIntensityAnalyzer analyzes the review texts to generate negative, neutral, positive sentiments, and an overall compound score for each review.

### **Data Structuring**

The sentiment analysis results are structured into a pandas DataFrame named 'scored_reviews.' This DataFrame presents a comprehensive view of reviewers' sentiments, aiding in better comprehension and analysis of the collected data. Each review's sentiment scores, along with reviewer names and dates, are organized into columns for further analysis.

---

### **Visualization**

The project culminates in visualizing the sentiment data. It computes the mean compound sentiment score per year and creates a bar chart using Matplotlib. The bar chart illustrates how sentiment has trended over different years based on the analyzed reviews, providing an overview of the movie's reception over time.

Additionally, Matplotlib is utilized to generate a 2x2 grid of histograms. Each histogram represents a different sentiment score (negative, neutral, positive, compound) derived from the 'scored_reviews' dataset. These histograms showcase the distribution of sentiment scores within their respective categories, aiding in understanding the frequency of sentiments expressed by reviewers.

---

This README provides an in-depth insight into the process of automated data extraction, sentiment analysis, and subsequent visualization, allowing for a comprehensive understanding of user opinions and sentiments towards "The Sound of Music" movie on IMDb.
