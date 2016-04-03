# Seeing Patterns

In this module we are asked to make a connection between the reading given to us and our work in other history classes. As I am not a historian and the last history class I had was in grade 8, I will try to apply it to my computer science research.

## Network Analysis (Graphs)
For this topic we had to read a Scottbot's blog. I chose the following articles to read (because there are a lot):

### [Topic Modeling and Network Analysis](http://www.scottbot.net/HIAL/index.html@p=221.html)
This article discusses the combination of topic and network models to achieve better results. One example algorithm briefly discussed is ART, which assumes topics are formed based on the combination of authors but also assumes a connection between author and recipient that molds the topic too. This connection means that the algorithm is also considering a communication network. The author also mentions a few more topic models  inferred from networks in less detail.

Next, the author mentions a few networks inferred from topic models, such as inferring social networks from meeting transcripts. He also mentions a combination of topic models and networks where networks were used to represent how documents, topics and words interacted with each other.

Lastly, the author states that one needs to limit how documents are linked, as a model that results in all documents being linked to all other documents is not useful at all. So once again, one needs to understand their problem and the technique before they use these tools to implement the technique.

### [Demystifying Networks](http://www.scottbot.net/HIAL/index.html@p=6279.html)
 This article aims to explain the basics of network analysis in the digital humanities. It mentions the overuse of network analysis. As I mentioned below, the type of analysis tool one chooses depends on the problem being solved, and in this case network analysis is not a free lunch either.

Networks create representations of interdependant components and the relationships between them. These are represented by nodes and edges (lines connecting the nodes). These edges can be directed or undirected and can even have weights assigned to them. There are bimodal (two types of nodes) and multi-modal (multiple types of nodes) networks (though apparently network science does not deal too well with these).

Hypergraphs and multigraphs are also mentioned, but are too new yet to have been incorporated into the toold digital humanists use. In a hypergraph more than two nodes can be connected by one edge, while a multigraph has multiple edges connecting two nodes. These graphs would be more suitable to the humanities as they allow more flexibility in the results.
