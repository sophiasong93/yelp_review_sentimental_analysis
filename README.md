# Project Overview
In this project, a text classifier using Natural Language Process (NLP) is built and focus on restaurant reviews on Yelp. 
The objective is to predict whether a review is positive or negative based on the context of the reviews. By implementing a prediction algorithm, a daily report for
the restaurants can be created and be used as sentiment analysis of the reviews.

### Data Source
Yelp open dataset 2020, yelp_business.json and yekp_review.json

### Downsize original Data 
To process the data that can be used as training data for our model, first downsized the dataset with three criterias: 
a. Drop rows with blank fields; 
b. Filtered category keywords including “Restaurant”; 
c. Category label length less than 4. 

With the data preprocessing, we have a cleaned and normalized CSV file as yelp_business.csv and the corresponding yelp_review.csv. Then merge the business information with corresponding reviews by business_id and create a new csv file with all the columns we need for further analysis.

### Data Preprocessing
The data preprocessing includes five main tasks: 
text cleaning, text normalization, tokenizer and pad sequence, prepare train/test data set, and creating word embedded vectors.

### Model
RNN model consisted of an embedding layer, a dropout layer, a LSTM layer with dropout, and the output from LSTM was fed into a hidden fully connected layer. For the
embedding layer, we passed 10000 features named as max_words, input length 200 as maxlen, and 32 as the timestep to form the dimension of the embedding layer. For the LSTM layer, the first parameter is the same as the third parameter from the embedding layer, and we added a 30% chance of dropout with L2 regularization. The activation function used in a dense layer is sigmoid function.

### Version
2020 Dec
