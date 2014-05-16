---
layout: post
title: jekyll disqus
description: "How to setting jekyll disqus"
modified: 2013-05-31
tags: [post, jekyll]
comments: true
---

## regedit disqus
register disqus and add short name for you'r jekyll blog.

## edit you'r jekyll config
In project folder _config.yml
{% highlight ruby %}
disqus_shortname: cameogen
{% endhighlight %}

## posts switch setting
In you'r post title
{% highlight ruby %}
---
layout: post
title: jekyll disqus
description: "How to setting jekyll disqus"
modified: 2013-05-31
comments: true #like this can control disqus
---
{% endhighlight %}
comments ture and false to control you'r disqus comment block show hide on post.