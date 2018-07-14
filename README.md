# Financial Modeling: Forecasting Securities

This project showcases an attempt to forecast securities using technical indicators (historical stock data) and, in a sense, the potential to earn capital using filings types from the United States Securities & Exchange Commission (SEC).

------

## Table of Contents

- [Problem Statement](#Problem-Statement)
- [Assumptions](#Assumptions)
- [Introduction](#Introduction)
- [Built with](#Built-with)
- [Directory Structure](#Directory-Structure)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Preprocessing Data](#Preprocessing-Data)
- [Optimal Model](#Optimal-Model)
- [Conclusion](#Conclusion)
- [Credits](#Credits)

-----

## Problem Statement 


The problem at hand is to evaluate and predict securities using statistical analyses of market activity (e.g. price & volume) and SEC filings.

-----

## Assumptions

The initial assumption is that the market moves in trends, therefore engineering short, medium, and long term patterns/trends (moving averages) will be a good indicator and trading strategy.

-------

## Introduction

This project is broken down into two main sub-directories. Beginning with, [Stocks](../capstone/stocks), which is the indicative dataset containing the historical price of a security. The second, is the [SEC](../capstone/sec), directory, where the data concerning with SEC filings is scraped and analyzed. Below, is a more extensive introduction and overview of the project and it's to sub-directories.

#### Stock Data:
 The indicative, or stock, data is sourced from [Quandle](https://www.quandl.com/)'s API and is a data set of historical stock data since the company's Initial Price Offering, which is the very first sale of stock issued by a company to the public.

Subsequently,  [Exploratory Data Analysis](../capstone/stocks/Apple_EDA.ipynb) (EDA) is performed. During this stage the data is analyzed, visualized, and feasture engineering. Feature engineering is the process of transforming the raw data into to effectively represent the underlying problem in predictive modeling. In the attempt to engineer the data, *moving averages*, *percent changes*, and *difference* in values are calculated--if these concepts are foreign to you, please do not worry as these concepts will be discussed in further detail  later. 

Upon analyzing and engineering the features, the data is [preprocessed](../capstone/stocks/Apple_Model_1_Data_Prep.ipynb) and prepared for predictive modeling.  Since the stock data is sequential and dealing with time, the training and testing set were done manually. 

Thereafter, the data is trained using machine learning models such as: [Linear](../capstone/stocks/Apple_Model_2_Linear_Regression.ipynb) Regression, [Random Forest](../capstone/stocks/Apple_Model_3_Random_Forest.ipynb) Regression, [Bagging Regression](../capstone/stocks/Apple_Model_3_Random_Forest.ipynb) on a Random Forest, and Regression using Facebook's [Prophet](../capstone/stocks/Apple_Model_5_Prophet.ipynb). 

#### SEC Data:

The [SEC](../capstone/sec) data is sourced from the [SEC website](https://www.sec.gov/), where the data was scraped using the *BeautifulSoup* library. Upon obtaining the documentation types, some brief [Exploratory Data Analysis](../capstone/sec/Apple_SEC_EDA.ipynb). During this brief analysis, some of document types where grouped accordingly and visualized to understand the frequency of filing. 

 Moreover, the SEC data was [merged](../capstone/stocks/Apple_EDA_wSEC.ipynb) with the stock data to further analyze, visualize, and feature engineer the data. The objective was to find whether an type of SEC filing was correlated to the price of the security.

Following the EDA, the data was [prepared](../capstone/stocks/Apple_Model_Classification_1_Prep.ipynb), turning files into binary values and manually splitting the train and test sets. Subsequently, the data was ready to be modeled using a [Random Forest](../capstone/stocks/Apple_Model_Classification_3_Random_Forest.ipynb) Classification Model.

----------

## Built with

#### This project was built with the following tools:
- Python
- Jupyter Notebook/Lab
- Seaborn
- Motplotlib
- Numpy
- Pandas
- [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
- [Quandle](https://www.quandl.com/)
- [Scikit Learn](http://scikit-learn.org/stable/index.html#)
- [Facebook Prophet](https://research.fb.com/prophet-forecasting-at-scale/)
- [BeakerX](http://beakerx.com/)


#### Installations

If the repository is downloaded and the notebooks would liked to be ran using Jupyter Notebook/Lab, please install the dependencies below:

- [Quandle](https://docs.quandl.com/docs/python-installation)
- [Installing Quandle](https://docs.quandl.com/docs/python-installation)
- [Installing Scikit Learn](http://scikit-learn.org/stable/install.html)
- [Installing Prophet](https://github.com/facebook/prophet)
- [BeakerX](http://beakerx.com/)
----------


## Directory Structure
An index of both directories are provided below.
### Stocks:

The [Stocks](../capstone/stocks) directory has notebooks analyzing *Apple, Inc.* and are broken down as:

#### Continuous Data Analysis, Preprocessing, and Modeling:

- Apple [Exploratory Data Analysis](../capstone/stocks/Apple_EDA.ipynb) on Historical Stock Data.
- Apple Exploratory Data Analysis [Interactive Graphs](../capstone/stocks/Apple_EDA_BeakerX.ipynb).
- Apple [Preparing the Data](../capstone/stocks/Apple_Model_1_Data_Prep.ipynb) for Regression Modeling.
- Apple Modeling: [Linear Regression](../capstone/stocks/Apple_Model_2_Linear_Regression.ipynb).
- Apple Modeling: [Random Forest Regression](../capstone/stocks/Apple_Model_3_Random_Forest.ipynb)
- Apple Modeling: [Bagging Regression on a Random Forest](../capstone/stocks/Apple_Model_4_Bagging_Regressor.ipynb).
- Apple Modeling: [Facebook Prophet](../capstone/stocks/Apple_Model_5_Prophet.ipynb).

#### Classification Data Analysis, Preprocessing, and Modeling:

-  Apple Exploratory Data Analysis [with the SEC Data](../capstone/stocks/Apple_EDA_wSEC.ipynb).
- Apple [Preparing the Data](../capstone/stocks/Apple_Model_Classification_1_Prep.ipynb) for Classification Modeling.
- Apple [Preprocessing the Data](../capstone/stocks/Apple_Model_Classification_2_Data_Preprocessing.ipynb) for Classification Modeling.
- Apple Modeling: [Random Forest Classification](../capstone/stocks/Apple_Model_Classification_3_Random_Forest.ipynb).

---------

### SEC:

The [SEC](../capstone/sec) directory, has notebooks scraping and analyzing Apple's SEC Filings.

- SEC [Scraper](../capstone/sec/Apple_SEC_Scraper.ipynb).
- SEC [Exploratory Data Analysis](../capstone/sec/Apple_SEC_EDA.ipynb).

------- 

## Exploratory Data Analysis





------- 

## Preprocessing Data

Since the stock data is sequential and dealing with time, the training and testing set have to be done manually. Reason being, the training data must be historical data since the main objective to predict the future price. 

------- 

## Optimal Model



------- 

## Conclusion




--------

## Credits

Special thanks to:

- Douglas Strodtman and Wesley Bosse for providing the guidance, assistance, and mentorship to complete the project. 
