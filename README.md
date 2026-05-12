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

## Future Improvements
- Machine learning classifiers
- Deep learning sentiment models
- Advanced NLP preprocessing
- Comparison between platforms

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

## Author
Amaan Khalifa
