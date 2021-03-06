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


## Table Organization

It is sometimes nice to split tables up in order to eliminate dependancies on non-key fields.  This is called 3nF(3rd Normal Form).  The below picture is of a table that is not 3nf.
![_config.yml]({{ site.baseurl }}/images/3nf1.png)

If you look at the table then you will see that genreType is dependant on genreID and most of all the bookID is dependant on genreID. This is known as transitive dependency. It is because of this that the table is not in 3nf.  

To make it 3nf we can split the table into two seperate tables.  Because genreID is dependant on GenreType we can easily create a sperate table with those two fields.
![_config.yml]({{ site.baseurl }}/images/3nf2.png)
The final two tables now have columns that are dependant on one primary key. Also known as 3nf.


## Limited Users

When you are interacting with a database it is good practice to use the principle of least privilege.
This means that you create a user with limited abilities for the purpose of accessing the database.  The purpose of this is to restrict what a user can do in order to prevent malicious intent.  The below illustration demonstrates the creation of a limited user on an sql page that can be imported.  Once again notice the drop role statement.  This would allow you to make changes to the privileges then recreate the role.
![_config.yml]({{ site.baseurl }}/images/role1.png)

The below image is an example of the rights that the role being created should have.  The role is allowed to connect to only one specific database and to interact with one particular table.
![_config.yml]({{ site.baseurl }}/images/role2.png)

I cannot stress enough how beneficial it is to create an sql form for handling database information.  It is far more time efficient than inputing the queries one at a time.

