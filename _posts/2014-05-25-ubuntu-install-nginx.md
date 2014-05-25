---
layout: post
title: How to instll nginx on buntu
description: "My machine OS version is ubuntu Server 14.04 LTS"
modified: 2013-05-25
tags: [nginx, server]
comments: true
---

My machine OS version is ubuntu Server 14.04 LTS

#### Setting repository and install.
{% highlight bash %}
sudo -s
nginx=stable # use nginx=development for latest development version
add-apt-repository ppa:nginx/$nginx
apt-get update
apt-get install nginx
{% endhighlight %}

#### ERROR

##### if you machine return error like this.
`add-apt-repository: command not found`

##### You must install apt plugin before you can add repository.
`sudo apt-get install software-properties-common`

#### Reference document:
<a href="http://wiki.nginx.org/Install" class="btn btn-info">Nginx wiki</a>
