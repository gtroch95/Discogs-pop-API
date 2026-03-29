---
layout: default
title: Exploring Pop Music Collecting through Discogs
---
## Project Description:

This project explores the past 10 years of pop music physical releases on vinyl, CD, and cassette using the Discogs API. The project visualizes changes over the past decade and uncovers current collector interest in a music-listening era dominated by streaming services.

## Rationale Statement: 

In the current era of streaming services, music released on physical formats like vinyls, CDs, and cassettes feels antithetical to the way most people interact with music today. However, for smaller artists, the ability to make a living through music translates to touring, merch sales, and album sales, not streams. Issues of artist compensation by streaming services as well the ephemerality of and lack of personal ownership over streamed media makes physical media a potentially appealing alternative for music fans. 

For this project, the Discogs API was used to fetch vinyl, CD, and cassette release data from major labels, independent labels, and unsigned artists from 2015-2025, alongside "want" and "have" data from Discogs community members pertaining to releases. Through this project, I aimed to visualize changes in record collecting over the past 10 years and provide a picture of what it looks like in its current state through the genre of pop music. In creating visualizations of the data, I hoped to showcase pop music collecting as a microcosm of physical music releases and record collecting in general.

## Workflow:

I fetched data from the Discogs API using Discogs’ proprietary client, **discogs_client**. Because the API’s request limits and automatic pagination made it near-impossible to get bulk data on all pop releases, I opted to separate my requests into manageable chunks, those being six sub-genres that I felt encompassed most pop music on Discogs: alt-pop, indie pop, synth-pop, dance-pop, europop, and ballad. Additionally, dividing up the requests was beneficial in refining the data, as the definition of "pop" can be quite broad, which is especially evident in the community cataloging practiced on Discogs. 

I created a workflow to reuse for each year from 2015 to 2025 to fetch this data on the six subgenres. **Pandas** was utilized to create data frames for each subgenre, as well as to merge these data frames into one with concat(). These merged dataframes were then saved as separate CSVs, one for each year, and those CSVs were merged, again using concat(). **OpenRefine** was used to clean the data's formatting and remove duplicate rows. From the cleaned CSVs, I again used **Pandas** to create separate data frames based on format and label type for visualization with **Matplotlib** and **Seaborn**. Prior to visualizing the data, the label type dataframes were saved as CSVs and cleaned further in OpenRefine. 

<h2 style="text-align: center;">Visualizations</h2>

![Total releases from 2015 to 2025](https://raw.githubusercontent.com/gtroch95/Discogs-pop-API/master/totalreleases.png)

With this graph showing the past 10 years of physical pop music releases, we see that releases of pop music on vinyl, CD, and cassette slowly decreased until 2021, followed by an increase in 2022 and 2023 before beginning to decrease once more in 2024. Per the Discogs data, 26,859 of these releases were re-releases of older music, or 25.8%. In 2025 specifically, of 7,127 physical pop releases, 1,753 were re-releases, making that 24.5%. Therefore, the majority of pop music being released on vinyl, CD, and cassette is new, but there is still strong interest in older music. 

![Label graph](https://raw.githubusercontent.com/gtroch95/Discogs-pop-API/master/label_graph.png)
![Wants and haves by label type](https://raw.githubusercontent.com/gtroch95/Discogs-pop-API/master/2025_label.png)

These two graphs act as a comparison between Discogs data on label types. The first shows total releases across the past 10 years by label type, and the second shows Discogs community interest in 2025 releases by label type. We see that the majority of physical pop releases have come from independent labels, but there is clearly more interest from the pop record collecting community in major label releases. 

![Format graph](https://raw.githubusercontent.com/gtroch95/Discogs-pop-API/master/format_graph.png)
![Wants and haves by format type](https://raw.githubusercontent.com/gtroch95/Discogs-pop-API/master/2025_format.png)

These two graphs act as a comparison between data on format types. The first shows total releases across the past 10 years by format type, and the second shows Discogs community interest in 2025 releases by format type. Over the past 10 years, vinyl and CDs have traded places in terms of popularity, with vinyl production increasing rapidly before it began to decrease again in 2024. The amount of vinyl records being produced is mirrored in the 2025 community data from Discogs, as vinyl is by far the most popular format for pop record collectors.   

<h2 style="text-align: center;">Takeaways and Future Applications</h2>

Though the future of pop record collecting and music on physical formats cannot be predicted with this data, it seems that despite the production of physical music formats having decreased overall in the past two years, interest in those formats has not necessarily decreased from record collectors. 

Additionally, as this project explored a very commercial genre, it would be interesting to examine other genres for differences. For example, in the pop data, cassettes trail far behind vinyls and CDs, but that would likely look quite different if a genre with a more storied DIY ethos was used, such as certain subgenres of rock or electronic music. 

In the future, this project could be built upon to examine further developments in record collecting and physical music releases in pop. Currently, it could be used to examine other genres. The workflow I used for separating requests into manageable chunks might be particularly useful for those that are having trouble with Discogs’ limitations on bulk data gathering.

