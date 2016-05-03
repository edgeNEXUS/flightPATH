![jetNEXUS Logo](/jetnexus.jpg)

## These Rules

These rules provide source IP address based packet filtering. They can be used in many ways including;

- To deny known hostile or invalid IP addresses or address ranges (subnets) from accessing a site or service
- Equally, to only allow permitted addresses or ranges to access a site (known customers or registered users for example)
- To provide assurance that one environment cannot communicate with another (UAT servers talking to production ones for instance) or one customer/tenant to another

### Installation

Clone this repository, then, in the jetNEXUS GUI, browse to `Advanced > Configuration > Browse`, select the folder you cloned to and the rule you want and click on **Upload Config or jetPACK**. 

If you'd rather not use Git then click on the rule you want to install (above), then click **Raw** and then **Save [Page] As...** and download the text file to a suitable location. 

Then, in the jetNEXUS GUI, browse to `Advanced > Configuration > Browse`, choose the rule you downloaded and click on **Upload Config or jetPACK**.

Rules **must** be modified to suit your needs under: `Library > flightPATH`.

To assign rules to Virtual Services go to: `Services > IP Services > Virtual Services > flightPATH`.

### Address and Subnet Specification

You'll need to tailor any of the rules here to your specific needs. In all cases IP addresses and/or subnets are specified in one or more conditions using regular expressions (regexs). Here are some examples to get you started;

- A single IP address: 10\.11\.12\.99
- An address range: 10\.11\.12.\*
- A more specific address range: 10\.11\.12\.[100-200]
- Multiple single addresses: 10\.11\.12\.99|192\.168\.50\.44

### Caution

Most of these rules can be applied with little, if any, risk but in all cases you are advised to test thoroughly before deploying on any live site or service.

### User Guide

You can find the full flightPATH user guide [here](http://www.jetnexus.com/usercentral/4-1-4/flightpath.html).

### Tutorials

There are a number of useful tutorials available [here](http://www.jetnexus.com/load-balancer/resources/flightpath-tutorials/).

### Contributing

We're always happy to receive contributions and pull requests.

### License

These rules are offered license and copyright free.
