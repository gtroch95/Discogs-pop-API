# Exploring Pop Music Collecting through Discogs

## Project Description:

This project examines the past 10 years of pop music physical releases on vinyl, CD, and cassette using the Discogs API. The project visualizes changes over the past decade across major labels, independent labels, and self-released artists, and uncovers current broad collector interest in a music-listening era dominated by streaming services.

## Rationale Statement: 

Streaming services are the main method by which people currently listen to music; nevertheless, there has remained a strong community of collectors of physical albums. This community has the potential to grow due to streaming and subscription fatigue, the desire for personal ownership, and nostalgia. Additionally, public awareness has developed around the poor compensation of artists by streaming services, which especially affects artists signed to smaller independent labels and those who are not signed at all; an increased interest in purchasing physical albums could tangibly affect these artists’ ability to make music. 
  
With these factors in mind, this project was undertaken to understand how physical pop record releases have developed over the past decade and where pop record collecting actually stands in 2025. Pop music in particular was chosen for this project because it moves with the trends and encompasses a wide diversity of artists, from the most commercially successful to the truly bedroom-produced.  

## Workflow:

I fetched data from the Discogs API using Discogs’ proprietary client, **discogs_client**. Because the API’s request limits and automatic pagination made it near-impossible to get bulk data on all pop releases, I opted to separate my requests into manageable chunks, those being five sub-genres that I felt encompassed most pop music: alt-pop, indie pop, synth-pop, dance-pop, and ballad. Additionally, dividing up the requests was beneficial in refining the data, as the definition of "pop" can be quite broad, which is especially evident in the community cataloging practiced on Discogs. My results were therefore more "true" pop than if I had fetched data on all releases cataloged as being part of the "pop" genre.

I created a workflow to reuse for each year from 2015 to 2025 to fetch this data on the five subgeners. **Pandas** was utilized to create data frames for each sub-genre, as well as to merge these data frames into one. These merged dataframes were then exported as separate CSVs, one for each year. **OpenRefine** was used to combine the CSVs into one that encompassed 2015 - 2025, as well as to clean the data's formatting and remove any duplicate rows. From the main CSV, I again used **Pandas** to create separate data frames for use with **MatLibPlot** and **Seaborn** for visualization.  

## Further Uses:

	In the future, this project could be built upon to examine further developments in record collecting and physical music releases in pop. Currently, it could be used to examine other genres. The workflow I used for separating requests into manageable chunks might be particularly useful for those that are having trouble with Discogs’ limitations on bulk data gathering.

## Files:

Discogs_pop.ipynb contains the initial code used to fetch data from Discogs, create and merge the separate subgenre data frames, and save the resulting dataframe to CSV

Pop_2015.csv, Pop_2016.csv, Pop_2017.csv, etc… are the 11 CSVs that were created from Discogs_pop.ipynb

Pop_cleaned.csv is the merged CSV of all 10 years that was created using OpenRefine, with formatting cleaned

Dataframe_visualization.ipynb contains the code used to create smaller dataframes from the CSV for visualization, as well as the code for the graphs
