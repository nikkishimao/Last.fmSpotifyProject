<h1>Cross Trends: A Last.fm and Spotify Analysis</h1>

<h2>Description</h2>
</p>Together with Leonardo Pena Jarmillo and Wan-Hsin Hu, we developed this project to explore the relationship between two leading music platforms, Last.fm and Spotify. We explored how these platforms correlate and what they reveal about listener behavior. It focuses on three core questions:<p>

<ul>
  <li><strong>Genre Popularity Analysis</strong>: By aggregating play counts from Last.fm, we identify the most played genres globally and their respective audience engagement levels. This helps uncover genre trends and preferences across listeners.</li>
  <li><strong>Artist Dominance Within Genres</strong>: Using both Last.fm and Spotify data, we determine which artists dominate specific genres in terms of top track counts and popularity. This highlights key contributors to genre popularity.</li>
  <li><strong>Cross-Platform Metric Relationship</strong>: We analyze the correlation between Spotify's popularity scores and Last.fm's play counts. Through regression analysis and visualizations, we explore whether a track’s Spotify popularity reflects its listener engagement on Last.fm.</li>
</ul>

<p>By combining data from Last.fm's API for global play counts and Spotify's API for track popularity and availability, we create a unified dataset. This allows for comprehensive visualizations, normalization for cross-platform comparisons, and statistical evaluations. The project offers insights into genre trends, artist impact, and the interconnectedness of user engagement across platforms.</p>

<h2>Background</h2>

<p>As the year comes to an end, Spotify users eagerly await their Spotify Wrapped, a personalized summary of their listening habits, favorite tracks, and most-played artists over the past year. This annual tradition has become a cultural moment, sparking conversations about the music that resonates with people, the genres they gravitate towards, and the songs that defined the past year. Inspired by this excitement, we wanted to explore the underlying factors that contribute to the popularity of songs on Spotify, and how these trends compare to global listening habits tracked by Last.fm. In addition to Spotify’s detailed insights into personal listening data, Last.fm provides a broader, more global view of music consumption through its tracked users' play counts. By combining data from both platforms, we aim to uncover cross-platform trends in music popularity, comparing Spotify’s real-time popularity metrics with Last.fm’s cumulative play counts. Inspired by the Spotify Wrapped season, this project leverages both Spotify and Last.fm data to uncover valuable insights into the evolving landscape of music consumption.</p>

<h2>Data and Sources</h2>

<p>Our project incorporates data from two prominent platforms, Last.fm and Spotify, each offering unique insights into listener engagement and music trends.Both Last.fm and Spotify APIs return semi-structured data in JSON format. </p>

<ul>
  <li><strong>Last.fm API</strong>: The Last.fm API provides data such as track names, artist names, play counts, listener counts, and URLs. Each response is well-organized into nested key-value pairs, with consistent fields like track, artist, playcount, and listeners. Despite this structured organization, it allows variability—for instance, some tracks might have additional fields like tags or genre information, which may not always be present.</li>
  <li><strong>Spotify API</strong>: The Spotify API returns data in JSON format, with fields like name, popularity (ranging from 0 to 100, reflects real-time listener engagement, streaming activity), available_markets, and album. The data includes structured elements (e.g., numeric popularity scores) and lists (e.g., available markets).</li>
</ul>

<p>By integrating data from both platforms, we establish a comprehensive dataset that links Spotify’s dynamic popularity measures with Last.fm’s cumulative listener behavior. This enables a robust analysis of cross-platform trends, offering a nuanced perspective on music popularity. </p>

<h2>Data Preprocessing</h2>

<p>In our analysis, several preprocessing steps were essential to prepare the data for meaningful insights. The data retrieved from the Last.fm and Spotify APIs required cleaning, aggregation, and integration due to differences in data structures, naming conventions, and potential inconsistencies. </p>

<ul>
  <li><strong>Cleansing and Purging of Messy/Incomplete Data:</strong>
    <ul>
      <li><strong>Handling Missing or Incomplete Fields:</strong> Some tracks retrieved lacked certain attributes, such as genre tags from Last.fm or popularity scores from Spotify. We identified these incomplete records and decided whether to exclude them or impute missing values to maintain data integrity.</li>
      <li><strong>Standardizing Data Formats:</strong> Data types were inconsistent; for instance, play counts and listener counts were sometimes strings instead of integers. We converted these fields to appropriate numeric types to enable accurate computations.</li>
      <li><strong>Correcting Inconsistencies in Naming Conventions:</strong> Variations in track and artist names due to capitalization, special characters, or misspellings could hinder accurate data merging. We applied string normalization techniques—such as converting to lowercase and removing special characters—to ensure consistent naming across datasets.</li>
    </ul>
  </li>
</ul>

<ul>
  <li><strong>Aggregation and Summarization of Data:</strong>
    <ul>
      <li><strong>Normalizing Play Counts:</strong> Last.fm's play counts are raw numbers that can range widely, while Spotify's popularity scores are on a 0–100 scale. To compare these metrics directly, we normalized the play counts to a 0–100 scale using min-max normalization.</li>
      <li><strong>Summarizing Genre Popularity:</strong> We aggregated play counts by genre to determine which genres were most popular globally. This involved grouping tracks by their associated genres and summing their normalized play counts.</li>
      <li><strong>Calculating Statistical Measures:</strong> For regression analysis, we computed statistical metrics like means, variances, and correlation coefficients to understand the relationship between variables.</li>
    </ul>
  </li>
</ul>

<ul>
  <li><strong>Combining Different Data Sets:</strong>
    <ul>
      <li><strong>Merging Last.fm and Spotify Data:</strong> The core of our analysis required integrating data from both platforms. We merged the datasets on common keys, primarily the track name and artist name. Due to potential discrepancies, we implemented fuzzy matching algorithms to handle slight differences in naming.</li>
      <li><strong>Eliminating Duplicates and Redundancies:</strong> After merging, duplicate entries were identified and removed to prevent skewing the analysis. We ensured that each track-artist pair was unique in the combined dataset.</li>
      <li><strong>Aligning Data Structures:</strong> The APIs provided data in different formats and structures. We restructured the data frames to have consistent columns, data types, and hierarchies, facilitating seamless analysis and visualization.</li>
    </ul>
  </li>
</ul>

<h3>Rationale for Preprocessing Steps:</h3>
<ul>
  <li><strong>Enhancing Data Quality</strong>: Cleansing and purging were crucial to eliminate inaccuracies and ensure that analyses were based on reliable data.</li>
  <li><strong>Enabling Meaningful Comparisons</strong>: Normalizing and aggregating data allowed us to compare metrics from different sources on a common scale and draw valid conclusions.</li>
  <li><strong>Facilitating Cross-Platform Analysis</strong>: Combining datasets from Last.fm and Spotify was essential to explore the relationship between play counts and popularity scores. Proper integration enabled us to perform regression analyses and generate insights that would not be possible using data from a single source.</li>
 <li><strong>Improving Computational Efficiency</strong>: Preprocessing reduced data complexity and size, which improved the performance of analytical computations and visualizations.</li>
</ul>

<p>By meticulously preprocessing the data, we ensured that our subsequent analyses were accurate, meaningful, and reflective of true listener behavior across platforms.</p>

<h2>Code and Results</h2>
<ul>
  <li><a href="prepcode.md">Prep Code</a></li>
</ul>
