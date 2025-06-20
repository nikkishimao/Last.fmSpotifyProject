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

<h2>Question 3: Is there any relationship between Last.fm and Spotify?</h2>

<p>In this part of the project, we first integrate Last.fm and Spotify data to compare track popularity. First, we authenticate with the Spotify API using client credentials and create an instance of the Spotify client (sp). We then define a function, fetch_spotify_track_details(), which searches for tracks on Spotify by name and artist, returning their popularity score and available markets. </p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/ba0125bb9dce13092d059b496038d8f70a51b065/images/1Question3.png" alt="image alt" width="500" />
</p>

<p>Next, we define the combine_with_spotify() function to merge Last.fm data with Spotify details. For each track in the Last.fm dataset, it fetches the corresponding popularity score from Spotify and appends it to the data. The resulting data is stored in a new DataFrame that includes Track Name, Artist, Playcount (from Last.fm), Listeners (from Last.fm), and Popularity (from Spotify). The merged dataset allows for direct comparison of track performance across the two platforms, providing valuable insights into how tracks' popularity on Spotify relates to their playcounts on Last.fm.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/ba0125bb9dce13092d059b496038d8f70a51b065/images/2Question3.png" alt="image alt" width="500" />
</p>

<p>In this step, we save the merged data containing Last.fm playcounts and Spotify popularity scores into a CSV file for further analysis. The data includes columns such as Track Name, Artist, Playcount (from Last.fm), Listeners (from Last.fm), and Popularity (from Spotify). After saving the data, the script prints the combined dataset, which contains detailed information about the top 50 tracks from Last.fm and their corresponding Spotify popularity scores. </p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/ba0125bb9dce13092d059b496038d8f70a51b065/images/3Question3.png" alt="image alt" width="500" />
</p>

<p>The output shows the Track Name, Artist, Playcount, Listeners, and Popularity for each of the 50 tracks. For example, the track "Squabble Up" by Kendrick Lamar has a playcount of 3,776,877 on Last.fm and a Spotify popularity score of 91. Similarly, "Good Luck, Babe!" by Chappell Roan has 33,935,151 plays on Last.fm and a popularity score of 93 on Spotify. This dataset enables a side-by-side comparison of how tracks perform on both platforms, offering valuable insights into their relative popularity. </p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/ba0125bb9dce13092d059b496038d8f70a51b065/images/4Question3.png" alt="image alt" width="500" />
</p>

<p>Then in the next step, we are ensuring that the Playcount, Popularity, and Listeners columns in the merged dataset are correctly formatted as integers for proper analysis. The data initially contains these columns as strings, which could interfere with any numeric operations or comparisons we want to perform. By using the astype(int) method, we convert each of these columns from strings to integers, allowing us to treat them as numeric values for further statistical analysis or visualizations. This ensures that when performing calculations, such as sorting or generating plots, the data will be interpreted correctly.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/0eef1fa953f549f4706d840dbed17e6b8c01d2f3/images/5Question3.png" alt="image alt" width="500" />
</p>

<p>Then we perform a linear regression to analyze the relationship between Spotify Popularity and Last.fm Playcount for the top tracks. The independent variable (X) is the Spotify Popularity, and the dependent variable (y) is the Last.fm Playcount. Before fitting the regression model, we add a constant term to the independent variable using sm.add_constant(X) to account for the intercept in the model. We then use Ordinary Least Squares (OLS) regression to fit the model, which estimates the coefficients that best explain the relationship between Spotify Popularity and Last.fm Playcount.</p>

<p>The regression results yield several key statistics:</p>

<ul>
  <li><strong>R-Squared (0.0041)</strong>: This is a very low value, indicating that only a small portion of the variability in Last.fm Playcounts can be explained by Spotify Popularity. In other words, there is a very weak relationship between these two variables.</li>
  <li><strong>Coefficients</strong>: The constant term is 30,389,950, and the coefficient for Popularity is -179,329. This suggests that for each increase in Spotify Popularity, the Last.fm Playcount decreases by approximately 179,329, although this result is not statistically significant.</li>
  <li><strong>P-Values</strong>: The p-values for both the constant (0.3994) and Popularity (0.6598) are much higher than the common significance threshold of 0.05, suggesting that neither of these coefficients are statistically significant. This implies that there is no strong evidence to suggest a meaningful relationship between Spotify Popularity and Last.fm Playcount.</li>
  <li><strong>F-Statistic P-value (0.6598)</strong>: The high p-value for the overall model further confirms that the model does not fit the data well and that the relationship between the variables is not statistically significant. </li>
