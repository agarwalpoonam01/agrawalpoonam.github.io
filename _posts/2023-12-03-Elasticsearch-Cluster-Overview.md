---
layout: post
title: "Elasticsearch Cluster Overview"
date: 	2023-12-03 12:50:00 +0300
tags: Basics 
category: Tutorial
author: Poonam Agarwal
---
### Elasticsearch Cluster Overview

	- An elasticsearch cluster is made up of number of nodes.
	- Each node is nothing but an instance of elasticsearch.
	- The data in elasticsearch is stored in index, you can compare it as database in relational database.
	- The index can have any limit of data but this can create problem while operation as the index is large.
	- Now, to deal with this situation a shard needs to be created as a unit of data that represents a subset of a larger index. There can be more than one shard for an index.
	- Shard contains data represented as documents. 
	- Documents can be compared with rows in relational database.

<div>
<figure>
<img src="{{ site.github.url }}/media/img/elasticsearch-cluster-overview.png" />
</figure>

</div>

