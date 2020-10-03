# covid19-ml-dl
Simple forecast using public COVID-19 data in Hong Kong

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

Download the "Details of probable/confirmed cases of COVID-19 infection in Hong Kong (English)" csv file (daily case numbers in HK) and place it under "data" folder.

Select a date range of historical data of "Residential buildings in which probable/confirmed cases have resided in the past 14 days or non-residential building with 2 or more probable/confirmed cases in the past 14 days (English)" in the website and download a range of residential buildings data of your choice. Put these csv files under "data/history_data" folder.

The folder "data/processed data" is for storing the processed building data with addresses of the buildings coverted to GPS coordinates by GoogleMaps api. The code can be found in the Case 1 jupyter notebook. There is an example csv file in the folder.

# How to run the notebook
Run the two jupyter notebooks and execute the cells. If you run it in docker, you have to set up tensorboard for running in docker by forwarding tensorboard ports.

