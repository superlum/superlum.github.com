---
layout: post
title: Clean install of Mountain Lion with encrypted disk
description: 
---
I wanted to do a fresh clean install of Mountain Lion on my laptop but in order to do that, I needed to erase the disk. Since I used FileVault on the previous install, I couldn't erase the disk.

I found this [tip](http://www.drake.org.uk/2012/07/os-x-mountain-lion-clean-install-gotcha-corestorage-encrypted-disk-issue/) on the Interwebs.

You'll have to enter this command in Terminal:
<pre><code>diskutil CoreStorage list</code></pre>

Then copy the logical CoreStorage volume UIUD:
<pre><code>diskutil CoreStorage delete UUID</code></pre>

Quit Terminal and go back to Disk Utility and partition away and start on your clean install.