---
title: Generate GUID
---

Example 1:
{% highlight js %}
// http://slavik.meltser.info/the-efficient-way-to-create-guid-uuid-in-javascript-with-explanation/  
function CreateGuid() {
   function p8(s) {
      var p = (Math.random().toString(16)+"000000000").substr(2,8);
      return s ? "-" + p.substr(0,4) + "-" + p.substr(4,4) : p ;
   }
   return p8() + p8(true) + p8(true) + p8();
}

var guid = CreateGuid();

// 77dc70f6-149e-45b9-871a-73ee5deae227
{% endhighlight %}

Example 2:
{% highlight js %}
// http://guid.us/GUID/JavaScript  

function createGuid(){  
   function S4() {  
      return (((1+Math.random()) * 0x10000)|0).toString(16).substring(1);  
   }  
   return (S4() + S4() + "-" + S4() + "-4" + S4().substr(0,3) + "-" + S4() + "-" + S4() + S4() + S4()).toLowerCase();  
}  

var guid = createGuid();
{% endhighlight %}

Example 3:
{% highlight js %}
// http://note19.com/2007/05/27/javascript-guid-generator/  

function createGuid() {  
   function s4() {  
      return Math.floor((1 + Math.random()) * 0x10000).toString(16).substring(1);  
   }  
   return s4() + s4() + '-' + s4() + '-' + s4() + '-' + s4() + '-' + s4() + s4() + s4();
}  

var guid = createguid();
{% endhighlight %}

Example 4:
{% highlight js %}
//http://byronsalau.com/blog/how-to-create-a-guid-uuid-in-javascript/  

function createGuid()  
{  
   return 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, function(c) {  
      var r = Math.random() * 16|0, v = c === 'x' ? r : (r&0x3|0x8);  
      return v.toString(16);  
   });  
}  
var guid = createGuid();  
{% endhighlight %}
