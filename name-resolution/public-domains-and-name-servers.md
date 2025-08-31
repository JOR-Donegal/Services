# Public Domains and Name Servers

The DNS specifications details two types of name server with slightly un-PC terminology; a primary/master and a secondary/slave. A primary/master server is authoritative for the zone and keeps its records in zone files or a database. It replicates this information by means of a zone transfer to secondary/slave name servers, which are also considered authoritative for the zones.&#x20;

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Good design has the primary name server on one subnet/site and the secondary/slave on another subnet/site entirely. We can use whois \[6] to take a look at the registration information for lyit.ie from the IEDR’s website.&#x20;

There are two on-site DNS’s for this domain, but there is an entirely separate name server at HEANet, the Institute’s ISP. This server can be a secondary/slave for many zones (it is, for around 50 other sites) and will keep the site visible to the Internet even if the site loses all connectivity.&#x20;

If I am setting up DNS, I will always set up an off-site secondary. There is no cost if I have access to a secondary server and the bandwidth requirements are modest. The best way to organise this is to make it a reciprocal agreement between sites. Alternatively, host the offsite DNS with your ISP or in the cloud.
