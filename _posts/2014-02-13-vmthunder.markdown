---
layout: post
title: "VMThunder"
date: 2014-02-13 11:48:46 +0800
comments: true
categories: doc
---

Creating a large number of virtual machine instances in an IaaS
cloud can be quite time-consuming, because the virtual disk
images need to be transferred to the compute nodes in prior to
booting. 

VMThunder addresses this problem by following improvements: compute node 
caching, P2P transfering and prefetching, in addition to on-demand 
transfering (network storage). VMThunder is a scalable and cost-effective
accelerator for bulk povisioning of virtual machines. And it can
be, if preferred, gracefully turned off after the booting process is
complete.

Benchmarks show that VMThunder can boot 160 VMs (CentOS 6.2 with
gnome desktop) on 160 compute nodes with in a minute, and
the average time consumption is 20 seconds. With prefetching, the
complete and average time consumption can be respecttively reduced
to 18 and 16 seconds. The network is Gigabit Ethernet for all
servers in the benchmark environment.

VMThunder can greatly improves the ***elasticity*** of a cloud system,
which is considered as a major advantage over traditional system.
VMThunder is feasible for VM cluster of any ***scale***, no matter 
large or small. VMThunder is independent of and transparent to VMM. 
That means ***any*** VMM can be supported, such as VMM, Xen, Virtual BOX, 
VMWare etc. 