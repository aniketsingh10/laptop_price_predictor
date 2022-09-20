# laptop_price_predictor

<ul>
  <li>Designed a web app that predicts the price of the laptop given the configurations. </li>
  <li>Scraped the laptops data from laptop_data.csv</li>
  <li>Developed Linear, Lasso, and Random Forest Regressors using GridsearchCV to get the best model.</li>
  <li>Deployed the Machine Learning model using streamlit library in Heroku using flask</li>
</ul>

# Links and Resources Used
<li>PyCaret Library: <a href="https://pycaret.org/">https://pycaret.org/</a></li>
<li>Streamlit Library: <a href="https://www.streamlit.io/">https://www.streamlit.io/</a>
<li>Model Deployment Video: <a href="https://www.youtube.com/watch?v=IWWu9M-aisA">https://www.youtube.com/watch?v=IWWu9M-aisA</a></li>
<li>Model Deployment Github: <a href="https://github.com/krishnaik06/Dockers">https://github.com/krishnaik06/Dockers</a></li>
<li>Packages: pandas, numpy, sklearn, flask, streamlit, joblib</li>

# Web Scraping

This is the Flipkart website comprising of different laptops. This page contains the specifications of 24 laptops. So now looking at this, we try to extract the different features of the laptops such as:
<ul>
  <li> Description</li>
  <li>Processor</li>
  <li>RAM</li>
  <li>Storage</li>
  <li>Display</li>
  <li>Warranty</li>
  <li>Price</li>
</ul>
So we extract the data from laptops.csv pages so our dataset now consists of the information the 1303 different laptops. <br>


# Feature Engineering
We go through all the features one by one and keep adding new features. I have made the following changes and created new variables:
RAM - Made columns for Ram Capacity in GB and the DDR version <br>
Processor - Made columns for Name of the Processor, Type of the Processor, Generation <br>
Operating System - Parsed the Operating System from this column and made a new column <br>
Storage - Made new columns for the type of Disk Drive and the capacity of the Disk Drive <br>
Display - Made new columns for the size of the laptop(in inches) and touchscreen <br>
Description - Made new columns for the company and graphic card <br>

# Data Preprocessing
There are a few columns which are categorical here but they actually contain numerical values.So we need to convert few categorical columns to numerical columns. These are DDR_Version,Generation,Storage_GB,Price.

# Model Building
![Screenshot (90)](https://user-images.githubusercontent.com/97386407/191269612-c0385e02-d243-4ab9-80df-329c6f7f8454.png)

# Model Deployment
I have deployed the model using Streamlit library and flask framework on Heroku which is a Platform As A Service(PAAS)
![Screenshot (88)](https://user-images.githubusercontent.com/97386407/191269794-f113517e-bf33-4f54-827c-305dba409b21.png)

Web application: <a href="https://lapi-price-predictor.herokuapp.com/">https://lapi-price-predictor.herokuapp.com/</a>
