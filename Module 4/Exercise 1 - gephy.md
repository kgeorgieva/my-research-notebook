# Exercise 1

In this exercise we use Gephy to create a network model.

The model looked rather convoluted and not very informative when it was first imported. This is the first thing I saw:

![](https://raw.githubusercontent.com/kgeorgieva/my-research-notebook/master/Module%204/images/network.PNG)

According to the tutorial, in the data lab , under the edges tab I should be seeing "Henderson is in the “Source” column, Webb in the “Target,”, and the “Weight” is three.". When I look for Henderson I see 2 separate entries from Henderson to Webb with weights of 1, not 1 entry with a weight of 3. I've tried to replicate this requirement with my file as well as the one provided for those that didn't manage to get the file working last time.

Next we cleared the data by removing the disconnected nodes. This resulted in a much smaller network with is ore manageable. This is a nice tool to remove data outcasts before feeding data to a Computational Intelligence algorithm. It must be used within reason though, as it does mean data gets removed which might skew analysis.

