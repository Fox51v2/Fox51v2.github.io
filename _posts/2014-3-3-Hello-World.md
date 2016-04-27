---
layout: post
title: "Be sure to test your code thoroughly!!"
published: true
---
Something that I am still learning to do is to test my code thoroughly.  What I mean is that I make a program that I believe works but I fail to take into account the various ways that it can be broken.  The way a web page can be broken is through text box input submissions.

In the first example I will show you how to protect from sql injection.  Sql injdction is a technique that is used to attack data-driven applications. Sql statements are inserted into an entry field for execution and the the result is that database information is revealed to the attacker. Essentially the attacker inserts a statement that is always true into the text field.
![_config.yml]({{ site.baseurl }}/images/sqlinjection.png)

