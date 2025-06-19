<h1>Results</h1>

<h2>Question 1: Which music genres have the highest total play counts among the top 50 tracks globally? </h2>
<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/073d9ab6109c98c3de43c75ae9c83e025d7ff28c/images/Question1.png" alt="image alt" width="600" />
</p>
<p>Once the genre data was integrated into the dataset, we compiled the information into a Pandas DataFrame. The next step involved aggregating the play counts by genre to understand the relative popularity of different music styles. We used the groupby function to sum the play counts for each genre, followed by sorting the genres in descending order to identify which ones had the highest total play counts among the top 50 tracks. 

The resulting dataset revealed that Pop was by far the most-played genre, with a total of 310,976,942 play counts, significantly surpassing other genres. Hip-Hop followed as the second most-played genre, with 140,375,820 plays, while R&B ranked third with 108,800,524 plays. Other prominent genres included Indie Rock and Indie Pop, with play counts of 38,637,392 and 32,627,596, respectively. Interestingly, genres like 80s and Folk, while less popular, still contributed notable play counts of 11,133,298 and 9,353,785, respectively, indicating a continued appreciation for older and niche music styles. The genre seen live, which might refer to live performances or specific concerts, appeared in the dataset with a total play count of 41,925,406, suggesting the popularity of live music experiences. 

In summary, the analysis of the top 50 tracks globally revealed that Pop dominated global music consumption, followed by strong showings from Hip-Hop and R&B, while indie and niche genres also held significant but smaller portions of the global listening landscape. This exploration of genre play counts provides valuable insight into current musical trends and listener preferences across the world. </p>

<h2>Question 2: Who are the most dominant artists in Last.fm’s Top 50 global tracks, and how do these artists vary across different music genres? </h2>

<p>To explore the most dominant artists in Last.fm’s Top 50 global tracks and how they vary across different music genres, we first analyzed the number of tracks each artist had in the top 50. This was done by grouping the dataset by artist and counting the occurrences of each artist in the list. Our results revealed that Kendrick Lamar emerged as the most dominant artist, with a total of 13 tracks in the top 50, followed by Tyler, the Creator with 9 tracks and Sabrina Carpenter with 5 tracks. Other artists like Charli XCX, Billie Eilish, and Chappell Roan had between 2 and 4 tracks each, while several artists like Arctic Monkeys, SZA, and Wham! had a single track each in the top 50. This analysis highlighted the dominance of certain artists in global music, with Kendrick Lamar leading the charge in the overall ranking.</p>
<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/49c8702144f201947e2edc7322da8f3ec862383a/images/1Question2.png" alt="image alt" width="500" />
</p>

<p>In the second part of our analysis, we sought to understand how these dominant artists varied across different music genres. By grouping the data by genre and identifying the artist with the most tracks in each genre, we were able to determine the top artist per genre. The results revealed interesting insights into the relationship between artists and the genres they dominate. Kendrick Lamar was the dominant artist in Hip-Hop, while Wham! led the 80s genre, showcasing the enduring popularity of 80s music. In the Pop genre, Sabrina Carpenter stood out as the most played artist, reflecting her rising prominence in contemporary pop music. The Neighbourhood and TV Girl emerged as the top artists in Indie and Indie Pop, respectively, while Arctic Monkeys dominated Indie Rock. Frank Ocean was the most prominent artist in the R&B genre, illustrating his widespread influence in the alternative R&B scene. Interestingly, artists like Gigi Perez and Gracie Abrams topped the Folk and Seen Live genres, respectively, highlighting the diversity of global music preferences and the continued appeal of niche genres and live music.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/49c8702144f201947e2edc7322da8f3ec862383a/images/2Question2.png" alt="image alt" width="500" />
</p>

<p>In summary, our analysis of the top 50 tracks on Last.fm revealed that certain artists, like Kendrick Lamar, dominate multiple genres globally, while others, like Wham!, Sabrina Carpenter, and Frank Ocean, lead in specific genres like 80s, Pop, and R&B. The diversity of top artists across genres such as Indie, Hip-Hop, Folk, and Seen Live also highlights the broad range of musical tastes and trends that resonate with listeners worldwide. These findings underscore the complexity and richness of the global music landscape, where different genres and artists continue to shape listener preferences. </p>
