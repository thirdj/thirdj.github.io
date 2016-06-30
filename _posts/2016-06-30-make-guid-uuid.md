---
title: Generate GUID
---

전역 고유 식별자(全域固有識別子, 영어: Globally Unique Identifier, GUID)는 응용 소프트웨어에서 사용되는 유사 난수이다.  
GUID는 생성할 때 항상 유일한 값이 만들어진다는 보장은 없지만, 사용할 수 있는 모든 값의 수가 2128 = 3.4028×1038개로 매우 크기 때문에, 적절한 알고리즘이 있다면 같은 숫자를 두 번 생성할 가능성은 매우 적다.

GUID는 오라클 데이터베이스 등 많은 곳에서 쓰이지만, 가장 눈에 띄는 구현은 아마도 마이크로소프트의 구현일 것이다.     
표준으로는 오픈 소프트웨어 파운데이션(Open Software Foundation, OSF)이 지정한 범용 고유 식별자(Universally Unique Identifier, UUID)가 있다.

Per [Wikipedia](https://ko.wikipedia.org/wiki/%EC%A0%84%EC%97%AD_%EA%B3%A0%EC%9C%A0_%EC%8B%9D%EB%B3%84%EC%9E%90)

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
