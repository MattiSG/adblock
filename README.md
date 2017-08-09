Block any outgoing request to ad and tracker servers, system-wide.


Usage
-----

	$ sudo adblock [--force] [on]	# installs or updates the blocklist, --force to ignore lack of updates
	$ sudo adblock off	# deactivates blocking, so you can access, for example, affiliate links

Yes, you'll need to `sudo`, since you impact DNS resolution for the whole system.


Installation
------------

### On OS X with `brew`

If you're on OS X and use [Homebrew](http://brew.sh):

```shell
brew install mattisg/mattisg/adblock
```

### Other systems

You can download this repo as a ZIP and install the `adblock` script anywhere you want, or use this one-liner:

	sudo mkdir -p /usr/local/bin && sudo curl -\# https://raw.githubusercontent.com/MattiSG/adblock/master/adblock --output /usr/local/bin/adblock && sudo chmod u+x /usr/local/bin/adblock

Copy and paste the above to a Terminal prompt and press enter.

The `adblock` script was tried and duly tested on:
* Debian Stretch, 
* Debian Jessie.

It should work as is on many other GNU/Linux flavours.


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


Is it enough?
-------------

Using such a hosts file ensures adblocking, and a good level of privacy from tracker networks. However, I recommend to complement it with a browser plugin that can block trackers on a site-by-site basis. [Privacy Badger](https://www.eff.org/privacybadger) or [Ghostery](https://www.ghostery.com/try-us/download-browser-extension/) are good choices.

> Analytics software that tracks your behaviour can be served by each site from its own domain, thus being impossible to block on a DNS level.
> Moreover, some trackers (most notably, Google Analytics) are so common that some websites break when they are blocked, and they are thus not blocked by the hosts file. In order to prevent them from loading, yet easily load them if a site seems broken, an interactive browser plugin is easier.
