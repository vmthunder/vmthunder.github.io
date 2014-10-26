---
layout: post
title: "Publication"
date: 2014-03-02 19:18:21 +0800
comments: true
categories: 
---

<a href="http://www.computer.org/csdl/trans/td/preprint/06719385-abs.html">![TPDS](http://www.computer.org/plugins/images/digitalLibrary/magazines/tpds.gif) (Publisher)</a>

VMThunder: Fast Provisioning of Large-Scale Virtual Machine Clusters
===

**Zhaoning Zhang, Ziyang Li, Kui Wu, Dongsheng Li, Huiba Li, Yuxing Peng, Xicheng Lu**

Abstract
---

Infrastructure as a service (IaaS) allows users to rent 
resources from cloud to meet their various computing 
requirements. The pay-as-you-use model, however, poses a 
non-trivial technical challenge to the IaaS cloud service 
providers: how to fast provision a large number of virtual 
machines (VMs) to meet users' dynamic computing requests? 
We address this challenge with VMThunder, a new VM 
provisioning tool, which downloads data blocks on demand 
during the VM booting process and speeds up VM image 
streaming by strategically integrating peer-to-peer (P2P) 
streaming techniques with enhanced optimization schemes 
such as transfer on demand (ToD), cache on read (CoR), 
snapshot on local (SoL), and relay on cache (RoC). In 
particular, VMThunder stores the original images in a 
share storage and in the meantime it adopts a tree-based 
P2P streaming scheme so that common image blocks are 
cached and re-used across the nodes in the cluster. We 
implement VMThunder in CentOS Linux and thoroughly test 
its performance. Comprehensive experimental results show 
that VMThunder outperforms the state-of-the-art VM 
provisioning methods, with respect to scalability, 
latency, and VM runtime I/O performance.

[Full Text (PDF)](http://www.computer.org/csdl/trans/td/preprint/06719385.pdf)

