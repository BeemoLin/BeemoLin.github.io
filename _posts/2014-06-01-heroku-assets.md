---
layout: post
title: Can''t get CCS working on heroku
description: "Can't get CCS working on heroku using Rails 4"
modified: 2013-06-01
tags: [nginx, server]
comments: true
---

Can''t get CCS working on heroku using Rails 4

#### Setting production config
{% highlight bash %}
  vim config/environments/production.rb
{% endhighlight %}

#### find

{% highlight bash %}
  config.assets.compile = false
{% endhighlight %}

#### change to
{% highlight bash %}
  config.assets.compile = true
{% endhighlight %}

