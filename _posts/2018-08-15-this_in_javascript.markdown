---
layout: post
title:      "'This' in JavaScript"
date:       2018-08-15 14:25:53 +0000
permalink:  this_in_javascript
---


Along with other concepts in JavaScript, 'This' can be a confusing concept. Learn.co has put a simple rule which I have always come back to and have re-read several times already during the course of learning Object Oriented JavaScript:

> If this is referenced directly inside a method, it equals the object that received the method call. Otherwise this is global 

Expounding further..

>  A method is a property of an object that points to a function

So, the way I understand the above is and paraphrasing the above:


**if an object has a function as one of its properties, and 'this' is inside that function, then 'this' refers to the object.**


Example:

```
Let person = {
   name:  'Barack';
	 motto: function() { console.log(`Hello, I'm ${this.name}`) };
}

```


So,  person.motto() should put out 'Hello, I'm Barack'

One way to test if an object's property points to a function, one can just type, in this case, person.motto and that should return a function.

With the above example, it's pretty natural to think, that 'this' refers to the 'person' object, and that is my second point here:

**The object that 'this' points to should be self evident. This is like using the 'he' pronoun in a sentence instead of using always the person's name.**

I always just remember that the function which contains **'this' should be inside an object. If it's inside another function, then 'this' would no longer point to an object.**

Credits to this post:
* https://learn.co/tracks/full-stack-web-development-v6/javascript/object-oriented-js/this
* http://javascriptissexy.com/understand-javascripts-this-with-clarity-and-master-it/



