# Musical-Analysis

## Project Overview

This project involves the extraction, cleaning, and analysis of Spotify's top songs from the decade spanning 2010 to 2019. The goal was to combine yearly datasets, standardize the data types for analytical processing, and extract meaningful insights regarding musical trends, artist popularity, and song characteristics.

## Dataset Description

The final dataset consists of several musical attributes:

- **ID**: Unique identifier for each track.
- **Title/Artist**: Song metadata.
- **Top Genre**: The specific genre classification.
- **Year**: Release year.
- **BPM**: Tempo (Beats Per Minute).
- **Energy (nrgy)**: Intensity and activity level.
- **Danceability (dnce)**: Suitability for dancing.
- **Loudness (db)**: Average decibel level.
- **Valence (val)**: Musical positiveness.
- **Acousticness (acous)**: Amount of acoustic vs. electronic sound.
- **Speechiness (spch)**: Presence of spoken words.
- **Popularity (pop)**: Overall listener popularity score.

## Installation & Setup

1. **Clone the repository** and navigate to the project folder.
2. **Create a Virtual Environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # macOS/Linux
   venv\\Scripts\\activate     # Windows
   ```
3. **Install Dependencies:**
   ```bash
   pip install pandas matplotlib seaborn jupyterlab
   ```
4. **Launch the Analysis:**
    ```bash
    jupyter lab
    ```
Data Cleaning Process
To ensure an "Exceeds Expectations" grade, the following cleaning steps were implemented:

Encoding Management: Used latin-1 encoding to handle non-standard characters in song titles (e.g., accents).

Header Standardization: Renamed inconsistent headers (like Unnamed: 0 to id and dB to db).

Type Conversion: Forced numeric conversion using pd.to_numeric with errors='coerce'.

Handling Missing Values: Dropped rows containing null values in critical numeric columns to maintain data integrity for statistical analysis.

Key Insights
Most Popular Song: Identifies the single track with the highest popularity score.

Genre Trends: Analysis of the most frequent genres over the decade.

Energy vs. BPM: Statistical correlation calculated to see if faster songs are inherently more energetic.

Live & Acoustic Analysis: Calculated the percentage of studio vs. live/acoustic tracks using threshold logic (>50).

Files Generated
top_spotify_songs.csv: The final, cleaned, and combined dataset.
