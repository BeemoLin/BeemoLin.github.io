---
layout: post
title: Rails_bootstrap_install
description: ""
tags: [install, Rails]
comments: true
---
# Rails 專案設定 bootstrap 與 simple_form

1. gemfile的修改
# Use SCSS for stylesheets
gem 'sass-rails', '~> 4.0.0'
gem 'bootstrap-sass'

# twitter bootstrap
gem "therubyracer"
gem "less-rails"
gem "twitter-bootstrap-rails"

# simple form
gem 'simple_form'
gem 'country_select'

2. $ bundle install

3. 安装相应文件到assets目录
$ rails g bootstrap:install
$ rails generate simple_form:install --bootstrap

4. 使用bootstrap样式的simple_form

{% highlight bash %}
<div class="span12">
<%= simple_form_for @group do |f| %>
<%= f.input :title, :input_html => { :class => "input-xxlarge"} %>
<%= f.input :description, :input_html => { :class => "input-xxlarge"} %>
<div class="form-actions">
<%= f.submit "Submit", :disable_with => 'Submiting...', :class => "btn btn\
-primary"%> </div>
<% end %> </div>
{% endhighlight %}