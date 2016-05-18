![jetNEXUS Logo](/jetnexus.jpg)

## These Rules

These rules provide source IP address based packet filtering and/or traffic handling. There are two simple primitives you can use (and build upon);

- deny known hostile, invalid or unwanted IP addresses or address ranges (subnets) from accessing a site or service, or apply some other negative treatment
- allow permitted addresses or ranges to access a site (known customers or registered users for example,) or apply some other positive treatment

These can be used for ensuring isolation between environments and tenants using shared resources and much more. You can also use this filtering to identify and 'mark' traffic for special handling later (by inserting a specific HTTP header for example), or to route it in some unique way.

### Installation

Clone this repository, then, in the jetNEXUS GUI, browse to `Advanced > Configuration > Browse`, select the folder you cloned to and the rule you want and click on **Upload Config or jetPACK**. 

If you'd rather not use Git then click on the rule you want to install (above), then click **Raw** and then **Save [Page] As...** and download the text file to a suitable location. 

Then, in the jetNEXUS GUI, browse to `Advanced > Configuration > Browse`, choose the rule you downloaded and click on **Upload Config or jetPACK**.

Rules **must** be modified to suit your needs under: `Library > flightPATH`.

To assign rules to Virtual Services go to: `Services > IP Services > Virtual Services > flightPATH`.

### Address and Subnet Specification

You'll need to tailor any of the rules here to your specific needs. In all cases IP addresses and/or subnets are specified in the Value of a Condition using regular expressions (regexs). Here are some examples to get you started;

- a single IP address: **^10\\.11\\.12\\.99$**
- an address range: **^10\\.11\\.12\\..***
- a more specific address range (anything between 10.11.12.100 and 200): **^10\\.11\\.12\\.[1|2]00**
- multiple single addresses: **^10\\.11\\.12\\.99$|^192\\.168\\.50\\.44$**
- all loopback addresses: **^127\\.***
- all RFC1918 [https://tools.ietf.org/html/rfc1918] private addresses (which you should never see used on the Internet): **^10\..*|^172\.1[6-9]\..*|^172\\.2[0-9]\\..*|^172\\.3[0-1]\\..\*|^192\\.168\\..***

Do note that the whole address must be matched, not just part of it. You should find this site very useful for checking what you've created: https://regex101.com/.

You can only have one Condition per rule when packet filtering so your regex should encompass all the addresses and/or ranges you wish to identify. If that's not easy you can use multiple rules.

If you want to do something with traffic that **doesn't** match your regex, change the Sense from Does to Doesn't.

### Caution

In all cases you are advised to test thoroughly before deploying on any live site or service.

### User Guide

You can find the full flightPATH user guide [here](http://www.jetnexus.com/usercentral/4-1-4/flightpath.html).

### Tutorials

There are a number of useful tutorials available [here](http://www.jetnexus.com/load-balancer/resources/flightpath-tutorials/).

### Contributing

We're always happy to receive contributions and pull requests.

### License

These rules are offered license and copyright free.
