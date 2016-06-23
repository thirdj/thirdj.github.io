---
title: Verify IP Valid
---

문자열에 IP 가 포함되어 있거나 값이 IP 인지 체크 할 때

{% highlight js %}

const ip = '127.4.4.2:8080';

const filterMax = \b((?:25[0-5]|2[0-4]\d|1\d\d|[1-9]\d|\d)\.(?:25[0-5]|2[0-4]\d|1\d\d|[1-9]\d|\d)\.(?:25[0-5]|2[0-4]\d|1\d\d|[1-9]\d|\d)\.(?:25[0-5]|2[0-4]\d|1\d\d|[1-9]\d|\d)){1}([:][0-9][0-9][0-9][0-9][0-9]?)\b;  

const filterMin = /^\[\d]{1,3}.\[\d]{1,3}.\[\d]{1,3}.\[\d]{1,3}(:\[\d]+)$/g;  

let isIP = false;

if (filterMin.test(ip) === true) isIP = true;

{% endhighlight %}
