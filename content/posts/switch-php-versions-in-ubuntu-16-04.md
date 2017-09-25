---
title: "Switch Php Versions in Ubuntu 16 04"
date: 2017-09-20T17:21:49+05:45
draft: true
---

By default Ubuntu 16.04 (Xenial) now comes with php 7.0

You can install php 5.6 in parallel and switch between them using the following instructions:
{% highlight console %}
  sudo  add-apt-repository ppa:ondrej/php
  sudo apt-get update
  sudo apt-get install php5.6 libapache2-mod-php5.6 php5.6-curl php5.6-gd php5.6-mbstring php5.6-mcrypt php5.6-mysql php5.6-xml php5.6-xmlrpc
{% endhighlight %}

Configuring and Switching Versions

{% highlight bash %}
  sudo a2dismod php7.0
  sudo a2enmod php5.6
  sudo systemctl restart apache2
{% endhighlight %}

Check php version in php file.

```
print phpversion();
```
