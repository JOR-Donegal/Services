# Private Domains and Name Servers

A modern LAN needs DNS to work. Microsoft’s Active Directory (AD) is the most common and popular system for Authentication, Authorization and Accounting (AAA) and requires an integrated DNS to work. If my main organisation has a domain name of lyit.ie, I can create internal sub-domains which are not intended to be visible from the Internet.&#x20;

For example, letterkenny.lyit.ie, buncrana.lyit.ie, headoffice.lyit.ie etc.&#x20;

This is the concept of Split Head DNS; one group of name servers advertising public services eternally and another group for internal use, not visible to the Internet.&#x20;

Split head DNS is normal for large organisations and it is important from a security perspective. Anyone who can query your internal DNS service can quickly enumerate your network, mapping out services, servers, subnets and resources.&#x20;

Read Microsoft’s recommendations for this before setting up an Active Directory (AD) domain. The root of any AD forest will be a subdomain of the registered domain name; by convention this is often **ads**. So the AD domain name at the teaching data centre, Letterkenny is&#x20;

```
ads.letterkenny.kmn.ie
```