</ul>

<p>In summary, the linear regression analysis shows that Spotify Popularity and Last.fm Playcount do not have a significant relationship, and the model does not explain much of the variance in the Playcount data. </p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/0eef1fa953f549f4706d840dbed17e6b8c01d2f3/images/6Question3.png" alt="image alt" width="500" />
</p>

<p>Next, we  normalized the Last.fm Playcounts to a 0-100 scale to allow for an easy comparison between the Spotify Popularity Scores and Last.fm Playcounts. This normalization step ensures that both metrics are on a similar scale, which is important for visual comparison. We first drop any rows with missing values in the "Popularity" or "Playcount" columns to avoid issues during analysis. Then, we create a new column in the comparison_data DataFrame called "Normalized Playcount" by dividing the Playcount values by the maximum Playcount value and multiplying by 100.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/0eef1fa953f549f4706d840dbed17e6b8c01d2f3/images/7Question3.png" alt="image alt" width="500" />
</p>

<p>Next, we generate a bar chart to visualize the comparison. The X-axis represents the track names, and for each track, two bars are shown side by side: one for the Normalized Playcount (in red) and one for the Spotify Popularity Score (in light green). The chart also includes annotations above the bars, displaying the actual values for Playcount (in millions) and Spotify Popularity for each track. The bar chart provides a clear visual comparison of how the Last.fm Playcounts and Spotify Popularity Scores compare across different songs, making it easier to observe trends and differences between the two metrics for the top tracks.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/0eef1fa953f549f4706d840dbed17e6b8c01d2f3/images/8Question3.png" alt="image alt" width="500" />
</p>

<p>Since the relationship is not super clear we also wanted to create a scatter plot to visually explore the potential relationship between Spotify Popularity and Last.fm Playcounts. This approach allows us to see if there is any correlation or trend between the two variables. In the scatter plot the X-axis represents the Spotify Popularity Scores (ranging from 0 to 100) and the Y-axis shows the Last.fm Playcounts normalized in millions (i.e., divided by 1,000,000). Each point on the plot represents a song, and the color of the points is set to green with some transparency (alpha=0.7) for better visibility. We also annotated each point with the track name along with its Spotify Popularity and Last.fm Playcount (in millions). This allows us to directly identify the song and its respective values on the plot. The grid is added to the background to make it easier to visually compare the values.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/0eef1fa953f549f4706d840dbed17e6b8c01d2f3/images/9Question3.png" alt="image alt" width="500" />
</p>

<p>The resulting scatter plot provides a more detailed look at the distribution of Playcount and Popularity scores. From the plot, you can visually see that there still isn’t a obvious linear  pattern between the two variables but some conclusions can still be drawn a little better than just the graph with the bars.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/0eef1fa953f549f4706d840dbed17e6b8c01d2f3/images/10Question3.png" alt="image alt" width="500" />
</p>

<h2>Further Exploration: Is there a relationship for a specific artist?</h2>
<p>To take this question a bit further we now wanted to explore if for a specific artist, there was a relationship. So first, we focused on fetching data for Bruno Mars' top tracks using the Last.fm API to investigate the relationship between Spotify Popularity and Last.fm Playcount for a specific artist. We began by defining the necessary parameters for the API request, specifying the artist's name and setting a limit to fetch the top 10 tracks. The request was wrapped in a try block to ensure that any potential errors would be handled gracefully. If the request was successful, the data was processed and the top 10 tracks were extracted from the JSON response. For each track, we printed the track name along with its corresponding Playcount—the number of times the track had been played on Last.fm.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/cb4df0c6d95be276e2a16d4e46f4719ee0bf808d/images/Explor1.png" alt="image alt" width="600" />
</p>

