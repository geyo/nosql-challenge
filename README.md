# Use UK Food Standards Agency Data To Determine Magazine Article Topics

By Grace Yoo

**Programming Languages, Libraries, & Tools Used:** NoSQL, PyMongo, Jupyter Notebook

## Purpose

The purpose of this project is to evaluate the UK Food Standards Agency data to help journalists and food critics decide where to focus future articles for the fake food magazine, _Eat Safe, Love_. 

## Process

### ETL Data Into PyMongo

Before we can begin analysis, we must convert the data stored in the <code> establishments.json</code> file and store in a PyMongo database. We do that an assign this collection to a variable. 

Additionally, part of the instructions asked us to update the database with an exciting new halal restaurant that just opened in Greenwich. We do this by creating a new dictionary for said restaurant and inserting the restaurant into the collection:

<code>establishments.insert_one(greenwich_halal)</code>

We make various data corrections, such as updating the numerical data type, deleting redundant entries, and updating specific metadata. 

To see the code, access the [Preprocessing Jupyter Notebook](https://github.com/geyo/nosql-challenge/blob/main/NoSQL_setup_starter.ipynb).

### Exploratory Analysis

Next we conduct exploratory analysis to answer the following questions that the magazine editors want answered: 

1. Which establishments have a hygiene score equal to 20?

2. Which establishments in London have a RatingValue greater than or equal to 4?

3. What are the top 5 establishments with a RatingValue rating value of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

4. How many establishments in each Local Authority area have a hygiene score of 0?

To view how we arrived at the answers, access the [Exploratory Analysis Jupyter Notebook](https://github.com/geyo/nosql-challenge/blob/main/NoSQL_setup_starter.ipynb). 
