![jetNEXUS Logo](/jetnexus.jpg)

## These Rules

These rules provide geolocation-based source IP address based packet filtering and/or traffic handling. 

You can use [ISO 3166](https://dev.maxmind.com/geoip/legacy/codes/iso3166/) country codes (such as GB) or names (such as Great Britain) in your rules and also have the option of specifying [continents](https://dev.maxmind.com/geoip/legacy/codes/country_continent/).

### Installation

Clone this repository, then, in the jetNEXUS GUI, browse to `Advanced > Configuration > Browse`, select the folder you cloned to and the rule you want and click on **Upload Config or jetPACK**. 

If you'd rather not use Git then click on the rule you want to install (above), then click **Raw** and then **Save [Page] As...** and download the text file to a suitable location. 

Then, in the jetNEXUS GUI, browse to `Advanced > Configuration > Browse`, choose the rule you downloaded and click on **Upload Config or jetPACK**.

Rules **must** be modified to suit your needs under: `Library > flightPATH`.

To assign rules to Virtual Services go to: `Services > IP Services > Virtual Services > flightPATH`.

### Caution

In all cases you are advised to test thoroughly before deploying on any live site or service.

### User Guide

You can find the full flightPATH user guide [here](http://www.jetnexus.com/usercentral/4-1-4/flightpath.html).

### Tutorials

There are a number of useful tutorials available [here](http://www.jetnexus.com/load-balancer/resources/flightpath-tutorials/).

### Related Blogs

We've blogged in detail about many of these rules [here](http://blog.jetnexus.com/).

### Contributing

We're always happy to receive contributions and pull requests.

### License

These rules are offered license and copyright free.
