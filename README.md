# Notebook #2: K Nearest Neighbors and Normalization

## The Data 
For this notebook, you will load a new data set dealing with data from the top songs on Spotify in 2022. 🎵

*Note: this data may be a few weeks old*

The data is originally from here: https://www.kaggle.com/datasets/sveta151/spotify-top-chart-songs-2022. Note that the data is very detailed regarding the metrics of the music. Descriptions of each of the columns are available at the above link. Of particular note are the following:
- **artist_names**: Artist name of the song
- **track_name**: Track name of the song
- **peak_rank (target variable)**: Peak rank in the charts
- **danceability**: Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable.
- **energy**: Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy.
- **key**: The key the track is in. Integers map to pitches using standard Pitch Class notation. E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on. If no key was detected, the value is -1.
- **loudnes**: The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typically range between -60 and 0 db
- **mode**: Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0.
- **duration_ms**: The duration of the track in milliseconds.

## What you need to do: :exclamation:
You're going to write a function that can make k-Nearest-Neighbor predictions for the peak rank ("peak_rank" column) based on a subset of the data:  **between three and five predictor columns**.

Notebook #2 consists of the following exercises :muscle:. 

<b> Make sure you do the following </b>: [ 1 point each ]
1. Work with the right subset (both rows and columns): You're not going to work with the whole data set, just the 3-5 features that of your choice. To start, make this subset of the original data. Also, make sure your subset contains only countries with the "Status" feature as **Developing**. To start, make this subset of the original data. *hint: your initial subset should have between 2,000 and 2,500 rows.*
2. Check for null values in the target and predictor columns. If you have a null target value, you will need to throw that example out. Replace each of the null values within your predictors with the average of the column. *hint: Useful functions here are `isna()`, `any()`, `fillna()`, `value_counts()` and `dropna()`.
After you have eliminated null values, use `.isna().any()` to verify that your fields no longer contain any null values (all of the values should be False). 
3. Write up a k-nearest-neighbors function like the one you made for the iris data set in class. It should be able to make life expectancy predictions for countries based on the features you have decided to incorporate. You should also be able to specify what you want to use as k. You will need to incorporate the predictor features that you have chosen to be a part of your subset in your knn function. Pay special attention to whether this problem is a classification or a regression, and how the answer to that question may change the output of your model. 
4. Demonstrate that your function works by making up some new values for hypothetical countries and using your function to display the predicted life expectancy for that country.
5. Make a copy of the data and normalize the training data using Z-score. Predict the life expectancy of a particular country using your k-nearest-neighbors function with both the normalized and non-normalized training data. Compare your results. Use a markup cell to describe and explain the differences in a few sentences.

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
