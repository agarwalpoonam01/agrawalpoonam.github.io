---
layout: post
title: "Zombie vs Orphan process"
date: 2020-09-15 12:10:00 +0300
tags: Zombie process,Orphan process
category: Tutorial
author: Poonam Agarwal
---

### What is process and how it is reaped when dead?
	In computing, a process is an instance of a computer program that is being executed.
	A process notifies its parent process once it has completed its execution and has exited. Then the parent process would remove the process from process table.

### What is a Zombie process?
	Also known as “defunct” or “dead” process – In simple words, a Zombie process is one that is dead but it is present in the system’s process table. If the parent process is unable to read the process status from its child (the completed process), it won’t be able to remove the process from memory and thus the process being dead still continues to exist in the process table.

	The following command can be used to find zombie processes:
	$ ps aux | egrep "Z|defunct"

	To remove Zombie process entry from process table, what can be done is to notify its parent process explicitly to remove the  entry. This can be done by sending a SIGCHLD signal to the parent process. 

	The following command can be used to find the parent process ID (PID):
	$ ps -o ppid= <child pid>

	Once you have the Zombie’s parent process ID, you can use the following command to send a SIGCHLD signal to the parent process:

	$ kill -s SIGCHLD <parent pid>

	If this does not help t delete entry ofZombie process, you will have to kill. The following command can be used to kill its parent process:

	$ kill -9 <parent pid>


### What is an Orphan process?
	An orphan process is a running process whose parent process has finished or terminated.A process can be intentionally orphaned just to keep it running.

	Any orphaned process will be immediately adopted by the special init system process. This operation is called re-parenting and occurs automatically.

	Even though technically the orphan process has the init process as its parent, it is still called an orphan process since the process that originally created it no longer exists.

	Finding a Orphan Process:
	It’s very easy to spot a Orphan process. Orphan process is a user process, which is having init (process id – 1) as parent. You can use this command in linux to find the Orphan processes.

	$ ps -elf | head -1; ps -elf | awk '{if ($5 == 1 && $3 != "root") {print $0}}' | head
	This will show you all the orphan processes running in your system. The output from this command confirms that they are Orphan processes, i.e. the process couldbe intentionally orphaned, so confirm from some other source also before killing them.

	Killing a Orphan Process:
	As orphaned processes waste server resources, so it’s not advised to have lots of orphan processes running into the system. To kill a orphan process is same as killing a normal process. gracefuly using -15 (term)

	$ kill -15 <pid>
	If that don’t work then simply use
	$ kill -9 <pid>