<p>The output displayed the following tracks for Bruno Mars along with their playcounts: "Locked Out of Heaven" (17,383,335 plays), "Just the Way You Are" (13,473,528 plays), "When I Was Your Man" (13,176,832 plays), "Grenade" (11,799,716 plays), "That's What I Like" (10,765,543 plays), "Treasure" (9,175,395 plays), "The Lazy Song" (6,639,384 plays), "Talking to the Moon" (9,744,384 plays), "Leave The Door Open" (11,509,838 plays), and "24K Magic" (7,233,120 plays). With this data in hand, we now had a set of Bruno Mars' most-played tracks on Last.fm, which could be further analyzed in comparison with their Spotify popularity scores to explore whether there is a correlation between the two platforms for this specific artist.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/cb4df0c6d95be276e2a16d4e46f4719ee0bf808d/images/Explor2.png" alt="image alt" width="400" />
</p>

<p>Next, we performed a search for Bruno Mars on Spotify using the Spotipy API. By querying the Spotify database with the artist's name, we retrieved key information about the artist, including their Spotify Artist ID, Spotify URL, and the genres associated with them. The API returned Bruno Mars as the first result, providing the following details:</p>

<ul>
  <li><strong>Artist name</strong>: Bruno Mars</li>
  <li><strong>Spotify Artist ID</strong>: 0du5cEVh5yTK9QJze8zA0C</li>
  <li><strong>Spotify URL</strong>: Bruno Mars on Spotify</li>
  <li><strong>Genres</strong>: Dance pop, Pop</li>
</ul>

<p>This information was printed out, confirming that we successfully fetched Bruno Mars' details from Spotify, which would be useful for any further analysis or comparisons with other data sources like Last.fm.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/cb4df0c6d95be276e2a16d4e46f4719ee0bf808d/images/Explor3.png" alt="image alt" width="500" />
</p>

<p>The next step in the analysis involves retrieving the top tracks for Bruno Mars using the Spotify API. First, the artist's unique Spotify ID is defined, and the code uses this ID to query the API for the top tracks. Each track's name and popularity score are extracted and stored in a list. This data is then converted into a pandas DataFrame, which allows for easier manipulation and sorting. The tracks are sorted by their popularity score in descending order to show the most popular tracks at the top.</p>
<p>The output reveals that "Die With A Smile" has the highest popularity score of 99, followed by "Locked Out of Heaven" and "That's What I Like", both of which have a popularity score of 89. Other popular tracks such as "When I Was Your Man" (popularity 86) and "Just the Way You Are" (popularity 85) follow. The code effectively organizes the top tracks from Bruno Mars, giving a clear view of his most popular songs according to Spotify's ranking.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/cb4df0c6d95be276e2a16d4e46f4719ee0bf808d/images/Explor4.png" alt="image alt" width="500" />
</p>

<p>Then the top tracks of Bruno Mars are fetched from the Last.fm API using a set of predefined parameters. The code makes a request to Last.fm, specifying the artist and limiting the result to 50 tracks. The relevant data, specifically the track name and playcount, is extracted from the API response, with playcounts being converted to integers for proper numerical analysis. This data is then stored in a pandas DataFrame for further manipulation. The code proceeds to merge the Spotify data (which contains track names and popularity scores) with the Last.fm data based on matching track names. This merging process ensures that only the common tracks between the two sources are kept. The resulting DataFrame contains the Track Name, Popularity (from Spotify), and Playcount (from Last.fm). Finally, this merged dataset is saved to a CSV file for further use.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/cb4df0c6d95be276e2a16d4e46f4719ee0bf808d/images/Explor5.png" alt="image alt" width="600" />
</p>

<p>The output reveals the top tracks for Bruno Mars, with "That's What I Like" leading the list in terms of Spotify popularity (89) and a playcount of over 10 million. Tracks like "When I Was Your Man" and "Just the Way You Are" also show high popularity and significant playcounts, reflecting their success across both platforms. The DataFrame is ready for further analysis or visualization.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/cb4df0c6d95be276e2a16d4e46f4719ee0bf808d/images/Explor6.png" alt="image alt" width="400" />
</p>

