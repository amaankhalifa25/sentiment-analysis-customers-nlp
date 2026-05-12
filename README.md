# Sentiment Analysis Customers NLP

## Overview
This project performs sentiment analysis on customer reviews from Amazon and Starbucks using Natural Language Processing (NLP) techniques.

The project uses:
- TextBlob
- VADER Sentiment Analysis
- Pandas
- Python
- Jupyter Notebook

## Features
- Text preprocessing
- Sentiment classification
- Data cleaning
- Visualization
- Classification reports
- Confusion matrix analysis

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- TextBlob
- NLTK
- Scikit-learn

## Dataset
Datasets obtained from Kaggle customer review datasets. 
Amazon csv file available from the Kaggle link: https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset
Starbucks csv file available from: https://www.kaggle.com/datasets/harshalhonde/starbucks-reviews-dataset


# Project Workflow

## 1. Data Loading and Exploration

Datasets were loaded using pandas and explored using:
- `head()`
- `info()`
- `describe()`
- missing-value analysis

This provided an understanding of:
- dataset structure
- variable types
- missing values
- customer rating distributions

---

# 2. Text Preprocessing

Customer review text was cleaned before sentiment analysis by:
- converting text to lowercase
- removing punctuation
- removing numerical values
- standardising whitespace

A custom Python preprocessing function using regular expressions (`re`) was applied to review text columns.

---

# 3. TextBlob Sentiment Analysis

TextBlob was used to generate polarity sentiment scores ranging from:
- `-1` → strongly negative sentiment
- `0` → neutral sentiment
- `+1` → strongly positive sentiment

TextBlob sentiment scores were added as new dataframe columns and analysed using:
- descriptive statistics
- histograms
- scatter plots
- correlation analysis

---

# 4. VADER Sentiment Analysis

VADER sentiment analysis was added as a second NLP method to compare against TextBlob.

VADER is specifically designed for:
- social media text
- customer reviews
- emotionally expressive language

VADER generated compound sentiment scores ranging from:
- `-1` → negative sentiment
- `+1` → positive sentiment

The project compares how VADER and TextBlob behave differently across customer review datasets.

---

# 5. Visualisation and Exploratory Data Analysis

Several visualisations were created including:
- histograms of sentiment score distributions
- scatter plots comparing ratings vs sentiment scores
- comparison histograms between TextBlob and VADER
- confusion matrices for classification evaluation

These visualisations helped identify:
- sentiment skew
- class imbalance
- rating/sentiment relationships
- outliers
- sentiment intensity differences between NLP methods

---

# 6. Sentiment Classification and Evaluation

Customer ratings were converted into:
- negative
- neutral
- positive

sentiment classes.

TextBlob and VADER sentiment scores were also converted into classification labels and evaluated using:
- accuracy
- precision
- recall
- F1-score
- confusion matrices

---

# Results and Interpretation

## Amazon Dataset Results

### TextBlob Results
- Classification Accuracy: **96.66%**
- Correlation with Numeric Ratings: **0.1825**

TextBlob achieved very high classification accuracy on the Amazon dataset. However, this result was influenced by class imbalance, as most reviews in the dataset were positive. The confusion matrix and classification report showed that TextBlob performed well on positive reviews but struggled to identify the small number of negative and neutral reviews.

The histogram of sentiment scores showed a positive skew, with most reviews clustered around the positive sentiment values. The scatter plot comparing ratings and sentiment scores showed a weak positive relationship between customer ratings and textual sentiment.

---

### VADER Results
- Classification Accuracy: **94.06%**
- Correlation with Numeric Ratings: **0.2288**

VADER produced slightly lower classification accuracy than TextBlob but generated stronger sentiment intensity values. The VADER sentiment distribution showed more extreme positive and negative scores compared with the TextBlob distribution.

VADER also showed a slightly stronger correlation with customer ratings than TextBlob, suggesting that VADER sentiment scores aligned more closely with customer rating behaviour on a continuous scale.

---

### Amazon Interpretation

The Amazon dataset was overwhelmingly positive, with very few negative reviews present. This caused both TextBlob and VADER to achieve high overall accuracy while still performing poorly on minority sentiment classes.

The analysis demonstrated that:
- accuracy alone can be misleading in imbalanced datasets
- customer ratings and written sentiment are related but not perfectly aligned
- NLP tools may struggle with sarcasm, and mixed sentiment reviews

---

# Starbucks Dataset Results

### TextBlob Results
- Mean Sentiment Score: **0.0313**
- Correlation with Numeric Ratings: **0.5409**
- Minimum Sentiment Score: **-0.8000**
- Maximum Sentiment Score: **0.8250**

Unlike the Amazon dataset, the Starbucks reviews showed a much more balanced sentiment distribution. The average sentiment score was close to neutral, indicating that customer opinions were mixed overall.

The histogram showed a wider spread of positive and negative sentiment values, while the scatter plot demonstrated a clearer relationship between customer ratings and text sentiment.

TextBlob showed a relatively strong positive correlation with customer ratings in the Starbucks dataset.

---

### VADER Results
- Mean Sentiment Score: **-0.0027**
- Correlation with Numeric Ratings: **0.4546**
- Minimum Sentiment Score: **-0.9879**
- Maximum Sentiment Score: **0.9938**

VADER generated much more extreme sentiment values than TextBlob, with sentiment scores being closer to -1 and +1. The VADER histogram showed stronger separation between negative and positive sentiment regions.

Although VADER had a slightly weaker correlation with customer ratings compared with TextBlob, it captured emotional intensity more accurately and produced clearer sentiment extremes.

---

### Starbucks Interpretation

The Starbucks dataset provided a more realistic and challenging sentiment-analysis scenario because it contained a wider range of customer opinions and more negative reviews.

The key findings included:
- customer ratings and textual sentiment that showed a clearer relationship than the Amazon dataset
- TextBlob produced smoother sentiment distributions
- VADER generated more emotionally intense sentiment values
- both methods highlighted the complexity of interpreting customer feedback automatically

The Starbucks analysis demonstrated how dataset characteristics can significantly affect NLP sentiment-analysis performance.

## Author
Amaan Khalifa
