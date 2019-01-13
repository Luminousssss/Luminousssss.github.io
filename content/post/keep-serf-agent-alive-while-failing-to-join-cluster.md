---
title: "Serf agent to join cluster on start"
date: 2019-01-13T19:19:32+08:00
draft: true
---

> Serf is a decentralized solution for service discovery and orchestration that is lightweight, highly available, and fault tolerant.

## Tell a serf agent to join a node on start

Using serf [config file](http://www.serfdom.io/docs/agent/options.html) `-config-file` you can indicate to your starting serf agent to join a specific node.

`"start_join":["node2_host"],`

You even can indicate multiple nodes :

`"start_join":["node2_host","node3_host"]`


If *node2_host* and *node3_host* are not available, your agent will terminate.

## Keep agent alive, even if joinning nodes failed.

Just add _localhost_ (your agent bind iface) to the list of node to join on start.

`"start_join":["node2_host","node3_host","localhost"]`


---

[serfdom.io website](http://serfdom.io)
![](/content/images/2014/Feb/serf_logo.png)