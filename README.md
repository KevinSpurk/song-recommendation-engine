# Case | Song recommendation

This notebook creates a pipeline to get song recommendation based on songs in the Billboard Hot 100 list. A user can run a search for a song title and - if it is present in the Hot 100 list - is recommended a similar song based on a model of song clustering, or a song with that title is added to the cluster model.

### 1. Billboard Hot 100 data
Web scraping The Billboars Hot 100 list and creating a user search that enables the user to check if a song is in the Hot 100.

### 2. Spotify data
Using Spotify APIs to retrieve song info and audio features for tracks in the Hot 100 list. The info is gathered for the song selected by the user as well as for all songs in the list to train the model in the next step.

### 3. Clustering
Building a KMeans clustering model based on the gathered audio features and parameter tuning for a better model performance.

### 4. Song recommendation
Applying the user search of the Hot 100 list to the clustered data. If the song title provided by the user is matched with a song in the Hot 100 list, the user receives a recommendation of a song from the same cluster. If the song is not matched, The details and audio features for a track with that title are fetched from Spotify. The track is assinged to a cluster and gets added the song collection in the clustered data.
