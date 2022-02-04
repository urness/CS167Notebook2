# Notebook #2: K Nearest Neighbors and Normalization

## The Data
For this notebook, you will load a new data set dealing with public health and life expectancy :hospital:.

The data is originally from here: https://www.kaggle.com/kumarajarshi/life-expectancy-who

This data has a lot of columns, and Pandas will abbreviate the output by default. To show all of the columns, you can change this property using the set_option() function as follows:

`pd.set_option('display.max_columns', 100)` <br>

## What you need to do: :exclamation:
You're going to write a function that can make k-Nearest-Neighbor predictions for the life expectancy ("Life expectancy" column) based on a subset of the data:  **between three and five predictor columns**, and only **Developing** ("Status" column) countries.

Notebook #2 consists of the following exercises :muscle:. 

<b> Make sure you do the following </b>: [ 1 point each ]
1. Work with the right subset (both rows and columns, re-read the first paragraph under 'what you need to do'): You're not going to work with the whole data set, just the 3-5 features that of your choice. To start, make this subset of the original data. Also, make sure your subset contains only countries with the "Status" feature as **Developing**. To start, make this subset of the original data.
2. Check for null values in the target and predictor columns. If you have a null target value, you will need to throw that example out. If you have a null predictor value, you can either fill them in with something (like the mean/median) or you can drop those rows from the data set. Useful functions here are `isna()`, `any()`, `fillna()`, `value_counts()` and `dropna()`. Describe in a markup cell what you decided to do with the null data and why.
3. Write up a k-nearest-neighbors function like the one you made for the iris data set in class. It should be able to make life expectancy predictions for countries based on the features you have decided to incorporate. You should also be able to specify what you want to use as k.
4. Demonstrate that your function works by making up some new values for hypothetical countries and using your function to display the predicted life expectancy for that country.
5. Make a copy of the data and normalize the training data using Z-score-- copy() will be useful here. Predict the life expectancy of a particular country using your k-nearest-neighbors function with both the normalized and non-normalized training data. Compare your results. Use a markup cell to describe and explain the differences in a few sentences.

To submit your work, copy the link to your github repository, and submit the link to the Blackboard assignment (please help me save a few clicks and make sure your link it clickable). 


## :white_check_mark: Grading: 
I will update the following rubric with your grade after you have completed the assignment.
### Rubric:
| Exercise #  | Points Awarded (out of 1)  | Notes |
| --------- | -------------------: | --------- |
| 1: subset      |        |    |
| 2: null        |        |    | 
| 3: knn         |        |    |
| 4: demo        |        |    | 
| 5: normalize   |        |    |
| <b>Total       |      /5  | </b>   |
