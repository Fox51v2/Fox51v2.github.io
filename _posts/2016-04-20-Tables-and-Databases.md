---
published: true
layout: post
---
## A Breezy Tutorial

First I will answer the question, "What is a table?" A table is a collection of data held in a structured format within a database. It is made up of both columns and rows. The next logical question would be as to what a database is.  A database is a collection of tables queries and other data.  We will get into queries later. The method that I prefer for creating tables and databases is to import an sql file. The command to import an sql file is 
"\i FILENAME.sql" but lets not get ahead of ourselves because we need to creat the file first.

![_config.yml]({{ site.baseurl }}/images/table.png)

The above illustration is example code for creating a users table. It is a good idea to write the code for dropping a 
table just above the code for creating it.  This makes it much easier to wipe out your tables and create new ones.  This is sometimes necessary because you make create many garbage accounts for testing purposes.  Note the primary key field toward the bottom.  The purpose of the primary key is to uniquely identify each record in a database table.