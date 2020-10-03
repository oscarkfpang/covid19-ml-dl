# How Machine Learning and Deep Learning help decision-making – A practical approach using COVID-19 data
Simple forecast using public COVID-19 data in Hong Kong

# Background
Use some real-time data to demonstrate applications of machine learning (K-means Clustering) and deep learning (CNN-LSTM model on time-series data forecasting). 

The first ML notebook uses K-Means clustering to identify data centroids over the geographical distribution of buildings having probable/confirmed cases in the past 14 days in Hong Kong.

The second DL notebook compares two DL models, CNN-LSTM and TCN, on forecasting trends of COVID-19 in Hong Kong. The models are simply trained by the historical data taken from public domain, without having separated test / validation dataset for evaluation. Hyper-parameters (e.g. learning rate, epochs, etc) have been identified beforehand from some trials. The models are for demonstration purpose only and it should **not** be used for actual prediction task.

# Installation
Tested and created in Ubuntu 18 environment with the following packages installed:
+ Tensorflow v2.0.0 or above
+ [keras-tcn](https://github.com/philipperemy/keras-tcn) 
+ Jupyter Notebook
+ Numpy
+ Matplotlib
+ Bokeh
+ Pandas
+ SK-Learn
+ GoogleMaps API

Tensorflow-GPU docker running on Nvidia-docker 2 is also tested. Simply install the above into the docker environment.

# Data preparation
To successfully run the notebook, download the historical data of COVID-19 from https://data.gov.hk/en-data/dataset/hk-dh-chpsebcddr-novel-infectious-agent.

Download the "Details of probable/confirmed cases of COVID-19 infection in Hong Kong (English)" data (filename **enhanced_sur_covid_19_eng.csv**) (daily case numbers in HK) and place it under "data" folder.

Select a date range of historical data of "Residential buildings in which probable/confirmed cases have resided in the past 14 days or non-residential building with 2 or more probable/confirmed cases in the past 14 days (English)" in the website and download a range of residential buildings data of your choice. Put these csv files (filename **building_list_eng_20200901.csv**) under "data/history_data" folder.

The folder "data/processed data" is for storing the processed building data with addresses of the buildings coverted to GPS coordinates by GoogleMaps api. The code can be found in the Case 1 jupyter notebook. There is an example csv file in the folder.

# How to run the notebook
Run the two jupyter notebooks and execute the cells. If you run it in docker, you have to set up tensorboard for running in docker by forwarding tensorboard ports.

