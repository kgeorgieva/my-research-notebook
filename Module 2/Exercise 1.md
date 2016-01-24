# Analysis of dream case data


### Epigraphic Database Heidelberg

The task was to search for some latin words in this database. I used the example provided as I've never done latin.

The search results can be found [here](http://edh-www.adw.uni-heidelberg.de/inschrift/suche?hd_nr=&land=&fo_antik=&fo_modern=&literatur=&dat_jahr_a=&dat_jahr_e=&atext1=figli*&bool=AND&atext2=&sort=hd_nr&anzahl=20). The downloaded data can also be found in this folder.

I found that this export had a lot of natural language and would not be too suitable to analyse using a computational intelligence algorithm.


### Commwealth War Graves Commission, Find War Dead

The task was to search for one's own surname in this databases. My surname, however, is Bulgarian and did not retrieve any results. I have therefore used my partner's surname (Young) as he is South African and the surname retrieves a lot of records. Additionally his father has an interest in genealogy and would find this data of high interest.


The search results for Young can be found in this folder. I would have linked to them but the application is a single page application that uses a post and not a get to retrieve the search, so the search parameters are not included in the URL.

I found that this dataset was a bit more structured than the Epigraphic one, including categories and more separated concerns. This would make it a more appropriate dataset to analyse with computational intelligence algorithms.

### General comments applying to both datasets

Being able to extract the data into CSV/spreadsheet format is great as from here we can easily import it into a SQL database, giving us SQL's power to look through the data.