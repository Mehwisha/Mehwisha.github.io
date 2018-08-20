---
layout: post
title:      "ORM Mapping"
date:       2018-08-20 03:29:30 +0000
permalink:  orm_mapping
---


Seeing bugs caused by backend is something most of us are accustomed to. These bugs are really due to a miss in mapping the right tables to the frontend. ORM mapping is a really important concept which many full stack developers don't really pay attention to since Active Record makes life much easier. The issue is if ORM is not understod well enough, AR(Active Record) will not help much. 

ORM starts with making a database connectiuon i.e. database_connection = SQLite3::Database.new('db/name.db'). Once the connection is established, we create a table in database. A good practice is to use a statement "If Exists".  

database_connection.execute("CREATE TABLE IF NOT EXISTS Users(id INTEGER PRIMARY KEY, name TEXT, Address TEXT, age INTEGER)")
Thirdly once the table is created, data must be added to the table. 
database_connection.execute("INSERT INTO Users (name, address, age) VALUES ('Max', '123 abc road', 23)")

So far, we have the database connection, added table and data into that table. Now how do we call all of this from classes. 

class User
 
  @@all = []
 
  def initialize(name, breed, age)
    @name = name
    @address = address
    @age = age
    @@all << self
  end
 
  def self.all
    @@all
  end
 
  def self.save(name, address, age, database_connection)
    database_connection.execute("INSERT INTO Users (name, address, age) VALUES (?, ?, ?)",name, address, age)
  end
end

Lets add some new users to the class. 

User.new("Maxine", "234 hawthorne ave", 2)
User.new("Hardy", "777 main st", 1)
 
User,all.each do |t|
  t.save(t.name, t.address, t.age, database_connection)
end

There are many more methods that we need to eplore as this is just the tip of the icerberg.

 
