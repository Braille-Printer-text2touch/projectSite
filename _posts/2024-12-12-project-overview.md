---
layout: post
title:  "Project Overview"
braille-title: "⠠⠏⠗⠕⠚⠑⠉⠞⠀⠠⠕⠧⠻⠧⠊⠑⠺"
date:   2024-12-12 8:25:00 -0500
featured: true
---
## Design

The overarching infrastructure of Text2Type is as follows.

![Design Diagram]({{ 'assets/images/design-diagram.png' | relative_url }})

There are two interfaces by which a user can interact with the printer: the web interface 
or the IPP printer interface.

Website users will be greeted with a form asking for a file to upload, which is then 
transferred to the IPP server, as this spools all print jobs and acts as reverse-proxy to the 
driver.

The IPP server itself is really just an HTTP server that is additionally equipped to handle IPP interactions. 
It masquerades as IPP server when it advertises itself on the network, but IPP jobs simply come in as 
POST requests, from which the data can be collected and parsed as though just as though it had come through the 
web interface. It communicates to the driver via a FIFO pipe on the host OS.

The driver is a combination of various functions to convert a basic ASCII subset of characters into 
proper movements of the machinery in tandem with a daemon to listen to the FIFO pipe and compute how 
the machinery should be controlled. It is currently written in Python with CircuitPy libraries, as that 
is what is offered to run [Adafruit's I2C stepper motor hat](https://learn.adafruit.com/adafruit-dc-and-stepper-motor-hat-for-raspberry-pi). 

Our progress in implementing this plan is tracked through our "progress-update" posts. The most recent one is featured at the top 
of our [home page]({{ "/" | relative_url }}).

