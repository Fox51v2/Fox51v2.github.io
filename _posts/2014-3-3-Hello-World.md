---
layout: post
title: "Be sure to test your code thoroughly!!"
published: true
---
## SQL Injesction and coding errors

Something that I am still learning to do is to test my code thoroughly.  What I mean is that I make a program or webpage that I believe will work but I fail to take into account the various ways that they can be broken.  One way that a web page can be broken is through text box input submissions.

In the first example I will show you is how to protect from sql injection.  Sql injdction is a technique that is used to attack data driven applications. How it works- Sql statements are inserted into an entry field for execution and the result is that database information is revealed to the attacker. Essentially the attacker inserts a statement that is always true into the text field and database information is returned.

![_config.yml]({{ site.baseurl }}/images/sqlinjection.png)

In the picture above a hacker might get access to all the user names and passwords in a database by simply inserting 105 or 1=1 into the input box.

The way to prevent this is