<p>In this step, a linear regression analysis is performed to explore the relationship between Spotify Popularity and Last.fm Playcount for Bruno Mars' top tracks. The regression model is set up by defining Popularity as the independent variable (X) and Playcount as the dependent variable (y). A constant is added to the independent variable to account for the intercept in the regression model.</p>
<p>Once the regression model is fitted, the results are extracted to assess the strength and significance of the relationship between the two variables. The R-squared value of 0.5736 indicates that about 57% of the variation in the playcounts can be explained by the Spotify popularity scores. The coefficients suggest that for each one-unit increase in popularity, the playcount increases by approximately 314,654 plays. The P-value for Popularity is 0.0486, which is just below the common threshold of 0.05, indicating that the relationship between Spotify Popularity and Last.fm Playcount is statistically significant. On the other hand, the P-value for the constant term is 0.1868, which is not significant, suggesting that the intercept may not be an important factor in this model. These results imply a moderate but significant positive relationship between the two variables.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/cb4df0c6d95be276e2a16d4e46f4719ee0bf808d/images/Explor7.png" alt="image alt" width="500" />
</p>

<p>Similarly to the visualization created for top 50, we further analyzed the comparison between Spotify Popularity and Last.fm Playcount for Bruno Mars' top tracks by visualizing the data in a bar chart. First, the data was sorted by Playcount in descending order to highlight the most popular tracks based on their playcounts. Then, the Playcount values were normalized to a scale of 0-100 to make a fair comparison alongside the Spotify Popularity scores, as the two metrics have different units and ranges.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/cb4df0c6d95be276e2a16d4e46f4719ee0bf808d/images/Explor8.png" alt="image alt" width="500" />
</p>

<p>In the bar chart, each track's normalized playcount and Spotify popularity are represented by adjacent bars. The red bars represent Last.fm Playcounts, normalized to a 0-100 scale, while the light green bars show the Spotify Popularity scores. Values are annotated above each bar to provide actual numbers: for the playcounts, the values are displayed in millions, and for popularity, the raw score is shown. This side-by-side comparison allows a clear visual understanding of the relationship between the two variables for each track. For tracks like "Just the Way You Are," "When I Was Your Man," and "Grenade," the Last.fm playcounts were higher than the Spotify popularity scores, suggesting that these tracks had greater cumulative listener engagement on Last.fm compared to Spotify. On the other hand, tracks such as "That's What I Like," "Talking to the Moon," "Marry You," and "It Will Rain" showed higher Spotify popularity scores than Last.fm playcounts, indicating that these tracks were more popular or engaging on Spotify, likely due to its different user base and listening behaviors.The chart visually represented this divergence, with Last.fm playcounts shown in red and Spotify popularity in green, revealing that while some tracks had more playtime on Last.fm, others performed better in terms of real-time popularity on Spotify. This analysis highlights the differences in how each platform measures success and how audience behavior varies across them.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/cb4df0c6d95be276e2a16d4e46f4719ee0bf808d/images/Explor9.png" alt="image alt" width="500" />
</p>

<p>Next, in order to better see the relationship again, a scatter plot was created to visually explore the relationship between Spotify Popularity and Last.fm Playcounts for Bruno Mars' top tracks. The scatter plot allows for a more granular view of how each track's Spotify popularity score (ranging from 0-100) relates to its Last.fm playcount (displayed in millions). Each point on the plot represents a track, with the x-axis showing its Spotify popularity and the y-axis displaying the Last.fm playcount. The individual points are color-coded in green, and the actual values for popularity and playcount are annotated next to each track to provide further context. This plot enables the identification of potential patterns or outliers, illustrating whether more popular tracks on Spotify generally have higher playcounts on Last.fm, or if there are notable exceptions.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/cb4df0c6d95be276e2a16d4e46f4719ee0bf808d/images/Explor10.png" alt="image alt" width="500" />
</p>

<p>Overall, the scatter plot offers an effective tool for visually analyzing how Spotify popularity correlates with Last.fm play counts. There is a clear relationship between the two, which further supports the linear regression that was done earlier and its resulting p-value.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/cb4df0c6d95be276e2a16d4e46f4719ee0bf808d/images/Explor11.png" alt="image alt" width="500" />
</p>

