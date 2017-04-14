---
layout: post
title:  "Introduction to MongoDb"
date:   2015-10-01 16:16:01 +00:00
categories: mongo-db roadmap
---

So far, I haven’t touched MongoDb in commercial projects at work, most of the database I worked with were relational (everything having sql as part of their name).  SQL comes from Structured Query Language, used in most of the projects that were started in the last 20 years or so.

I started to work with MongoDb for a github project with colleagues and found it very easy to setup, easy to create and easy to use. It it truly a database `made by developers for developers`.

I could only setup the project using powershell and create the database in almost no time.

You could create a collection from scratch using something similar to a concept found in frameworks like Entity Framework, code first. I only create a class and when I saved the first object in database, the data was stored with no additional steps.

I used some of the libraries, which you can find below in the article, in order to do most of the CRUD operations it was easy to have a repository pattern in place to have all the functionality available.

Now having this all set for my project I could continue doing the rest of functionality, that will be detailed in a future post.

Apart from the obvious speed, performance and the ability to store data that has or has not the same structure, you can configure it easily to scale vertically, you can find more information in this scaling in mongo db article.

There are numerous libraries that you can use for you projects (nuget packages):

* mongocsharpdriver
* MongoDB.Bson
* MongoDB.Driver
* MongoDB.QueryHelper
or at least this I use them in my project
The above ones are enough to allow you to do basic crud operations and create/drop database (document collection).

Yes, I forgot to mention the oldie, but goldie concept of relational database and relations between tables with primary and foreign keys, was replaced by a document oriented approach that allows you to store similar or not so similar data in a collection.

I would say a word of caution when changing this approach, because not all the project are the same and not all the projects require the same approach and performance; some of them need speed and the data relation is important, but others have the same structure and you need to represent data relations.

Github project can be found here: <a href="https://github.com/floradu88/DGraph/">Example repository</a>