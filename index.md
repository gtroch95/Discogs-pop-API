---
layout: default
---

## Introduction

In the current era of streaming services, music released on physical formats like vinyls, CDs, and cassettes feels antithetical to the way most people interact with music today. However, for smaller artists, the ability to make a living through music translates to touring, merch sales, and album sales, not streams. Issues of abysmal artist compensation by major streaming services as well the ephemerality of streamed media and lack of personal ownership makes physical media a potentially appealing alternative for music fans. Through this project, I aimed to visualize changes in record collecting over the past 10 years and provide a picture of what it looks like in its current state using release data and community collecting data from the Discogs API.  

Specifically, the Discogs API was used to fetch vinyl, CD, and cassette release data from major labels, independent labels, and unsigned artists from 2015-2025, alongside "want" and "have" data from Discogs community members pertaining to releases. Pop music was chosen for this project because it moves with the trends, making it a good candidate for visualization. Through visualizing the data, I hoped to showcase pop music collecting as a microcosm of physical music releases and record collecting in general. 

## Visualizations

![Total releases from 2015 to 2025](https://raw.githubusercontent.com/gtroch95/Discogs-pop-API/master/totalreleases.png)

With this graph showing the past 10 years of physical pop music releases, we see that releases of pop music on vinyl, CD, and cassette slowly decreased until 2021, followed by an increase in 2022 and 2023 before decreasing once more from 2024 to 2025. 

![Label graph](https://raw.githubusercontent.com/gtroch95/Discogs-pop-API/master/label_graph.png)
![Wants and haves by label type](https://raw.githubusercontent.com/gtroch95/Discogs-pop-API/master/2025_label.png)

These two graphs act as a comparison between data on label types. The first shows total releases across the past 10 years by label type, and the second shows Discogs community interest in 2025 releases by label type. We see that the majority of physical pop releases have come from independent labels, but there is clearly more interest from the pop record collecting community in major label releases. 

![Format graph](https://raw.githubusercontent.com/gtroch95/Discogs-pop-API/master/format_graph.png)
![Wants and haves by format type](https://raw.githubusercontent.com/gtroch95/Discogs-pop-API/master/2025_format.png)

These two graphs act as a comparison between data on format types. The first shows total releases across the past 10 years by format type, and the second shows Discogs community interest in 2025 releases by format type. Over the past 10 years, vinyl and CDs have traded places in terms of popularity, with vinyl production increasing rapidly before it began to decrease again in 2024. The amount of vinyl records being produced is mirrored in the 2025 community data from Discogs, as vinyl is by far the most popular format for pop record collectors.   


In the graph showing interst in formats, vinyl is clearly the most popular. We see in the second graph that vinyl has grown in popularity as a format  having grown in popularity over the past 10 years. 

Graphs by label / format

![Label_graph](https://raw.githubusercontent.com/gtroch95/Discogs-pop-API/master/label_graph.png)


26,859 of releases from 2015-2025 were re-releases of older music. In 2025 specifically, 1,753 of the total releases were re-releases of older music. Therefore, the majority of music being released on physical formats is new. Additionally, for re-releases from 2025, there were 54,721 "wants" total from the Discogs community, and 248,037 "haves." 



