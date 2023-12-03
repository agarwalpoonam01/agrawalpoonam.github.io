---
layout: post
title: "Elasticsearch at a glance"
date: 	2023-11-09 12:50:00 +0300
tags: Basics 
category: Tutorial
author: Poonam Agarwal
---
### What?
	 ElasticSearch is a lucene based search engine which stores JSON data using the inverse index data structure, processes it and that supports full text based search using REST APIs


### Why?
	 We can perform various kind of search irrespective of there data type which included structured, unstructured, geo  and metrics data type.

	 Query can retrieve data in any form required.

	 Possible to analyze billions of records in few seconds.
	 
	 Provides aggregations which can explore trends and patterns of data.


### How?
	 A document is like a row in a relational database, representing a given entity — the thing you’re searching for. 
	 For example, a document can represent an encyclopedia article or log entries from a web server.   

	 An index is a collection of documents that have similar characteristics.

	 An index in Elasticsearch is actually what’s called an inverted index.
	 
	 Instead of searching the text directly it searches the index.
	 
	 An inverted index lists every unique word that appears in any text being searched and identifies all of the saved document for each word occur. 

	 The term “name” occurs in document A and B, so it is mapped to that document.
	 
<div>

<figure>
<img src="{{ site.github.url }}/media/img/inverted-index.png" />
<figcaption>Inverted index</figcaption>
</figure>

</div>
