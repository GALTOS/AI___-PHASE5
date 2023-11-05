# First, you need to install TextBlob if you haven't already:
pip install textblob

from textblob import TextBlob

# Sample text for sentiment analysis
sample_text = "I love this product. It's amazing!"

# Create a TextBlob object
analysis = TextBlob(sample_text)

# Perform sentiment analysis
polarity = analysis.sentiment.polarity
subjectivity = analysis.sentiment.subjectivity

# Determine sentiment based on polarity
if polarity > 0:
    sentiment = "Positive"
elif polarity < 0:
    sentiment = "Negative"
else:
    sentiment = "Neutral"

# Print the results
print(f"Text: {sample_text}")
print(f"Polarity: {polarity} (Sentiment: {sentiment})")
print(f"Subjectivity: {subjectivity}")
