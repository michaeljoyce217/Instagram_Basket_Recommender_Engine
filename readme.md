## Recommender engine for Instacart

This project is a simple cosine similarity based recommender engine for Instacart, a web-based grocery delivery service in the United States. I may expand it at a later date but my intention here was to prepare for data science job interviews that require building a simple recommender engine.


## Overview

Instacart released anonymized customer data as part of a Kaggle competition entitled Instacart Market Basket Analysis. The goal of the competition is to predict which previously purchased products will be in a user's next order. Cosine similarity based on a user's previous purchases is arguably the simplest and crudest recommender engine but is a good starting point nonetheless.


## Datasets

All data was provided by Instacart. The included datasets that were provided were:

* aisles.csv- aisle information

* departments.csv- department information

* order_products_prior.csv- previous order contents for all customers

* order_products_train.csv- the order training set for the model

* orders.csv- states which set (prior, train, test) an order belongs

* products.csv- list of products sold by Instacart

## Exploratory data analysis

Constructing a cosine similarity based recommender engine does not require a great deal of exploratory data analysis. However, this project was undertaken with the goal of expanding my skill set.

The usual EDA was performed, such as checking for missing data, merging dataframes, etc. In addition, I experimented with apriori and associaton_rules from the mlextend package, along with the metrics they give, as well as sparse from the scipy package, mainly using the aisle information. I had hoped to perform similar exploration on the product information, but this would likely require an EC2 instance on AWS. If I go back to build a better recommender engine, this exploration will likely be useful.

## Simple recommender engine

The recommender system uses cosine similarity to compare each user and find similarities between each pair of users, as well as similarity between product reorders, and then makes a recommendation based on the user ID. A function is included that allows the user ID to be input and passed through the model with the output consisting of the top items for that user.


## Toolkit

* Jupyter Notebook - integrated development environment for python; used to explore data and test code
* Pandas - provides high-performance, easy-to-use data structures and data analysis tools for Python; used for basic data manipulation & some file reading
* NumPy - the fundamental package for scientific computing with Python; used for math functionality
* Scipy- python package based on numpy for higher math functions
* Sci-kit learn - data modeling library




<br>
