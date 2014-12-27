Block any outgoing request to ad and tracker servers, system-wide.


Usage
-----

	$ sudo adblock [--force] [on]	# installs or updates the blocklist, --force to ignore lack of updates
	$ sudo adblock off	# deactivates blocking, so you can access, for example, affiliate links

Yes, you'll need to `sudo`, since you impact DNS resolution for the whole system.


Installation
------------

You can download this repo as a ZIP and install the `adblock` script anywhere you want, or use this one-liner:

	sudo mkdir -p /usr/local/bin/adblock && sudo curl -# https://raw.githubusercontent.com/MattiSG/adblock/master/adblock --output /usr/local/bin/adblock && sudo chmod u+x /usr/local/bin/adblock

Copy and paste the above to a Terminal prompt and press enter.


What does it block?
-------------------

Ads, shock sites, hijack sites, malware servers, click trackers, popup traps (sites that make you confirm on and on), spam sending servers…

If you still see some ads after installing, please identify the domain that serves them, and send a request to Dan Pollock at hosts@someonewhocares.org.


How does it work?
-----------------

This script is a simple wrapper around downloading and installing Pollock’s [hosts file](http://someonewhocares.org/hosts/).

Dan Pollock maintains a list of servers to block based on community reports. This list is then simply formatted as a [hosts file](http://en.wikipedia.org/wiki/Hosts_file).

A hosts file maps hostnames (i.e. domains) to IPs. It does the same job as a DNS, but the lookup is made entirely locally.

This feature is used to map all the domains to blacklist to the [`0.0.0.0` IP meta-address](http://en.wikipedia.org/wiki/0.0.0.0).
