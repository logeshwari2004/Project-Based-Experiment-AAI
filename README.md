<H3>ENTER YOUR NAME:LOGESHWARI.P</H3>
<H3>ENTER YOUR REGISTER NO:212221230055</H3>
<H3>DATE:15.05.2024</H3>
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective:Perform sentiment analysis using your Facebook data and filter the data that has only negative feedback for the code given in the following link.<H3>

<H3>Program:</H3>

```
pip install pandas textblob
import pandas as pd
from textblob import TextBlob

# Load the CSV file into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Output the DataFrame with sentiment analysis results
print(df.head())

# Filter out rows with negative sentiment (label 'N')
negative_feedback = df[df['Label'] == 'N']

# Output the negative feedback
print(negative_feedback)
```

<H3>Output:</H3>

![329918019-a6539c89-7efd-4679-b2d3-b7da9feb4393](https://github.com/logeshwari2004/Project-Based-Experiment-AAI/assets/94211349/1eca63b6-e706-4224-9749-48220d39bfc7)





<H3>Inference:</H3>
Thus sentiment analysis using your Facebook data ias done and filtering the data that has only negative feedback for the code is done.
