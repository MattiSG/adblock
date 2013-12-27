Block ad serving and tracking system-wide, even before a request is issued.


Usage
-----

	$ adblock [on]	# blocks all ad servers, shock sites, click trackers according to latest definition
	$ adblock off	# deactivates blocking, so you can access, for example, affiliate links


Installation
------------

You can download this repo as a ZIP and install the `adblock` script anywhere you want, or use this one-liner:

	curl https://raw.github.com/MattiSG/adblock/master/adblock --output /usr/local/bin/adblock && chmod u+x /usr/local/bin/adblock


What does it block?
-------------------

Ads, shock sites, hijack sites, malware servers, click trackers, popup traps (sites that make you confirm on and on), spam sending servers…

If you still see some ads after installing, please identify the domain that serves them, and send a request to Dan Pollock at hosts@someonewhocares.org.


How does it work?
-----------------

This script is a simple wrapper around downloading and installing Pollock’s [hosts file](http://someonewhocares.org/hosts/).

Dan Pollock maintains a list of servers to block based on community reports. This list is then simply formatted as a [hosts file](http://en.wikipedia.org/wiki/Hosts_file).
A hosts file maps hostnames (i.e. domains) to IPs. It does the same job as a DNS, but the lookup is made entirely locally.
We use this feature to map all the domains we want to blacklist to the IP address [`0.0.0.0`](http://en.wikipedia.org/wiki/0.0.0.0).