<h2>Extra Tests:</h2>
<p>So for our first extra test we decided to do an Ordinary Least Squares (OLS) regression was performed to analyze the relationship between Listeners and Playcount. The independent variable (X) was the number of Listeners, while the dependent variable (y) was the Playcount. The results from the regression analysis indicated a strong and statistically significant relationship between these two variables.</p>
<p>The R-Squared value of 0.8244 suggests that about 82.44% of the variance in Playcount can be explained by the number of Listeners, indicating a good fit of the model. The coefficient for Listeners was 21.56, meaning that for each additional listener, the Playcount increases by approximately 21.56 units. The intercept (constant) was estimated at -6.12 million, representing the predicted Playcount when there are zero listeners, though this is a theoretical value and not practically meaningful. Both the p-values for the intercept (0.0002997) and the Listeners variable (9.29e-20) were extremely small, indicating that these variables are statistically significant in predicting Playcount. The very low p-value for Listeners suggests a highly significant relationship, while the low p-value for the intercept further supports the model's validity. Additionally, the F-statistic was high, suggesting that the regression model as a whole is statistically significant.</p>
<p>Overall, the results demonstrate that the number of Listeners is a strong and significant predictor of the number of Playcounts. The high R-Squared value and the very low p-values confirm that tracks with more listeners generally have higher playcounts, emphasizing the importance of Listeners in explaining the variation in Playcount.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/153baab277c4b146bb612d124ed8d6bc4e546035/images/Extra1.png" alt="image alt" width="500" />
</p>

<p>Next, we decide to create a scatter plot to show the relationship between play count and listeners. Both Playcount and Listeners were converted to millions for better readability and comparison. The plot displays Playcount on the x-axis and Listeners on the y-axis, with each point representing a track.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/153baab277c4b146bb612d124ed8d6bc4e546035/images/Extra2.png" alt="image alt" width="500" />
</p>

<p>The plot reveals a noticeable positive relationship between Playcount and Listeners, meaning that tracks with more listeners generally have higher playcounts. The data suggests that as the number of listeners increases, so does the number of plays, which supports the findings from the regression analysis. This pattern indicates a strong dependency between these two variables. However, the plot also highlights a few outliers, particularly around certain holiday or seasonal tracks, such as Christmas songs. So next we will VIF to check.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/153baab277c4b146bb612d124ed8d6bc4e546035/images/Extra3.png" alt="image alt" width="500" />
</p>

<p>Now, the Variance Inflation Factor (VIF) was calculated to assess multicollinearity between Playcount and Listeners. VIF measures how much the variance of a regression coefficient is inflated due to correlations with other variables. High VIF values indicate potential issues with multicollinearity The results showed VIF values of const (Intercept): 5.76 Playcount: 5.69, and Listeners: 5.69.  These values suggest moderate multicollinearity, but since they are below the threshold of 10, the correlation between Playcount and Listeners is not severe. Still, it indicates that their relationship should be considered when interpreting regression results.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/153baab277c4b146bb612d124ed8d6bc4e546035/images/Extra4.png" alt="image alt" width="500" />
</p>

<p>Next, created a new variable, Playcount per Listener by dividing Playcount by Listeners to reduce the impact of multicollinearity. This transformed variable was then used for a regression model to analyze its relationship with Popularity. The results from the regression model showed that the R-Squared value was 0.0053, indicating a very weak explanatory power of the model. The coefficient for Playcount_per_Listener was 0.0487, but the corresponding p-value of 0.6157 suggests that the relationship between Playcount per Listener and Popularity is not statistically significant. This indicates that Playcount per Listener does not have a strong predictive relationship with Popularity in this case.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/153baab277c4b146bb612d124ed8d6bc4e546035/images/Extra5.png" alt="image alt" width="500" />
</p>

<p>In the final step, a scatter plot was created to visualize the relationship between the new feature, Playcount per Listener, and Popularity. The plot confirmed that the influence of Playcount per Listener on Popularity is minimal, reinforcing the regression results. Despite the creation of this new feature, the scatter plot demonstrated that there is still a weak relationship between these two variables, as evidenced by the lack of a clear trend or correlation. This suggests that Playcount per Listener does not significantly impact Popularity in this dataset.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/Last.fmSpotifyProject/blob/153baab277c4b146bb612d124ed8d6bc4e546035/images/Extra6.png" alt="image alt" width="500" />
</p>
