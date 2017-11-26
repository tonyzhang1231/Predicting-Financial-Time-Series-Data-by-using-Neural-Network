# Predicting-Financial-Time-Series-Data-by-using-Neural-Network

In this project, we aim to predict the close price of sp500 index based on the previous 22 days from year 1950 - 2017.

This work is based on [BenjiKCF's work](https://github.com/BenjiKCF/Neural-Network-with-Financial-Time-Series-Data). This result is much better since the models are optimized. 

There are 2 models. Neural network and lstm-rnn.


- Filename: NN_ClosePrice_prediction.ipynb

- Filename: LSTM_ClosePrice_prediction.ipynb

NN model result

![Alt text](https://github.com/tonyzhang1231/Predicting-Financial-Time-Series-Data-by-using-Neural-Network/blob/master/png/nnmodel.png?raw=true)

Train Score: 0.00003 MSE (0.00574 RMSE)

Test Score: 0.00009 MSE (0.00934 RMSE)

LSTM model result

Train Score: 0.00001 MSE (0.00325 RMSE)

Test Score: 0.00006 MSE (0.00765 RMSE)

![Alt text](https://github.com/tonyzhang1231/Predicting-Financial-Time-Series-Data-by-using-Neural-Network/blob/master/png/lstm.png?raw=true)

LSTM has better result than regular Neural network

# Future improvement:
1. Sentiment analysis will be added as features
2. More indexes and stocks will be included

# Some Notes
1. CuDNNLSTM is much faster than LSTM, in my experience, it's around 5x. 
2. Predicting close price is very challenging, both complex model are beaten by naive prediction.


# How to set up the environment and train the model
I suggest using  `virtualenvwrapper`, then this project will not affect others
- Set up a virtualenv with python3 (same for python2)

`mkvirtualenv --python=/usr/bin/python3 nameOfyourEnvironment`

`workon nameOfyourEnvironment`

- Install all the requirements

`pip install -r requirements.txt`

- Install tensorflow and keras with gpu enabled

`pip install tensorflow-gpu`

`pip install keras`

- Setup ipykernel

`pip install ipykernel`

`python -m ipykernel install --user --name=nameOfyourEnvironment`

- Open jupyter notebook, choose nameOfEnvironment kernel

