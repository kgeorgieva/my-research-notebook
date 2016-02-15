# Working with Open refine

- server timed out at some point

### Clustering 
I found that the clustering algorithms seemed pretty good for this task. I did the following for each method:

-  key collision fingerprint - merged all
-  key collision ngram-fingerprint - no results (probably due to previous merge). Changed size to 1 and it found a valid pair.
-  key collision metaphone3 - did not merge any. These were different senders.
-  key collision cologne-phonetic - merged all
-  Nearest neighbour levenshtein - merged all on default. Changed radius to 2.0 and merged a few that had symbols or contained rn as m. Block chars didn't make a difference in my case.
-  Nearest neighbour PPM - merged all. Changed radius to 2/0 and found a few more to merge. there was an interesting one where the word "reply" was also included but the clustering algorithm figured it out. Radius 3.0 and up retrieved irrelevant results.

As someone that has worked with clustering algorithms I understand what the radius means for example. However, someone that is not exposed to the inner workings of clustering may not. The same applies to the algorithm's names.  I personally have no idea what Block Chars means in this context. An explanation should be provided in the application, either through a hover state or clickable links.

It says in the exercise that we should end up with more or less 150 senders. My exercise resulted in 160. The remaining clusters when playing with the clustering capabilities of the application were not valid options to merge (in my case).

I was a lot more confident with the application when working with the recipients as it was the second attempt at this. I managed to reduce these to 163, which is close to the expected 160+-.

### Palladio
Exported graph of sender and recipient. The map is quite big, so it does not really filter much information out.

The graph for a recipient and date combination is also huge and doesn't really filter much out.

The table just gives a table view of the columns selected. This doesn't give any more insight than the CSV

A map is not appropriate for this exercise as there is no location data.