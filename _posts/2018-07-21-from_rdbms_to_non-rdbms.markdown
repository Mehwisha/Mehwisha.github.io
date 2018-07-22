---
layout: post
title:      "From RDBMS to Non-RDBMS"
date:       2018-07-22 01:38:04 +0000
permalink:  from_rdbms_to_non-rdbms
---


Gone the days when it was very simple to retrieve data with simple select statement. Enter the world of open source, schemaless, Structured vs non Structure DBs, it is easy to get overwhelmed on what to choose and what not to choose.

Users may opt out from oracle to use Postgres, MongoDB, Cassandra,etc to save on heavy licensing fees. There is practically  no difference from Oracle to Postgres but from Oracle to MongoDB, its a whole different world. Oracle is RDBMS whereas Mongo is Non-RDBMS. MongoDB introduced schemaless structure which serves the purpose if you are facebook, twitter, etc but it may not be the solution to a small and midsize data company. Most of the educational curriculumn is based on SQL and users have given enough training on learning RDBMS. With the introduction of Social media massive dataset, storing data structually may not be possible so it will be easier to move towards Non-RDBMS DBs. 

With MogoDB,JSON was introduced and it kept everything as Key:Value pair.  Here are few key differences between MongoDB and Oracle

Oracle          MongoDB

Table             Collection
Row               Document
Column        Field

Oracle vs MongoDB Query:

Oracle:
Select * from User;

MongoDB:
db.users.find()

If application is anticipated to grow into petabytes of data, Hadoop with some scalable database will be required. With unstructure data, non-RDBMS Database will be a great use case. Every Company should see their data projection in next 5 years and see if its viable to move to non-RDBMS and RDBMS. With Database migration, employees must be well trained as nowadays everything is about data correctness. 
