# Next Word Prediction using Statistical NLP
Next word prediction software observes what the user types and predicts what will be the next word based on the words typed and suggests the word to the user. Language model predicts the probability of sequence of words. So, it has been adopted to accomplish the task.
We have 4 important tasks in this work. They are:-
1.	Data Collection
2.	Data preprocessing
3.	Develop language model 
4.	Prediction

# Data Collection:-
The first and foremost task we do is data collection. We didn’t take an existing corpus directly. Rather, we scraped data from the URLs related to environmental sciences like pollution, global warming, climate change etc.. and created a data set. We used 57 URLs to scrap data. 

# Data Preprocessing:-
The second step is data preprocessing. Preprocessing is done to convert the raw text into understandable and needed format. In this step, we do a lot of tasks like removing numbers, percentages, links/URL, special characters and all punctuations except period (.), non-English text (if any) as they are not at all significant in predicting the next word. 
After preprocessing, we perform normalization. Normalization is done to convert the data into standard form. We perform tasks such as case folding and removal of additional whitespaces. Now we have a clean data set. 

# Language model creation (bigram, trigram and quadgram model):
We now move on to the third step, wherein we create the language model. We created bigram, trigram and quadgram models which calculate the probabilities of the possible next words based on the previous word, two words and three words respectively. We choose the word with the maximum probability as the next word and display it to the user. 

# Prediction:
If the length of the user input is >=3, send the last 3 words as input to the quadgram model. If empty result set is returned by the quadgram model, then send the last 2 words in the user input as input to the trigram model. If that result set is also empty, we move on to bigram model. If the result set is not empty, then it will hold the word with the maximum probability. So, it will be suggested to the user.
And, it should be noted that our model will not predict any word if the typed sequence of words is not found in our data set.  

