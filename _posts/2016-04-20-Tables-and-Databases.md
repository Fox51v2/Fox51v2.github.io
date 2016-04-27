---
published: true
layout: post
---
## A Breezy Tutorial

First I will answer the question, "What is a table?" A table is a collection of data held in a structured format within a database. It is made up of both columns and rows. The next logical question would be as to what a database is.  A database is a collection of tables queries and other data.  We will get into queries later. The method that I prefer for creating tables and databases is to import an sql file. The command to import an sql file is 
"\i FILENAME.sql" but lets not get ahead of ourselves because we need to creat the file first.

![_config.yml]({{ site.baseurl }}/images/table.png)

The above illustration is example code for creating a users table. It is a good idea to write the code for dropping a 
table just above the code for creating it.  This makes it much easier to wipe out your tables and create new ones.  This is sometimes necessary because you make create many garbage accounts for testing purposes.  Note the primary key field toward the bottom.  The purpose of the primary key is to uniquely identify each record in a database table.  In this case each user that is created would have a unique number associated with their account.


It is sometimes nice to split tables up in order to eliminate dependancies on non-key fields.  This is called 3nF(3rd Normal Form).  The below picture is of a table that is not 3nf.
![_config.yml]({{ site.baseurl }}/images/3nf1.png)

If you look at the table then you will see that genreType is dependant on genreID and most of all the bookID is dependant on genreID. This is known as transitive dependency. It is because of this that the table is not in 3nf.  

To make it 3nf we can split the table into two seperate tables.  Because genreID is dependant on GenreType we can easily create a sperate table with those two fields.
![_config.yml]({{ site.baseurl }}/images/3nf2.png)
The final two tables now have columns that are dependant on one primary key. Also known as 3nf.



