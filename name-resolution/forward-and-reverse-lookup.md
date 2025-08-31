# Forward and Reverse Lookup

Forward lookup is where we provide a resolver with a name like www.lyit.ie and get a response like 193.1.80.100. Reverse lookup is where we provide an IP address like 193.1.80.16 and get a response dns2.lyit.ie.&#x20;

One of the most confusing things about DNS is that the database for forward and reverse are separate and may be inconsistent. Indeed, many people do not bother to populate the reverse lookup zones. This is a bad idea!&#x20;

ICANN put aside a special domain for reverse lookup, the in-addr.arpa domain. Every IP address can appear in this name space, there should be an entry for the University web site.&#x20;

To add to the confusion, because the domain is inverse-tree shaped, all the addresses are backwards!! So www.lyit.ie which has an IP address of 193.1.80.100 will have a reverse lookup entry as 100.80.1.193.in-addr.arpa

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Reverse domain entries were originally done as blocks of 256 addresses and for this reason, we normally see them as blocks equivalent to class C address space.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

In Linux these zones files are text files within a folder structure.
