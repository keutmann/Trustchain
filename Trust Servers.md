#Trust Servers

##Introduction 
The Trustchain system consist of several components each divided into a Application server each.
* TrustBuild
* TrustStamp
* TrustIndex
* TrustTorrent
* TrustTorrentTrack
* TrustResolve

TODO:
Describe all servers

###TrustResolve
Adding Trust to the system will build up a Graf like structure. This needs a resolver, which are able to traverse through the structure in order to resolve the Trust. 
The rules for the resolver are as following.
*	Follows shallow pattern first
*	Find shortest path, if multiple exist at same level, the most Trust with the same value are used
*	Distrusted nodes are not followed

** Chaining and hash tables **
Normally Trust are chained up, however it is also possible the use hash tables. This occurs when a node trusts a high number of nodes, then the resolvment of Trust from that node may simple be impractical. 
Imagine a search provider issuing trust to millions of nodes from one single node. Using a hash table, will make it possible for the resolver to evaluate the Trust fast. The downside is that the Resolver will not be able to follow the trust further down.
