---
description: Resource Records
---

# RRs

Each domain name server maintains resource records which can be requested by any client. These are divided into classes of which the only significant class is “Internet”, I am not aware of any other classes still in use. Within the class, there are record type which correspond to the different kinds of data stored.&#x20;

For example;&#x20;

* An A record defines an IPv4 name/address mapping
* An AAAA record defines an IPv6 name/address mapping
* An MX record is used to define an e-mail exchanger
* A SRV record defines the location of a server for a particular service
* A CNAME record defines an alias

Finding a good single reference to all resource records is difficult, as they are defined in many RFCs. You may need to revert to Wikipedia!&#x20;

Zone Files are the individual collections of resource records that describe a domain. Each zone is described by a general record, the Start of Authority (SOA). If a name server and zone have been delegated as being responsible for a domain, we say they are authoritative for that domain.

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

In a complex arrangement, the solution may not be obvious afterwards. Where I have subdomains I will always document why and how things work.
