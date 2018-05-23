---
layout: post
title:      "Databases- Many Choices"
date:       2018-05-23 03:33:03 +0000
permalink:  databases-_many_choices
---


Back in the days, Oracle was the only database choice which came with heavy cost. Nowadays with ever expanding data and choices, companies have started including No-SQL databases in their architecture/Infrastructure. Whether money saving is the motive or technical advancement, data must be understood well by the company. 

Many important decisons and questions needs to be answered  in order to migrate from one database to another and some of these important questions are not limited to:

1. Which type of user data exist currently?
2. How important is the security and integrity of data is for Customers/Clients?
3. Do we want to go schema less?. 
4.  What will be Knowledge/Training cost be if they moved from paid to open source?
5.  How long the training will take?

These questions needs thorough planning.  The last two questions are very important in order to keep day to day tasks rolling. Syntax from one database to another varies. How tables are called in MongoDB (No Sql) and Oracle(RDMS) are lot different. Here is little Comparison between MongoDB and Oracle:

**Oracle	                                                                                      MongoDB**
                                                                  
Table                                                                                             	Collection
Row	                                                                                                Document
Column	                                                                                        Field
Secondary Index	                                                                      Secondary Index
JOINs	                                                                                            Embedded documents, $lookup & $graphLookup
GROUP_BY	                                                                                Aggregation Pipeline


The syntax on querying the database is much different between the two

**Oracle	                                                                                       MongoDB**

INSERT INTO users (user_id, age, status)                        db.users.insert({
VALUES ('bcd001', 45, 'A');                                                      user_id: 'bcd001',
                                                                                                          age: 45,
																																																					status: 'A' })

Select * from table;                                                                   db.users.find()


Issues with Scalability, delivering faster applications and handling different datatypes is handled much nicely by NoSQL Databases. Given the dynamic nature of applications nowadays, companies should be open to adapt new emerging technologies. The above questions should be part of the thought process in order to make a valuable choice.

