---
layout: post
title: "Elasticsearch Components"
date: 	2023-12-15 1:30:00 +0300
tags: Basics 
category: Tutorial
author: Poonam Agarwal
---
### What are the components of ELK Stack?

	- E=? Elasticsearch. 
	- It is distributed store, search and analytics engine based on Apache lucene. Elasticsearch is where indexing, search and analytics happens. 

	- L=? Logstash.
	- Collects, aggregates, enrich and ships data to elasticsearch.

	- K=? Kibana.
	- With Kibana one can explore, visualize the data in elasticsearch.

	- There are few more components that can send data to elasticsearch - Beats, APM, external services.

	- There are different kind of beats shipper, for eg. filebeat, metricbeat, packetbeat, winlogbeat etc.
	- Beats=? For eg. Filebeat can collect data from files in distributed serevrs and send data to the logstash or directly to elasticsearch.

	- APM=? Application Performane Monitoring. Capture and analyze distributed transactions in distributed system and sends the captured trace data to elasticsearch.

	- External services=? can send data directly to elasticsearch using elasticsearch api end points.


<div>
<figure>
<img src="{{ site.github.url }}/media/img/elasticsearch-components.png" />
</figure>

</div>

