munin-nexsan
============

A munin plugin for a Nexsan SAN
Created from the XML output from a Nexsan E60

Requires Ruby and the libxml-ruby gem

Munin config

	[nexsan]
	user root
	group root
	# IP address of Nexsan controller
	env.host 127.0.0.1
	# Username for admin access to the /admin/opstats.asp page
	env.user username
	# Password for the admin user
	env.password password

	Optional
	# Port used
	env.port 80
	# Time to wait before HTTP request times out
	env.timeout
	# Page to request, should never change unless Nexsan change the location of the XML page.
	env.request


data.xml - Example data to work with

The plugin currently gets the following information

* Controller CPU usage
* Controller Memory Usage
* Controller Voltages
* PSU Temp
* PSU Fan speeds
* Fan tray fan speeds
* Front panel fan speeds
* Array loads
* Port stats - MB/sec - IO/sec - Blocks/sec


Still To Do
------------

1. Get the maid stats from the nexsan
2. Tidy up the code a bit
