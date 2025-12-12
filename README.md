# Exploring Pop Music Collecting through Discogs

## Project Description:

This project explores the past 10 years of pop music physical releases on vinyl, CD, and cassette using the Discogs API. The project visualizes changes over the past decade and uncovers current collector interest in a music-listening era dominated by streaming services.

## Rationale Statement: 

In the current era of streaming services, music released on physical formats like vinyls, CDs, and cassettes feels antithetical to the way most people interact with music today. However, for smaller artists, the ability to make a living through music translates to touring, merch sales, and album sales, not streams. Issues of artist compensation by streaming services as well the ephemerality of and lack of personal ownership over streamed media makes physical media a potentially appealing alternative for music fans. Through this project, I aimed to visualize changes in record collecting over the past 10 years and provide a picture of what it looks like in its current state through the genre of pop music. Pop music in particular was chosen for this project because it moves with the trends, making it a good candidate for visualization. 

## Workflow:

I fetched data from the Discogs API using Discogs’ proprietary client, **discogs_client**. Because the API’s request limits and automatic pagination made it near-impossible to get bulk data on all pop releases, I opted to separate my requests into manageable chunks, those being six sub-genres that I felt encompassed most pop music on Discogs: alt-pop, indie pop, synth-pop, dance-pop, europop, and ballad. Additionally, dividing up the requests was beneficial in refining the data, as the definition of "pop" can be quite broad, which is especially evident in the community cataloging practiced on Discogs. 

I created a workflow to reuse for each year from 2015 to 2025 to fetch this data on the six subgenres. **Pandas** was utilized to create data frames for each subgenre, as well as to merge these data frames into one with concat(). These merged dataframes were then saved as separate CSVs, one for each year, and those CSVs were merged, again using concat(). **OpenRefine** was used to clean the data's formatting and remove duplicate rows. From the cleaned CSVs, I again used **Pandas** to create separate data frames for visualization with **MatLibPlot** and **Seaborn**.  

## Further Uses:

In the future, this project could be built upon to examine further developments in record collecting and physical music releases in pop. Currently, it could be used to examine other genres. The workflow I used for separating requests into manageable chunks might be particularly useful for those that are having trouble with Discogs’ limitations on bulk data gathering.

## Files:

- Discogs_pop.ipynb contains the initial code used to fetch data from Discogs, create and merge the separate subgenre data frames, and save the resulting dataframe to CSV.

- The CSV-years folder contains the 11 CSVs that were created from Discogs_pop.ipynb (Pop2015.csv, Pop2016.csv, Pop2017.csv, etc.), as well as Pop2025_cleaned.csv, which was used for visualization.

- The CSV-labels folder contains both the initial and cleaned CSVs used to create label-based dataframes for visualization for Major_releases.csv, Major_releases_cleaned.csv, Self_released.csv, and Self_released_cleaned.csv. The file sizes of Independent_releases.csv and Independent_releases_cleaned.csv were too large, and so they've been compressed into the zip files independent_releases.csv.gz and independent_releases_cleaned.csv.gz respectively.  

- Pop_cleaned.csv.gz is the merged CSV of all 10 years that was created using OpenRefine, with formatting cleaned. The file size is too large for the GitHub repository, so it has been compressed into a zip file. 

- Dataframe_visualization.ipynb contains the code used to create smaller dataframes from the CSV for visualization, as well as the code for the final graphs.

- format_graph.png, label_graph.png, wantshaves_label.png, wantshaves_format.png, 2025_label.png, 2025_format.png, and totalreleases.png are the graphs created for this project.
