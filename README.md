

Name:Adarsh mishra  
Company:CODTECH IT SOLUTIONS  
ID:CTO8DS3576  
Domain:ARTIFICIAL INTELLIGENCE    
Duration:JULY 1st 2024 to AUGUST 1st 2024  

## Overview of the project:
### PROJECT:Sentiment analysis in NLP
__objective:__
The objective of this Project is to sentiment analysis on amazon reviews dataset. This project analysizes the emotion behind the text using VADER method  
### Steps_Involving:  
1)__Data Collection:__ Gather text data from various sources like social media, reviews, surveys, etc  
2)__Text Preprocessing:__  
       * Tokenization: Splitting text into individual words or phrases.  
       * Lemmatization/Stemming: Reducing words to their base or root form.   
       * Stop Words Removal: Removing common words that do not contribute much to meaning (e.g., "the", "and").   
3)__Feature Extraction:__   
       * Bag of Words: Represents text data as a collection of word frequencies.  
       * TF-IDF (Term Frequency-Inverse Document Frequency): Weighs the importance of a word in a document relative to a collection of documents.  
       *  Word Embeddings: Using pre-trained models like Word2Vec, GloVe, or FastText to convert words into vector representations.  
4)__Model Selection:__  
       * Choose between lexicon-based, machine learning, or deep learning approaches.  
       * Train the model on labeled data if using machine learning or deep learning methods.  
5) __Sentiment Analysis:__  
       * Apply the model to analyze the sentiment of new text data.  
       * Calculate sentiment scores or classifications.  

### Technology used:  
1)__python__: The primary programming language used to implement VADER.  
2)__NLTK__:Natural Language ToolKit a powerful python library for working with human language data.
3)__VADER lexicon__: A dictionary that maps lexical features to sentiment intensity scores which have been manually annotated by human raters.  
3)__Text Processing Tools__: tokenization,lemmatization,and other preprocessing techniques are used to prepare the text for sentiment analysis

### Expalanation:
 VADER sentiment scoring technique involves taking all the word from the statment and assigning them with positive ,negative and neutral responses .This responses
 tells how positive or negative or netural is our statement is.  
 here is the complete step by step guidance.  

__step 1__: collect the dataset and import all necessary headers  

>import pandas as pd  
import matplotlib.pyplot as plt  
import seaborn as sns  
from nltk.sentiment.vader import SentimentIntensityAnalyzer  
from tqdm.notebook import tqdm.  

__step 2__: read the review.csv file using pandas 

>df=pd.read_csv('Reviews.csv')  
 df=df.head(500).

__step 3__: creating an object for sentimentIntensit Analyzer . Its the key component of the VADER sentiment analysis tool. it is responsible for 
 evaluating the intensity of sentiments expressed in text. 

  >x=SentimentIntensityAnalyzer().
__step 4__: in this step we will apply analyzer to whole dataset

>data=[]
polarity=[]
for i in range(0,len(df)):  
    data.append(df['Text'][i])  
    compound_score=x.polarity_scores(df['Text'][i])   
    ans=compound_score['compound']  
    if ans>=0.05:  
        ans="positive response"  
    elif ans<=-0.05:  
        ans="Negative response"  
    else:  
        ans="Neutral Response"  
    polarity.append(ans)  
sf=pd.DataFrame({"text":data,"polar":polarity})  
print(sf.head())

## conclusion:
   these project involves taking any text or dataset as input an applying  sentiment analysing on it. If the polarity score is less then or equal to -0.05 this shows that the response is negative 
   and if the polarity score is greater then equal to 0.05 then the response is positive else neutal response



![Screenshot 2024-07-28 145709](https://github.com/user-attachments/assets/71462c99-8bc9-4b95-8844-8500e03518dc)


