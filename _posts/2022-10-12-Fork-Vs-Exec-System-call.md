---
layout: post
title: "Fork vs Exec System call"
date: 	2020-10-12 12:50:00 +0300
tags: fork system call, exec sytem call
category: Tutorial
author: Poonam Agarwal
---

### What is Fork System Call?
	When a new process is created by making an exact copy of itself it is fork. As this is the exact copy the environment remains same as that of parent process with the only difference is pid.

### What is Exec System Call?
	The exec system call replaces the current process image with the new process image. We can also say that after the fork process, the address space of the child process is overwritten with the new process data.


### Fork and Exec System call together?
	The fork-and-exec switches the process with each other as in the following example:
	
<div><figure><img src="{{ site.github.url }}/media/img/forkandexec.jpg" /><figcaption></figcaption></figure></div>
	
	Have a look on the process they are same in case of fork and different incase of exec. Also the PID is different in case of fork and same incase of exec.


