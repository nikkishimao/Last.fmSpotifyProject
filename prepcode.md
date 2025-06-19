<h1>Preparation Code</h1>

<h2>Fetching Data from Last.fm</h2>
</p>We fetch data from Last.fm by first connecting to the Last.fm API using a unique API key in order to fetch the top 10 tracks using the chart.getTopTracks method. The request parameters specify the method, api_key, format, limit, and page, with a limit of 10 tracks per page. The API request is made using the requests.get() function, and the response is parsed into JSON format. From the response, the relevant information for each track is extracted, including the track name, artist, playcount, listeners, and a URL to the track on Last.fm. The code then iterates through the fetched tracks, printing each track's name, artist, playcount, listeners, and URL. If there is an issue with the API request, an error message is displayed. The output of the code provides a list of the top 10 tracks on Last.fm, including artists like Kendrick Lamar, Billie Eilish, and Tyler, the Creator, along with detailed information such as the playcount and number of listeners for each track.<p>

<p align="center">
  <img src="https://raw.githubusercontent.com/nikkishimao/Last.fmSpotifyProject/a5e8a8d32dd4b58d052c1e04e3a73996e0988fc2/images/StartCode.png" alt="image alt" width="500" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/nikkishimao/Last.fmSpotifyProject/a5e8a8d32dd4b58d052c1e04e3a73996e0988fc2/images/TopLastfmTracks.png" alt="image alt" width="500" />
</p>

<p>For example, one of the top tracks is "Squabble Up" by Kendrick Lamar, with 3,776,877 plays and 630,350 listeners, along with a direct link to the track on Last.fm. Other tracks in the list include "Good Luck, Babe!" by Chappell Roan, "BIRDS OF A FEATHER" by Billie Eilish, and "See You Again" by Tyler, the Creator. The output showcases the diversity of music on Last.fm and provides a clear picture of the popularity and reach of these tracks within the Last.fm community.</p>

<h2>Data Preparation: Top 50 Tracks</h2>
</p>To explore which music genres have the highest total play counts among the top 50 tracks globally, we first retrieved the top 50 tracks from Last.fm using the chart.getTopTracks API method. This API provided essential information for each track, including its name, artist, play count, and listener count. However, the genre of each track wasn't directly available from this data, so we used another API call, artist.getInfo, to fetch genre information for each artist. This additional data helped us assign a genre to each track based on the primary genre associated with the artist. <p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/770f816c571d4ad9b87f7e848b766640dd55db38/images/1Top50.png" alt="image alt" width="600" />
</p>
<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/770f816c571d4ad9b87f7e848b766640dd55db38/images/2Top50.png" alt="image alt" width="600" />
</p>
