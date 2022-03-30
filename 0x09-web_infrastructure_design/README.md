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

## Be sure to know the main DNS record types: 

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


## Monitoring

<p> 

Just as the heart monitor in a hospital that is making sure that a patient’s heart is beating and at the right beat, software monitoring will watch computer metrics, record them, and emit an alert if something is unusual or that could make the computer not work properly happens.

You cannot fix or improve what you cannot measure is a famous saying in the tech industry. In the age of the data-ism, monitoring how our software systems are doing is an important thing.

Web stack monitoring can be broken down into 2 categories:

    Application monitoring: getting data about your running software and making sure it is behaving as expected
    Server monitoring: getting data about your virtual or physical server and making sure they are not overloaded (could be CPU, memory, disk or network overload)

### Here are few famous monitoring tools:

### NewRelic

NewRelic requires you to add a piece of JavaScript to your website, this agent will collect information and send it back to the New Relic servers. It will give you a detailed analysis of how quickly your website loads in a browser, with a detailed analysis at every level of the stack. If the website is loading too slowly or users are experiencing error (500), there is a feature that allows you to trigger an alert. NewRelic now does much more than this, I’ll let you discover the rest.

### DataDog

DataDog allows you to measure and monitor everything with graphs. It gathers performance data from all your application components. The service has a lot of integrations. You usually just need to properly configure your alert and you are good to go with solid monitoring coverage.

### Uptime Robot

Uptime Robot is a simple service that will check that your website is responding from multiple locations in the world. This is the bare minimum when you host a website.

### Nagios

Nagios is an open source project started in 1999, it is among the most widely used monitoring tools in the tech industry. It is, however, seen as outdated. Nagios had trouble adapting to the rise of the Cloud but is slowly trying to catch up.

### WaveFront

Wavefront is a cutting edge monitoring service funded by great software engineers who’ve built monitoring tools for the best tech companies in Silicon Valley. The idea is to be able to analyze anything that can produce data points. A query language that looks like SQL allows users to apply mathematical operations to these data points to extract values or detect anomalies from the time series data. While it takes some time to get used to the tool, it’s the type of monitoring that the best companies are using. To my knowledge, LinkedIn, Facebook and DropBox are using a very similar tool for their monitoring needs.
 </p> <br>

##  Web Server 

* Do not mix up web server and server.

A web server is a software that delivers web pages. A server is an actual computer.

But you might hear people referring to a web server using the word server. (Check out the server concept page to learn more about this.)

As mentioned above, a server is a physical machine, an actual computer, but in the Cloud era that could also be a virtual computer, generally called a VM (<a href ="https://en.wikipedia.org/wiki/Virtual_machine"> Virtual Machine </a>) or <a href ="https://www.cio.com/article/247005/what-are-containers-and-why-do-you-need-them.html"> container</a>. <br>

### Readme:

* <a href="https://en.wikipedia.org/wiki/Web_server"> Wikipedia page about web server </a> <br>

* <a href="https://whatis.techtarget.com/definition/Web-server"> Web server </a> <br>

* <a href="https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_web_server"> What is a Web Server? </a> <br>

## Network basis

* <a href="https://www.techtarget.com/searchnetworking/definition/protocol"> What is a protocol </a> <br>

* <a href="https://computer.howstuffworks.com/internet/basics/what-is-an-ip-address.htm"> What is an IP address </a> <br>
     
* <a href="https://www.techtarget.com/searchnetworking/definition/TCP-IP"> What is TCP/IP </a> <br>

* <a href=""https://www.lifewire.com/port-numbers-on-computer-networks-817939> What is an Internet Protocol (IP) port? </a> <br>

## Load balancer

* <a href ="https://www.thegeekstuff.com/2016/01/load-balancer-intro/"> Load-balancing </a> <br>

* <a href ="https://community.f5.com/t5/technical-articles/intro-to-load-balancing-for-developers-ndash-the-algorithms/ta-p/273759"> Load-balancing algorithms </a> <br>

## Server

<p>

Servers are located in datacenters which are buildings that host hundreds, or even thousands of computers (servers). You can think of a server as a computer without a keyboard, mouse, or screen, that is accessible only by a network. A server can be physical or virtual. A server runs an OS (operating system).

Read:

    * <a href="https://en.wikipedia.org/wiki/Server_(computing)#Hardware_requirement"> What is a server </a>

Watch:

    * <a href ="https://www.youtube.com/watch?v=B1ANfsDyjeA"> What is a server </a><br>
    * <a href ="https://www.youtube.com/watch?t=33&v=iuqXFC_qIvA&feature=youtu.be"> Where are servers hosted (data centers) </a>

Do not mix up server and web server. (Check out the web server concept page to know more about this.)

</p>
