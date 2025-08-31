# Limitations

At time of writing there were over 1,000 gTLDs and c.250 ccTLDs.&#x20;

* Each branch is a label <63 characters&#x20;
* Each word between dots <63 characters&#x20;
* Total domain name <253 characters&#x20;
* Total Levels <= 127&#x20;
* Each label may consist of any character but in practice uses letters, digits, hyphens&#x20;
* An NS record defines a name server for the domain

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

I am using the Windows implementation in these notes set, as it is easy to follow. In Linux, we use BIND, do look it up and be familiar with it, it is the reference architecture! 
