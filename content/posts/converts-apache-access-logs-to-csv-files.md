---
title: "Converts Apache Access Logs to Csv Files"
date: 2017-09-20T17:23:36+05:45
draft: true
---

## Apache-Access-Log-to-CSV-Converter

Download [Apache-Access-Log-to-CSV-Converter](https://raw.githubusercontent.com/relizont/Apache-Access-Log-to-CSV-Converter/master/apache_log_to_csv_converter.php)

## Takes an Apache log of the form:

{% highlight console %}
123.45.67.890 - - [23/Sep/2011:12:13:32 -0400] "GET / HTTP/1.1" 200 2279 "http://www.some-referrer.com/referral-page/" "Some User Agent 1.0.1"
{% endhighlight %}

and converts it to:

{% highlight console %}
"IP","Time","Request_Type","Path","Response","Referral_Domain","Referral_Path","User_Agent"
"123.45.67.890","2011-09-23 12:13:32","GET","/","200","http://www.some-referrer.com/","/referral-page/","Some User Agent 1.0.1"
{% endhighlight %}

 ================
 = INSTRUCTIONS =
 ================

Use it via command line as...

{% highlight console %}
path/to/script.php relative/path/to/input_file relative/path/to/output_file.csv
{% endhighlight %}

e.g.:

{% highlight console %}
php apache_log_to_csv_converter.php access_log access_log.csv
{% endhighlight %}
