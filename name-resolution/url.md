---
description: Uniform Resource Locator
---

# URL

Tim Berners-Lee defined a Uniform Resource Identifier (URI) as “a compact sequence of characters that identifies an abstract or physical resource” \[4]. In the same RFC, he further describes Uniform Resource Locators as referring “to the subset of URIs that, in addition to identifying a resource, provide a means of locating the resource by describing its primary access mechanism”.&#x20;

Consider the URL;&#x20;

```
http://www.lyit.ie/organisation/administration/computerservices/ 
```

In this URL

* http:\ is a protocol
* lyit.ie is the domain name
* www is the hostname of a particular server at lyit.ie
* /organisation/administration/computerservices/ is a directory path.&#x20;

If DNS was not working, we could equally use the URL;&#x20;

```
http://193.1.80.100/organisation/administration/computerservices/ 
```

The Internet is defined by two namespaces, the domain name hierarchy and the Internet Protocol (IP) address system. DNS maintains the domain namespace and provides translation services between these two namespaces.

We use the term Fully Qualified Domain Name (FQDN) to describe the complete domain name for a specific host.
