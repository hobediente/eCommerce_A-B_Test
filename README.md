# eCommerce A/B Testing Project

Run an A/B test to determine if there is a significant difference in purchases between shoppers who remove items from their cart and shoppers who do not remove items from their cart.

As the online shopping community continues to grow it becomes increasingly important for marketers to understand consumer behavior in the online environment.

People behave differently in different environments. Unlike when shoppers have carts the grociery store, adding an item to an online shopping cart never nesscitiates the shopper remove items they no longer wish to purchase, or reach the checkout line at all. As the online shopping community continues to grow it becomes increasingly important for marketers to understand consumer behavior in the online environment. 

Traditionally songs are grouped together with other songs on the basis of genre. While this method of grouping is useful for identifying different styles, there may be other valuable ways to group songs together. The aim of this study is to apply clustering algorithms to an assorment of songs across generes and explore cluster centers to determine if the the algorithms grouped songs together on the basis of genre, or in another way that is or is not of value. 
 
<img src="Images/Spotify Logo.jpg"></img>

# DATA:

The data for this project is sourced from Kaggle
- Each playlist is created by Spotify, features the top 100 tracks for that genre, and is updated weekly

1) Top 100 Pop Tracks on Spotify
2) Top 100 Alternative Tracks on Spotify
3) Top 100 Rock Tracks on Spotify
4) Top 100 Country Tracks on Spotify
5) Top 100 Hip Hop Tracks on Spotify
6) Top 100 Indie Tracks on Spotify
7) Top 100 Electronic Tracks on Spotify

# DATA ANALYSIS:

# 1. Data Collection:
In this step I collect and concat all playlists

# 2. Exploratory Analysis:
In this step the relationships between each genre playlist amd the song metrics provided by Spotify.

# 3. Clustering:
In this step I run clustering algorithms on the unique dataset I put together to see if songs are clustered along genre lines or clustered in novel way. 

# Model Results :
- KMeans is the best preforming model 
- With K=4 , KMEans achieved a silhoutte score of .1935
- Visual comparison

<img src="Images/clustering_by_genre.png" width="650" height="500"></img>

<img src="Images/clustering_by_KMeans.png" width="650" height="500"></img>

### Conclusion: Genres do not appear to have distinct clusters, so we can assume each of the KMeans clusters contain songs from multiple genres.

- Numeric comparison

<img src="Images/cluster_centers.png"></img>

    * KMeans cluster 0: High energy, high danceability, high valence
    * KMeans cluster 1: High energy, high danceability, low valence
    * KMeans cluster 2: High instrumentalness
    * KMeans cluster 3: Low liveness, low energy, high danceability
   
### Conclusion: Some clusters closely represent genres i.e. rock and cluster 0, while others do not seem to represent any one particular genre but songs with similar metrics within them.

# Analysis Takeaways :
- The KMeans algorithm did not cluster along genre lines
- Instead it grouped songs of similar moods across genres, which can be valuable for creating genre-diverse playlists for occasions that require consistent energy
   * Runnning playlists
   * Party playlists
   
# Limitations :
- Small dataset
  * Some clustering algorithms can be heavily influenced by outliers. So if I had more data I would preform further cleaning       of outliers.
