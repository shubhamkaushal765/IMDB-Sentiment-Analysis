# Machine Learning Projects - by Shubham Kaushal

## IMDB reviews Sentiment Analysis | LSTM

### Dataset
IMDB is a dataset of 50,000 movies reviews labeled by sentiment (positive/negative). Instances have been preprocessed, and each review is encoded as a list of word indexes (integers). Words are indexed based on their frequency on the dataset. The dataset is split into a training set (25,000) and a testing set (25,000). The task is to perform sentiment analysis to classify the instances into positive or negative reviews using Recurrent Neural Networks (RNNs).

### Preprocessing
The input reviews must be converted to integers before feeding them into a model. For this preprocessing step, word embedding or vectorization is used. Two ways are explored in this project. The first is vectorizing using a matrix. Each row represents each instance and each column represents a unique word. This technique takes a huge amount of memory but is faster and easier to train. <br>

The second is using the Embedding layer and LSTM. Keras provides for both layers to be included in the model. It takes less memory, but the model is more complicated and training time is larger. <br>

For the second technique, another thing that must be taken care of is that reviews are of different lengths. Before feeding them to a model, they must be cast to the same size. For this, zero padding is used. In this technique, a maximum length is defined. Reviews with a length greater than this are truncated, and those with a smaller length get zero-padded.

### Models
<ul>
  <li> MLP (Dense model): used on the matrix representation of the dataset. Achieved 89.89% percent accuracy when trained for 10 epochs using RMSprop optimizer.
  <li> LSTM (Recurrent Neural Networks): used with the Embedding layer. This takes less memory but increases training time. Achieved 87.99% percent accuracy when trained for 5 epochs using RMSprop optimizer.
<\ul>
