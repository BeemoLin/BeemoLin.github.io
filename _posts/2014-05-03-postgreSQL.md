---
layout: post
title: "PostgreSQL"
description: ""
tags: [jekyll, images, test]
comments: true
---
Here are the steps I followed:

Install PostgreSQL and development package
{% highlight bash %}
	$ sudo apt-get install postgresql-9.1
	$ sudo apt-get install libpq-dev
{% endhighlight %}
Set up a user that is the same as my Ubuntu log-in
{% highlight bash %}
$ sudo su postgres -c psql
postgres=# CREATE ROLE <username> SUPERUSER LOGIN;
postgres=# \q
Modify Gemfile
{% endhighlight %}

# Remove gem 'sqlite3'
gem 'pg'
Modify database.yml in app directory

{% highlight bash %}
development:
  adapter: postgresql
  encoding: unicode
  database: appname_development
  pool: 5
  timeout: 5000
  username: <username>
  password:

test:
  adapter: postgresql
  encoding: unicode
  database: appname_test
  pool: 5
  timeout: 5000
  username: <username>
  password:
{% endhighlight %}
<code>
Run bundle install

$ bundle install
Create databases and migrations

$ rake db:create:all
$ rake db:migrate
</code>
