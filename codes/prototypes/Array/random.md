##### usage
~~~ts
<Array>.random(): unknown;
~~~
##### requires
[random](https://github.com/Pavez7274/Pavez7274/blob/main/codes/util/random.md)
##### example 
~~~js
var myArray = [ 'uwu', 'owo', 'unu', 'ovo' ];
console.log(myArray.random());
// logs some random value
~~~

## Code
~~~js
// import random from 'random';
Array.prototype.random = function () {
	return this[random(this.length - 1)]
};
~~~
