<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

# Project Title

Final project for the Building AI course

## Summary

This project creates a simple sentiment analysis tool that analyzes text input (e.g., user reviews or social media posts) to determine whether the sentiment is positive, negative, or neutral. It's aimed at helping businesses understand customer feedback.

## Background

Manual analysis of customer feedback is slow and inconsistent.
Businesses struggle to efficiently track and act upon customer sentiments.
There’s a need for a simple tool to categorize sentiment in text data.


## How is it used?

Users simply enter a piece of text, such as a product review or comment, into the tool. The AI then analyzes the text and returns a sentiment label: Positive, Negative, or Neutral.

This solution is useful in situations such as:

Analyzing customer reviews for products or services.
Monitoring social media feedback.
Gathering insights for product improvement or marketing strategies.

from textblob import TextBlob

Example code:

def analyze_sentiment(text):
    # Create a TextBlob object
    blob = TextBlob(text)
    # Get the polarity of the text
    polarity = blob.sentiment.polarity
    # Determine sentiment based on polarity
    if polarity > 0:
        return "Positive"
    elif polarity < 0:
        return "Negative"
    else:
        return "Neutral"

# Example usage
review = "I love this product! It's amazing."
print(analyze_sentiment(review))  # Output: Positive



## Data sources and AI methods
This project utilizes the TextBlob library for sentiment analysis. TextBlob is a simple NLP library built on top of NLTK, designed for tasks such as part-of-speech tagging, noun phrase extraction, and sentiment analysis.

No custom data collection is required for this basic implementation, as it uses a pre-trained sentiment analysis model available in the TextBlob library.

## Challenges

This project does not handle sarcasm or context-dependent phrases well, which could lead to inaccurate sentiment classification in certain cases. Ethical considerations include ensuring the tool doesn't perpetuate bias in sentiment interpretation or misclassify text due to language nuances.

## What next?

Training a custom sentiment analysis model using deep learning techniques for better accuracy.
Expanding the tool to detect emotions such as joy, sadness, or anger.

## Acknowledgments

* TextBlob library: TextBlob GitHub
NLTK library: NLTK
Sentiment analysis tutorial
