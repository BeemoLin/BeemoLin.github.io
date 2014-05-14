---
layout: post_page
title: Heroku database reset
---
[How to empty DB in heroku](http://stackoverflow.com/questions/4820549/how-to-empty-db-in-heroku)
<p>
To drop the database, if you are using SHARED_DATABASE_URL:

heroku pg:reset DATABASE

To recreate the database with nothing in it:

heroku run rake db:migrate

To populate the database with your seed data:

heroku run rake db:seed

You can combine the last two into one action by executing this:

heroku run rake db:setup

Edit 2014-04-18: rake db:setup doesn't work with Rails 4, it fails with a "Couldn't create database error".

You can do this with pretty much any rake command, but there are exceptions. For example, db:reset doesn't work via heroku run rake. You have to use pg:reset instead.

More information can be found in Heroku's documentation.
</p>
