===============================
Kibana 5 Templates for Suricata
===============================

Templates/Dashboards for Kibana 5 to use with Suricata IDPS and the ELK stack

This repository provides 13 templates for the Kibana 5.x and Elasticsearch 5.x
for use with Suricata IDS/IPS - Intrusion Detection and Prevention System.

These dashboards are for use with Suricata and ELK - Elasticsearch, Logstash, 
Kibana and comprise of more than 140 visualizations and 11 searches.

The dashboards are:

 - ALL  
 - ALERTS 
 - DNS  
 - FILE Transactions  
 - FLOW  
 - HTTP  
 - IDS
 - OVERVIEW
 - SMTP
 - SSH  
 - TLS
 - VLAN
 - STATS

How to use
==========

::

     apt-get install git-core
     git clone https://github.com/aspel/KTS5.git
     cd KTS5
     
Load the dashboards: ::

 ./load.sh

You would need to select ``suricata-*`` as a default index once you open any dashboard for the first time after initial load/import.

For optimal results an example of elasticsearch template has been included under `es-template\elasticsearch5-template.json` that is used in SELKS 4.

**NOTE:**  
If the traffic you are inspecting contains vlans - in order to use the VLAN template, make sure you have enabled vlan tracking in ``suricata.yaml`` -

     vlan:
       use-for-tracking: true
