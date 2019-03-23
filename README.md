# myspotifytop100

An analysis of my Spotify top 100 songs and Spotify's top 100 from 2016 using R. 
The data was analyzed using PCA and Kmeans clustering and visualized using ggplot2 
and plotly. 

## Motivation and Research Question

This was inspired by [this project](https://medium.com/latinxinai/discovering-descriptive-music-genres-using-k-means-clustering-d19bdea5e443) by Victor Ramirez. 

Research Question(s): How can my top 100 most listened to songs be partitioned into different clusters? 
                      How does my top 100 most listened to compare to the top 100 most listend to on Spotify?


## Retrieving Data 
My personal dataset was obtained using the spotifyR package and 
the Spotify API. 

A top 100 songs on Spotify overall was used to 
compare my music taste with Spotify's total listeners. The data 
was obtained from [kaggle](https://www.kaggle.com/nadintamer/top-tracks-of-2017). 

## Spotify Features Data

Spotify provides numerous [features](https://developer.spotify.com/documentation/web-api/reference/tracks/get-audio-features/) that could be analyzed for each track. 

I decided to use the following features: 

**acousticness**: A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.

**danceability:** Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable.

**energy:** Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy.

**instrumentalness:** Predicts whether a track contains no vocals. “Ooh” and “aah” sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly “vocal”. The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content.

**liveness:** Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live.

**speechiness:** Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value.

**valence:** A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).

## Data Cleaning and Preparation

Since all the data was on a scale from 0.0 to 1.0, no further scaling was necessary to prepare data for machine learning algorithms. 

To clean data, I simply removed all columns that were not the song title, song uri, band name, and the pertinent features. 
![Alt text](https://github.com/brynl/myspotifytop100/blob/master/pics/songs_df.png)


## Principal Compenents Analysis 
![Alt text](https://github.com/brynl/myspotifytop100/blob/master/pics/pca_1.png)

### Choosing Number of Clusters 
![Alt text](https://github.com/brynl/myspotifytop100/blob/master/pics/wss.png)
![Alt text](https://github.com/brynl/myspotifytop100/blob/master/pics/sil.png)
## Kmeans Clustering
![Alt text](https://github.com/brynl/myspotifytop100/blob/master/pics/mykm.png)
![Alt text](https://github.com/brynl/myspotifytop100/blob/master/pics/plotly.png)
![Alt text](https://github.com/brynl/myspotifytop100/blob/master/pics/myauto.png)
![Alt text](https://github.com/brynl/myspotifytop100/blob/master/pics/spotifydf.png)

## Conclusion

My top listened to music is more diverse and much less "danceable" than Spotify's top listend to. 

##### Strengths
* Can visualize “true” styles of music, rather than labeled genres 
* Understanding diversity of each individual’s taste in music
##### Weaknesses
* Randomness characteristic of K-Means
* Different numbers of clusters for different features/datasets
* Difficult to interpret what each cluster represents
* Inclusion of Hot 100, limited sample size
##### Potential Extensions
* Hierarchical Clustering of music
* Decision Trees
* Recommender Systems
* Changes in taste over time
* Predicting an individual’s musical taste



