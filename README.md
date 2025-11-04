🎧 Spotify Songs Analysis Dashboard — Power BI Project
📘 Overview
This project presents a Spotify Songs Analytics Dashboard built in Power BI to analyze song popularity trends, artist performance, and monthly listening patterns using Spotify’s global dataset (Top 50 World).
The dashboard provides a clear picture of how song characteristics (popularity, duration, explicit content, and artist count) vary across months and genres.
________________________________________
🧠 Objectives
•	Analyze the popularity trends of top songs over time.
•	Compare explicit vs non-explicit song distributions.
•	Measure artist performance based on total songs and popularity.
•	Visualize monthly variations in distinct songs and average popularity.
•	Build an interactive and dynamic dashboard using Power BI visuals and DAX.
________________________________________
📊 Key Insights
•	🎵 Average Popularity: 89.62 across 789 distinct songs
•	👩‍🎤 Count of Artists: 342 unique artists, with Taylor Swift leading the charts
•	⏱️ Average Song Duration: 3.28 minutes
•	📈 Peak Popularity: Observed during the last quarter of the year
•	🔥 Most Streamed Songs: “I Wanna Be Yours,” “Cruel Summer,” and “As It Was”

DAX measure USED
DEFINE MEASURE 'Top-50-World'[Avg Popularity] = AVERAGE('Songs'[pop])
DEFINE MEASURE 'Top-50-World'[Count of Artist] = DISTINCTCOUNT('Songs'[artist])
DEFINE MEASURE 'Top-50-World'[Distinct Songs] = DISTINCTCOUNT('Songs'[song])
DEFINE MEASURE 'Top-50-World'[Avg Duration] = AVERAGE('Songs'[duration])
DEFINE MEASURE 'Top-50-World'[Explicit Songs] = CALCULATE(COUNTROWS('Songs'), 'Songs'[explicit] = TRUE)
DEFINE MEASURE 'Top-50-World'[Non-Explicit Songs] = CALCULATE(COUNTROWS('Songs'), 'Songs'[explicit] = FALSE)
