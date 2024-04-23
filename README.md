# Sentiment Analysis of Airline Reviews
Sentiment analysis of Airlines customer reviews using Libraries and tools in Python

## Project Overview

This project involves scraping airline reviews from a website and performing sentiment analysis using two different tools: TextBlob and VADER (Valence Aware Dictionary and sEntiment Reasoner). The objective is to evaluate the sentiments expressed in customer reviews and visualize the distribution of these sentiments to gain insights into customer satisfaction.

## Methodology

1. **Data Collection**: Reviews are scraped from the airline quality review website using BeautifulSoup.
2. **Data Preprocessing**: Reviews are cleaned by removing non-alphabetic characters, punctuation, and stopwords.
3. **Sentiment Analysis**:
   - **TextBlob**: Used to get a baseline sentiment polarity.
   - **VADER**: Specifically tuned for social media content to provide a more nuanced analysis.
4. **Visualization**: Sentiment distributions are visualized using histograms to compare the results from both tools.

## Tools Used

### TextBlob
TextBlob is a Python library for processing textual data. It provides a simple API for diving into common natural language processing (NLP) tasks such as tagging, noun phrase extraction, sentiment analysis, classification, translation, and more.

- **Accuracy**:
  - TextBlob’s sentiment analysis is rule-based and relies on predefined sets of categorized words.
  - It performs well for simple cases but may not be highly accurate.
  - To improve accuracy, consider training your own sentiment classifier using a custom dataset1.
- **Efficiency**:
  - TextBlob’s approach is efficient for basic sentiment analysis tasks.
  - It uses an “averaging” technique to compute polarity scores for individual words.
  - Handles negations and provides combined polarity for longer texts2. 
- **Sentiment Polarity**: TextBlob returns two properties, polarity and subjectivity, where polarity is a float within the range [-1.0, 1.0] and indicates the sentiment. Negative values indicate negative sentiment, positive values indicate positive sentiment, and zero indicates neutral.

### VADER
VADER (Valence Aware Dictionary and sEntiment Reasoner) is a lexicon and rule-based sentiment analysis tool that is specifically attuned to sentiments expressed in social media.

- **Accuracy**:
  - VADER performs remarkably well, often matching human raters in sentiment classification.
  - F1 scores (classification accuracy) show that VADER (0.96) outperforms individual human raters (0.84) in correctly labeling sentiment as positive, neutral, or negative1.
  - VADER’s sensitivity to both polarity and intensity contributes to its accuracy.
- **Efficiency**:
  - VADER is resource-efficient and doesn’t require extensive training.
  - It’s designed for real-time analysis of streaming data (e.g., tweets, news headlines).
  - The valence scores assigned to words are based on observation and experience, making it efficient and effective1.
- **Sentiment Polarity**: VADER provides a compound score that aggregates the polarity into a single normalized score. The `compound` score ranges from -1 (most negative) to 1 (most positive).

## Sentiment Polarity

Sentiment polarity quantifies the emotional content of the text, indicating whether the tone is positive, negative, or neutral. Understanding sentiment polarity allows businesses to gauge overall sentiment trends from customer feedback, enabling better decision-making and customer relationship management.

## Example analysis

![vaderanalysis](https://github.com/Lalith-Sagar-Devagudi/Sentiment-Analysis-Airlines-Reviews/assets/40135491/6b790db2-b70a-4d48-9be7-437cd4fe3820)

