---
layout: post
title: "Elasticsearch at a glance"
date: 	2023-11-09 12:50:00 +0300
tags: Basics 
category: Tutorial
author: Poonam Agarwal
---
### What?
	 - ElasticSearch is a search engine (lucene based )
	 - Which stores JSON data (using the inverse index data structure) 
	 - Processes it
	 - Supports full text based search using REST APIs


### Why?
	
<div>
<figure>
<img src="{{ site.github.url }}/media/img/why-elastic.png" />
</figure>

</div>


### How?
	 - A document is like a row in a relational database, representing a given entity — the thing you’re searching for. 
	 For example, a document can represent an encyclopedia article or log entries from a web server.   
	 - An index is a collection of documents that have similar characteristics.
	 - An index in Elasticsearch is actually what’s called an inverted index.
	 - Instead of searching the text directly it searches the index.
	 - An inverted index lists every unique word that appears in any text being searched and identifies all of the saved document for each word occur. 
	 - The term “name” occurs in document A and B, so it is mapped to that document.
	 
<div>

<figure>
<img src="{{ site.github.url }}/media/img/inverted-index.png" />
</figure>

</div>
