Block ad serving and tracking system-wide, even before a request is issued to them.


Usage
-----

	$ adblock [on]	# blocks all ad servers, shock sites, click trackers according to latest definition
	$ adblock off	# deactivates blocking, so you can access, for example, affiliate links


How does it work?
-----------------

This script is a simple wrapper around downloading and installing Pollock’s [hosts file](http://someonewhocares.org/hosts/).

Dan Pollock maintains a list of servers to block based on community reports. This list is then simply formatted as a [hosts file](http://en.wikipedia.org/wiki/Hosts_file).
A hosts file maps hostnames (i.e. domains) to IPs. It does the same job as a DNS, but the lookup is made entirely locally.
We use this feature to map all the domains we want to blacklist to the IP address [`0.0.0.0`](http://en.wikipedia.org/wiki/0.0.0.0).
