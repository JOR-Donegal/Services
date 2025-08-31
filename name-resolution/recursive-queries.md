# Recursive Queries

With a recursive query, the client/resolver may ask a name server for a record it is not authoritative for. The name server is then obliged to go off and find the answer!&#x20;

Supposing the query is unique, and the servers have no close answers cached, I want to find the engineering department at MIT. First my DNS queries a root name server on the Internet to ask it where to find the name servers for the .edu domain. It uses the response to ask the .edu servers where to find the mit.edu domain name servers. Finally, it asks the mit.edu name servers where to find the name server authoritative for engineering.mit.edu.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

There are security issues here and there are weaknesses to the DNS system. I can for example put false information into a DNS response and “poison” the cache. Cache poisoning is a standard attack vector and there are ways to protect against it. Making a query against a root server is probably safe enough, however once you are referred on, not so safe.&#x20;

Forwarding requests to a managed, clean DNS service is probably safer and we can manually configure forwarders at the server level. Many recommendations tell users to use their ISP. The performance of your ISPs solution should be good, there is no way to know what the security of the solution will be like. Companies come and go, so for want of a better reference, take a look at [this](https://en.wikipedia.org/wiki/Public_recursive_name_server). No one provides this service for free (!) so read the small print to see why you are being provided with the service. These days, it’s all about analytics, the providers can figure out what you are buying etc. based on your DNS activity.&#x20;

For specific domains, we can configure conditional forwarders and in the example below, I show how the various data centres of lyit-cdc.net resolve.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Many environments are simple and have no forwarders. But when you need them...
