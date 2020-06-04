---
layout: post
title:  Second Article
date:   2020-06-04
---
Here is a write up for the challenge called john 1 on hackertouvert.pw. 
First, you need to retrieve a user password used for an SSH connection. For that you are provided with a hash file ( mdphache )

palpaguin:$6$/V3orOfX4XBKq2wM$QHlkZE0SIPJEmhC0a7E17aS3OhVUrIqCFT8XFojSgDvyKRMHRMY9wL6sj
.N9luQzEjm6FXwV9aU6VixEvzlc5/:100:65533:Linux User,,,:/home/palpaguin:/bin/false

This is usually what you’ll find in Linux systems in the /etc/shadow file, the golden file where all the passwords are stored. Of course, the passwords are hashed , encrypted in a certain way. Otherwise the storing would not be secure.

Thus, the goal is pretty straightforward: crack the hash (which is generally what people mean by “cracking a password”). There a different ways to crack a password, one of the most obvious is the “dictionary attack”: you take a file with words and john will check the hash for those words against the one you have to crack.


Then, it is really important to have a good dictionary to crack passwords, or a list of mostly used passwords, or trying to guess the passwords based on your target (but this is more advanced).


So to crack our hash:

john --wordlist=dict.txt mdphache


After we got our password, we can login to the SSH server and recover our flag.