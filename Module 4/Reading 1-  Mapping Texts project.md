# Seeing Patterns

In this module we are asked to make a connection between the reading given to us and our work in other history classes. As I am not a historian and the last history class I had was in grade 8, I will try to apply it to my computer science research.

## Mapping Texts Project
This project aims to combine text-mining and geo-spatial analysis for analysing in order to find meaningful language patterns in large collections of text.

As I am not a historian, my research has been in computational intelligence, a field of techniques often used for natural language processing. 

This paper re-visits the issues with simple word searches with no context that were discussed in previous modules. It also revisits the challenges of for OCR when scanning historical documents. These challenges are:

- Bad quality of microfilm images of historical newspapers
- Small fonts and narrow columns of old newspapers

The researchers aimed at creating methods to assess the quality of OCR data by:

- Scrubbing the OCR data and correcting small common errors using the GNU Aspell dictionary
	- They considered using this to also correct misspellings. I feel this shouldn't be done as the data should be transcribed as is in order to be a historical record. However, this would impact language based research on the records.
	- They also had human readers proof reading results in order to ensure that the scripts did not introduce errors rather than fix them. Has this really then automated the process?
- Running the data again against the dictionary to produce word counts of recognised words vs unrecognised words. This gives an indication of the quality of the data
- Data was visualised by time period and geography, using freely available tools. The quality of the data was also visualised.

In order to assess the language patterns, the team used:

- Word counts
- Named Entity Recognition (covered in the previous module, where we used the same parser the team found to b =e the most accurate)
- Topic modeling, which uses statistical models to discover connections between collections of words. This sounds like a place where my masters in temporal data clustering might be useful, as data clustering is often used to find relationships between groups of data. 
	- The team used a tool called MALLET (MAchine Learning for LanguagE Toolkit), where machine learning forms part of Computational Intelligence, which is my specialisation.
	- The team could not generate models for one time period and then combine these with models for another time period. This is because the relationship between the data points is specific to the initial set of parameters given to the algorithm. As a simple example: one cluster of words from one model, may be a similar cluster of another model. Combining these models would then have to result in some form of merging rather than just adding two clusters together.

At this point my power went off, because Africa, and I lost some part of what I was writing and forgot it already ( :( )

The team created visualisations of the data after applying the above methods. These visualisations help make sense of the data by providing visual geographical information along with information about the text.

Although the above methods are great for cleaning up the data and visualising it, the original data is being changed, so is it really a fair analysis? This will always be one of the problems with data, and a good balance needs to be found between cleaning the data to make it machine readable and keeping the original as intact as possible. 

In my case, the question "what would your last essay last term have looked like, if you'd been thinking along these lines?" is not really applicable, as my research was in computer science. However, knowing about the mentioned analytical tools used could have helped with my research by providing a real-life example of the use of data clustering. It would be interesting to find out the inner workings of the MAchine Learning for LanguagE Toolkit.
