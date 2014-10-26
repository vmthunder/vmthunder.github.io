---
layout: post
title: "Key Idears Behind VMThunder"
date: 2014-03-02 21:52:09 +0800
comments: true
categories: 
---

1. On-demand Transferring
---
The booting process of a VM requires only a small part of the image data.
We test the bootstrap process of popular operating systems, including 
Windows and various Linux distributions like Fedora, Ubuntu, OpenSUSE, 
and CentOS. We record the data access traces, including the address and 
the request time of the data blocks. The following figure shows the result.

{% img /images/img-differentos.png 450 %}

The test shows that, only a few hundreds MBs of data is required for
booting, whereas the whole image is at least GBs big. Most of the data 
is not used during the booting process, and some of data is nevever 
used during the whole life time of the VM instance. So on-demand
transferring will reduce a lot of data transferring need, escpecially
in the booting process.

2. Caching
---
Data blocks should be cached on compute nodes so that they can be reused
later, if the instance is rebooted or new instances of the image are 
created.


3. P2P Transferring
---
The data set required to boot each VM instance of the same origin image
is quite similar to one another. So data received by a compute node can 
be forwarded to another, in order to reduce pressure of image server(s), 
and to improve efficiency. P2P transferring allows image service capacity 
to scale up accordingly with the number of clients (compute nodes).

{% img /images/img-tree.png 450 %}

4. Prefetching
---
The sequence of data blocks required to boot each VM instance of the 
same origin image is quite similar to one another, too. And the sequence
is likely to stay preserved when the instance is rebooted. So we record
the sequence of each image, and use it as a predict to prefetch data
for the booting process.







