# Sentiment-Analysis

## Dataset
The dataset is comprised of tab-separated files with phrases from the Rotten Tomatoes dataset. Each Sentence has been parsed into many phrases by the Stanford parser. Each phrase has a PhraseId. Each sentence has a SentenceId. Phrases that are repeated (such as short/common words) are only included once in the data.

train.tsv contains the phrases and their associated sentiment labels.
test.tsv contains just phrases. The task is to assign a sentiment label to each phrase.
The sentiment labels are:
0 - negative
1 - somewhat negative
2 - neutral
3 - somewhat positive
4 - positive

## Techniques Used

For preprocessing, firstly, all the stopwords and special characters were removed using the NLTK library. 
Then, after tokenization, the words were changed to their root form using lemmatization.
Same process was used for both training and test set. 

Count Vectorizer and Tfidf Transformer were used to convert the texts to numbers and convert the data into a sparse matrix which could be fed to the classifier model.

## Classifier

I used Decision Tree Classifier to identify the sentiments associated with all the reviews. 

## Performance

It was able to achieve an accuracy of 58.9% on the test set. Considering the best score of the competition was 65%, the results are pretty good. 
