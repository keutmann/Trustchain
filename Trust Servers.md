#Trust Servers

##Introduction 
The Trustchain system consist of several components app combined into a single applications.


###TrustGraph
Adding Trust to the system will build up a Graph like structure. This needs a query engine, which are able to traverse through the structure in order to resolve the Trust. 
The rules for the resolver are as following.
*	Follows shallow pattern first
*	Find shortest path, if multiple exist at same level, the most Trust with the same value are used
*	Distrusted nodes are not followed
