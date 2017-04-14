---
layout: post
title:  "CQRS and Web Applications"
date:   2015-06-14 16:16:01 +00:00
categories: cqrs roadmap web-apps
---

CQRS stands for Command Query Responsibility Segregation. A very useful article about this concept can be found here on <a href="https://martinfowler.com/bliki/CQRS.html">Martin Fowler website</a>.

Basically CQRS means that all the requests are separated into Commands and Queries.

* A *Command* is a change in your data for e.g. insert, update, delete DML or a task for your ORM to handle and transform it into data manipulation
* *Query* is a data retrieval from the database and this will allow you to offer BASE or Basically Available, Soft state, Eventual consistency:  
        - This means that at any moment your data might be pending a change, but at some point in time you will have a consistent data when all this ends.  
        - The data you get right now, is retrieved very fast instead of ACID way of doing things: Atomicity, Consistency, Isolation and Durability you can find more here

I found a very good example of CQRS in .net web application on this blog <a href="http://web-matters.blogspot.ro/2014/08/cqrs-with-aspnet-mvc-entity-framework.html">post</a>. But in order to build this you must first start with basic message queue. I started this github repo to show some basic examples working.

Starting from the above basic <a href="https://github.com/floradu88/ZeroMqExamples">examples</a> we will build up the framework for CQRS.