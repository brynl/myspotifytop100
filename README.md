# myspotifytop100

An analysis of my Spotify top 100 songs and Spotify's top 100 from 2016 using R. 
The data was analyzed using PCA and Kmeans clustering and visualized using ggplot2 
and plotly. 

## Motivation and Research Question

This project was inspired by [this project](https://medium.com/latinxinai/discovering-descriptive-music-genres-using-k-means-clustering-d19bdea5e443) by Victor Ramirez. 

Research Question(s): How can my top 100 most listened to songs be partitioned into different clusters? 
                      How does my top 100 most listened to compare to the top 100 most listend to on Spotify?


## Retrieving Data 
My personal dataset was obtained using the spotifyR package and 
the Spotify API. 

A top 100 songs on Spotify overall was used to 
compare my music taste with Spotify's total listeners. The data 
was obtained from kaggle. 

## Spotify Features Data

Spotify provides numerous [features](https://developer.spotify.com/documentation/web-api/reference/tracks/get-audio-features/) that could be analyzed for each track. 

I decided to use the following features: 

**acousticness**: A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.

**danceability:**
**energy:**
**instrumentalness:**
**liveness:**
**speechiness:**
**valence:**
