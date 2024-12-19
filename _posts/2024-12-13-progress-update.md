---
layout: post
title:  "12/13/24 Progress Update"
braille-title: "⠼⠁⠃⠸⠌⠼⠁⠉⠸⠌⠼⠃⠙⠀⠠⠏⠗⠕⠛⠗⠑⠎⠎⠀⠠⠥⠏⠙⠁⠞⠑"
date:   2024-12-12 8:25:00 -0500
featured: true
---

The slides presented cooresponding to this information can be [found here]({{ site.download_link_base }}/assets/misc/12-13-presentation.pdf)

Our progress on the infrastructure is as follows.

![]({{ "/assets/images/12-13-progress.png" | relative_url }})

We've added the web interface and it's path to the driver. This means that the IPP server, too, is up and running. 
The red line leading into it represents that we have yet to get it successfully advirtising on the network 
as an IPP printer, which is our highest priority next step.

We've additionally begun working on power upgrades. Currently the Pi, steppers, and solenoids all need to be run off of 
different small power supplies. This is unweildy and not end-user-friendly, so we are working on getting just one mutli-output 
PSU off of which to run the Pi and machinery.
