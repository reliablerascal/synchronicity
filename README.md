# Still Shouting above the Din of Our Rice Krispies
_An analysis of the staying power of Synchronicity by The Police, four decades after its release_

This project looks at the enduring legacy of _Synchronicity_ by The Police on the 40th anniversary of its release on 17 June 17 1983.

Here's my story, [Still Shouting above the Din of Our Rice Krispies](https://reliablerascal.github.io/synchronicity/), as published on GitHub.

## Key Findings
My key findings are as follows:
<ul>
<li>Synchronicity was the #1-selling record in the U.S. for 17 weeks, surpassed only by Thriller by Michael Jackson at 22 weeks. Thriller is a tough comparison, because it's the best-selling record of all time.
<li>The Police have more than twice as many active monthly listeners today on Spotify as the three members' solo acts combined.
<li>Published cover versions of Synchronicity tracks peaked in the third decade following its release, from 2003 to 2012, according to data from <a target = "_blank" href="https://secondhandsongs.com/">Second Hand Songs</a>
</ul>

## Data sources
|Data Source|Description|
|---|---|
|[SecondHandSongs](https://secondhandsongs.com/release/413)|This database tracks published covers of songs, and seems to be more comprehensive than rival databases [cover.info](https://cover.info/) and [whosampled.com](https://www.whosampled.com/Database/) |
|[Spotify Monthly Listeners](https://open.spotify.com/artist/5NGO30tJxFlKixkPSgXcFE)|This tracks the current number of monthly listeners for each artist|
|[U.S. Billboard #1 Charts for 1983](https://en.wikipedia.org/wiki/List_of_Billboard_200_number-one_albums_of_1983)|Compiled for published print versions of Billboard magazine, this tracks the #1 best-selling album in the U.S. by week|

## Overview of Data Analysis Process
My data analysis process required the following steps:
* Acquired basic contextual data manually from Billboard and Spotify
* Acquired info on cover songs by decade for each of four albums by scraping the list of hyperlinks for each track on [each album's release page](https://secondhandsongs.com/release/413) and then creating a dataframe tracking the year of release of [each cover](https://secondhandsongs.com/performance/656).
* Cleaned up data by subtracting one from each track's cover count to remove the original recording, and adding Men at Work's "Down Under" (a separately tracked single) to that band's dataframe
* Summed count of covers by decade- 1983 to 1992, 1993 to 2002, 2003 to 2012, 2013 to 2022
* Prepared graphics by organizing data in Google Sheets

## Data Quirks and Other E-Varmints Standing in My Righteous Path
I initially tried to look at deep engagement in song lyrics, based on comments in [SongMeanings.com](https://songmeanings.com/albums/view/tracks/1816/). But haven't yet learned how to scrape a page built on Javascript results.worked on a web scraper.

Developing my graphics, I also had significant trouble getting Figma2HTML to render properly with complex graphics, and ending up instead relying on my CSS for addressing graphics responsiveness. At this point, it's best to wait for subsequent releases of this otherwise handy tool.

## What I Learned
I gained a lot of practice with tailoring graphics using Figma. The final rendering of graphics depended on two happy accidents:
* Mistakenly trying to create a series of pie charts with one row of data, resulting in the "planet" chart (a.k.a. single-slice pie chart) showing relative popularity of Sting vs. The Police
* My attempt to create a streamgraph "mountain" chart showing the depth of cover songs ended up looking more like a flame. So, I tailored the colors accordingly.

I also gained some practice with web scraping.

## What I'd Like to Learn Next to Advance this Project
I originally wanted to create a graphic showing covers by decade as a grove of trees, with each branch representing a song and each cover a leaf on each branch. Some day I may learn to do this in D3, but that's way too complex of a task for a short deadline.

I'd also like to build my web scraping and text analysis skills so I can analyze listener engagement based on comments in Songmeanings and Genius.com.

## Guide to the Repository
Following is an overview of files in this repository:

<!---* [source_data](source/data/)- includes only my own manually-entered lookup table for CTA stations--->
* [Jupyter Notebook](scrape_secondhand.ipynb)- steps through scraping Second Hand Songs
* [results](results/)- results output from Jupyter Notebook scraping of Second Hand Songs
* [results for graphics](results_graphics/)- results organized and prepped for graphics design in DataWrapper, Rawgraphs, and Figma

