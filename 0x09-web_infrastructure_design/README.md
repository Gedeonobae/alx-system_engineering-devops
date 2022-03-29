# Web infrastructure design

This was a week-long project in which I began to research web infrastructure
design. As I conducted research on different design principles, I
whiteboarded diagrams of a developing web infrastructure. I started with a
simple LAMP model and ended with a fully distributed, monitored, and secured
system.

Files in this project contain links to each respective whiteboard diagram


## Concepts

* <a href ="https://howdns.works/"> Learn everything about DNS in cartoon
 </a> <br>

### Be sure to know the main DNS record types: 

* <a href ="https://support.dnsimple.com/articles/a-record/"> A </a> <br>

* <a href ="https://en.wikipedia.org/wiki/CNAME_record"> CNAME </a> <br>

* <a href ="https://en.wikipedia.org/wiki/MX_record"> MX </a> <br>

* <a href ="https://en.wikipedia.org/wiki/TXT_record"> TXT </a> </br>

### Advanced

* <a href ="https://www.dnsknowledge.com/whatis/round-robin-dns/"> Use DNS to scale with round-robin DNS </a> <br>

* <a href ="https://support.dnsimple.com/articles/ns-record/"> What’s an NS Record? </a> <br>

* <a href ="https://support.dnsimple.com/articles/soa-record/"> What’s an SOA Record? </a> <br>

### The root domain and sub domain - differences

<p> A root domain is the parent domain to a sub domain, and its name is not, and can not be divided by a dot.

While creating any domain at a website of domain provider, the provider system will always ask you to choose a domain name without a dot in the name. In other words, the address of the root domain may be mydomain.com but it can never be my.domain.com. Domain providers block the ability to create such a root domain until you type a name without the dot. Why?

The dot in the domain name delimits the sub domain name (the part of the name before the dot, eg. www.my.) and the root domain name ( the part after the dot, ie .domain.com). This means that the address my.domain.com is a sub domain of the root domain, whose name is domain.com

In an administrator panel at domain provider account, you can create any number of sub domains. This means that for the root domain called domain.com it is possible to create different sub domains eg. my.domain.com, your.domain.com, school.domain.com… Creating multiple sub domains is always free and does not require you to set up new accounts on a domain provider website.

As you can see, all of the domain addresses used as an example (above) do not start with the www prefix. www is also a sub domain. The www prefix always leads to the main domain. See: <a href ="https://serverfault.com/questions/145777/what-s-the-point-in-having-www-in-a-url"> What’s the point in having www in a url? </a> </p>
