# NLP Project-
This is a semster project based on the problem statement which was - 
<h2> 'Sentiment Analysis in Healthcare using Machine Learning' </h2>The problem statement given is not directed to any specialized field in Healthcare. What this project focuses on is - Classifying the sentiment of reviews of patient into two possible categories - Positive or Negative.  


## APPROACH- 
### DataSet-
The first and most important step is to find a relevant dataset which is already classified into Positve review or Negative Review. This data set then will be used for training model. 

### Data Cleaning - 
This is step is used to refine the dataset which will be used for training model. In this step each and every review is formatted by removing unwanted voacbulary present in the review. Removing punctautions, pronounce, numericals and other words (which does not help in classifying the review as positive or negative) is the crucial step which is done by creating a function and passing the dataset in it. 

### Vectors - 
Simply saying, Neural Models cannot take strings as input for machine learning therfore the string are converted to coressponding numeric representation(here we used numpy array) which can easily be used for model training. 
#### One hot vector -
The 'Positive' word is has numeric representation as [1,0] and 'Negative' as [0,1].
#### Multi hot vector - 
This is used for creating numeric representation of the reviews. This is done by first creating a dictionary of words (all the words present in the cleaned dataset). Now each review is assigned a numpy array(initialized with all values as 0) and for each word present in that review, the 0 value is replaced by index in that coressponding numpy array. <br />
For eg - The dictionary has four words - [1:'love', 2:'dog', 3:'cat', 4:'ball'] <br />
So, for a sentence - 'I love dog', the cleaned sentence will be- 'love dog' and the numpy array representing it will be [1,2]

### Model -
This project invovles a simple model which is linear regression model. The model has two hidden layers- <br />
The first layer has TanH as activation function (It is a best for linear regression model as the the values are mapped quite accurately by this function). <br />
The second layer has sigmoid as activation function cause the output of the model should be binary classified.

## RESULT - 
