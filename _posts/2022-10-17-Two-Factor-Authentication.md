---
layout: post
title: "Two Factor Authentication"
date: 	2020-10-12 12:50:00 +0300
tags: 2FA, TOTP, MFA 
category: Tutorial
author: Poonam Agarwal
---
### 2 Factor Authentication

	2FA adds an extra layer of account protection by requiring two types of authentication. 
	This can be something a user knows, like a password, and something the user has, like a phone(one-time passwords), inherence factors are things that the user is, typically a biometric characteristic such as a fingerprint or an iris pattern.

### TOTP
	Time-based One-Time Passwords(TOTP) is a common form of MFA specifically based on 2 Factor Authentication. TOTP Algorithm uses current time(device or server time) and shared key as input.


### How TOTP works?
	The inputs include a shared secret key and the system time.
	Neither the inputs nor the calculation require internet connectivity to generate or verify a token. Diagram below shows this:

	
<div><figure><img src="{{ site.github.url }}/media/img/totp-2fa.jpg" /><figcaption></figcaption></figure></div>
	
	
	You can notice that the secret key and the time both at server end as well as user's end is same. And gives the passcode here for eg."343267" is same at user's as well as server's end.