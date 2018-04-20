#Trustchain Protocol
    
##Introduction
Anything digital can be trusted. This is done by making a digital checksum (HASH) value of the digital value, known as an Address, and issuing a Trust to that Address. For issuing a Trust, one needs to have a Subject Address, which are generated from a private/public key algorithm.
This ends up with two types of nodes.
1.	End Nodes, can receive Trust but cannot issue Trust. The node is based on any form digital martial, like documents, pictures, and sound or any other digital value.
2.	Entity Nodes can receive Trust and can issue Trust. The node is based on a private/public key that represent any form of entity. This can be a person, organization and software. Anything that are able to make a decision on its own or indirectly.
The Trust
When an entity issue a Trust, it makes a connection between to nodes. This connection contains some standard data about the trust.

##Blockchain
A blockchain is very good at controlling ownership of a token, and ensuring that token cannot be double spent. However, Trustchain system do not need a traditional blockchain, because there is no token to be owned. Trust can be handed out unlimited from a single source and nobody else can spend that trust again. Only thing needed is the timestamp service to ensure that Trust cannot be fabricate back or ahead of time. There will be no blockchain in the Trustchain system.


##Trust schema
```
{
"head": {
"version": "standard 0.1.0",
"script": "btc-pkh"
},
"body": {
"subject": "1ERgQJdwncLvXv16mQaKu...",
"subjecttype": "person",
"confirm": true,
"trust": true,
"custom": null,
"activate": 1231006505,
"expire": 2231006505,
"routingcost": 100,
"scope": "global",
"issuer": "1DuDZDtoLfNHrmSY2QUCWu...",
"server": "1HQkogrxHpobnrtPkeHuBm9r4s..."
},
"timestamp": [
{
"blockchain": "bitcoin",
"proof": "MHg2ODU4ZmNkNDhmMjg1OGI4MWFmZGRmYmI0MmZ..."
},
{
"blockchain": "ethereum",
"proof": "MHhiN2ZmZjQ5MDAwNWUyOWM4YmFhNjY4NzA3NmZ..."
}
],
"signature": {
"issuer": "VGhpcyBpcyB0aGUgc2lnbmF0dXJlIGZvciB0aGUgaXNzdWVy",
"subject": "",
"server": "VGhlIHNlcnZlciBoYXMgaXRzIG93biBzaWduYXR1cmUNCg=="
}
}
```

The explanation of the Trust entry with following properties.

*Head*
It provides with information about how to read the Trust issued.

*Version*
A string that tells the Trust server how to read the Trust, especially the custom property field.

*Script*
The scripting language used to sign the Trust with, the “btc-pkh” value stands for “Bitcoin Pay 2 Public Key Hash” algorithm.

*Body*

*Subject*
This can be either the address of an End Node or the Entity Node public key Address.

*SubjectType*
Some description id of the subject address. This may something like “Person”, “Organization” or “Software”, it can literally anything.

*Confirm*
This confirms the subject and the subjecttype is valid. It is a way to say a person exist or not exist.

*Trust*
This indicates if the subject is trusted or not.

*Custom*
For providing custom data, regarding the Trust. It can be used for providing “5 star” rating information about a product or some services. It works with the Version property in the Head section, where the version string can be some code that indicate the data structure in the custom field. This makes it possible to make any form of trust that is specialized to specific purposes. Then only Trust Servers that understand the specific version code will process the Trust.

*Issuer*
This can only be from an entity node, because the need for signing with the private key to the public key address.

*RoutingCost*
When trust has to be resolved, a Trust Resolver Service is needed. To limit the processing power consumed processing the trust chains, the value of RoutingCost are used the limit the search in the Graph network of Trust. The RoutingCost solves the problem with large organizations will providing Trust. They need to be able to delegate out that task of issuing Trust to multiple entities but still have only one a main Trust Address to be trusted. This main address will trust the delegated issuer’s trust that again may Trust other internal Trust issuers. This introduce a longer chain than normal and therefore provide an unrealistic result from the Trust resolver calculating the RoutingCost. The property will have the value no lower of 100 points expect if the Issuer can provide the signature for both the issuer and receiver address. This makes it possible to provide internal Trust with a very low RoutingCost value that will count very little against the RoutingCost limit of the Trust Resolver.

*Scope*
Trust have limited value and only relevant to a small number of people. The Scope property makes it possible to define a scope of relevance. Like the most of the world may care very little about what a factory worker in Peru thinks of his local coffee shop. Most Trust servers will likely concentrate on specific scopes and thereby limit the number of Trust needed to be processed.

*Activate*
The datetime value when the Trust is considered included by the resolving process.

*Expire*
The datetime value when the Trust is considered excluded from the resolving process.
The Trust may be removed from the Trust server, as it will never be used again.

*Timestamp*
Timestamp is used to verify creation date. However, a timestamp requires a blockchain to make proof of its creation date. The Merkle Tree Hash algorithm solves this, where it is possible to create a very high amount of timestamps within a single transaction on some blockchain. Because of the timestamp, it is possible to replace the Trust issue with a new Trust and thereby alternating the existing Trust. The old Trust will not be used anymore and possible discarded.
The property is optional. However, the Trust Node server receiving the Trust will automatically create the timestamp.

*Signature*
Issuer: The signature of the Trust issuer proofs that the issuer is indeed the owner of the issuer address.
Subject: The signature of the receiver of the Trust, used for lowing the RoutingCost property value.
Server: The signature of the Trust Server issuing the Trust on behalf of the client. Makes it possible to trust servers and avoid spam. (May be optional)
