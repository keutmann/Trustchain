# Digital Trust Protocol
Decentralized trust

## Introduction
With the introduction of the World Wide Web, the possibility for everybody to produce content that could potentially each anyone else became possible, however, one crucial element was digitally left behind - Trust. 
The reputation of a few persons could easily be manage, however for a single person to manage the reputation of many others only known loosely, becomes an exhausting task. Relying on friends and family’s trust network may help but usually they are not available at the time or do not even have the same interest sphere. Further the possibility to be anonymous and still provide content make it hard for the reader to verify if the message is authentic.

## Digital Trust Protocol (DTP)
The protocol defines a way to handle trust in the digital world. The idea is to make it possible for everybody to leverage the trust network of anybody else. The goal of the DTP system is it will be able to be used for literally anything, this includes anything from trust, security, rating and identity. 

The system works by a person named Alice trust another person named Bob that trust his Car mechanic. Alice can now check the trust of the Car mechanic without asking Bob for his advice first, this work by querying Alice own trust network on a graph server. The final trust result will depend on a calculation of the trust from Alice to Bob to the Car mechanic. Also known as a chain of trust. Trust is subjective and therefore it should be resolved in a subjective way, this will eliminate the influence from others that are not within Alice trusted network. 

The Trust system is not limited to only person’s trust. It will work on everything, like persons, software, products and organizations. Because it is always possible to create some digital representation of something physical, it is possible to Trust it. 

A trust is a small piece of data with a claim attached to it. It is signed by the creator by used of a Public/Private key algo. When the trust is send to a DTP Graph Server, it will be time stamped by using a blockchain. The signing and timestamping will make the trust secure from tampering of any kind, this will enable the DTP Server to share the trust with other DTP Servers without the risk of tampering.


## Potential use
### Trust
Simply to trust someone or something?

### Confirmation
Confirm the existens of someone or something. It do not matter if its trusted or not.

### Rating
The classic form of current trust are based on a rating / reputation system. However they usually very limited in there scope and specific to particularly domain. The Trustchain system aims to cover everything possible to be trusted.  

### Security
Because of the chain system, it is possibly to give trust to somebody for a limited time, thereby providing access to something. It simply works by the authorization process check if the user is trusted by a specific address. This system could also be used for a ticket system.

### Identity
Identity is not a property to be have, but is something that given or recognized by somebody or something.  Just as a newly formed country/state is first a country/state when other countries and states is recognizing it.
Passport
Government A can issue a trust to another government B. Government B issue a Trust to it citizens. The citizen can prove to the government A that they are citizens of government B. 
The digital identity trusted can be in form of a picture of the citizen with inline printed name and information.  This picture can be stored on a cloud account, making it possible to travel cross border without any devices or papers in hand and still be able to provide proof of identity.

## Goal and requirements
The systems usefulness and value depends on it will be used widely in large networks. Therefore, the system needs to have a low entry point for people to use it, which requires it to be secure, decentralized, scalable, fast, easy and cheap.

### Secure
The protocol will use private/public key algorithm (PK) for proving proof of ownership of a trust, by providing a signature of the Trust, this insures that no other identity can create the same trust. Adding the Trust to a timestamping service based on blockchain technology, will ensure verification of the time of the Trust. This enables the system to replace old with new trust, made from the same issuer to the same subject. 

### Decentralized
It is important to keep the system decentralized in order to avoid gatekeeping of Trust issued on the network. Even that some Trust server may chose not to relay specific Trust, issued by specific issuer, other Trust server, can chose to do so. 

### Scalable
You cannot spent Trust, only issue it. Therefore, there is no need for embedding the Trust into a blockchain. Only the Timestamping service are required, which can provide unlimited timestamps per block, ensures the Trusts are timestamp. The storage method can be any database desired and the peer 2 peer protocol optimized for transfer and relay. The hardware infrastructure sets the limits. 

### Fast
Resolving Trust can be a very CPU and memory resource intensive because of the huge Trust network build up by the clients. Therefore Trust servers with the “Resolver” role, will only be dedicate a specific number of users. This may a local Trust server on a client or a TSR (Trust Server Resolver) hosted by an ISP (Internet Service Provider). 

### Easy
For using the Trustchain system, a client do not need a PK key. A client can simply chose to use predefined list of trusted nodes, or even selected by the application from the start. Only if the user needs to be trusted by somebody else, a key is needed to generate the public key address, however this is easy to produce, it could be generated from a simply password. It is imagined that there will be Browser add-ins and a range of other implementations that will give quick access to issuing Trust. Eventually it may be an imbedded part of most applications using external content.

### Cheap
The system do not have coin or payment method, therefore, the cost of issuing Trust is on the hosting environment of the Trust Servers. It imagined that issuing Trust should be free, but to resolve Trust may come at a cost if it not hosted locally. In the end Trust Providers may be a service include with an Internet Service Provider (ISP) subscription.
In order to avoid spamming, Trust Server can limit who has access to using it for issuing Trust. Furthermore, a Trust Server can imbed spam/ban filters for other Trust Servers on the network known for issuing spam.
