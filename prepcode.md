<h1>Preparation Code</h1>

<h2>Fetching Data from Last.fm</h2>
</p>We fetch data from Last.fm by first connecting to the Last.fm API using a unique API key in order to fetch the top 10 tracks using the chart.getTopTracks method. The request parameters specify the method, api_key, format, limit, and page, with a limit of 10 tracks per page. The API request is made using the requests.get() function, and the response is parsed into JSON format. From the response, the relevant information for each track is extracted, including the track name, artist, playcount, listeners, and a URL to the track on Last.fm. The code then iterates through the fetched tracks, printing each track's name, artist, playcount, listeners, and URL. If there is an issue with the API request, an error message is displayed. The output of the code provides a list of the top 10 tracks on Last.fm, including artists like Kendrick Lamar, Billie Eilish, and Tyler, the Creator, along with detailed information such as the playcount and number of listeners for each track.<p>



<p>For example, one of the top tracks is "Squabble Up" by Kendrick Lamar, with 3,776,877 plays and 630,350 listeners, along with a direct link to the track on Last.fm. Other tracks in the list include "Good Luck, Babe!" by Chappell Roan, "BIRDS OF A FEATHER" by Billie Eilish, and "See You Again" by Tyler, the Creator. The output showcases the diversity of music on Last.fm and provides a clear picture of the popularity and reach of these tracks within the Last.fm community.</p>
