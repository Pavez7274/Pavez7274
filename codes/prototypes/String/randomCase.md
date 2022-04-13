## String.prototype.randomCase();
##### usage
string.randomCase();
##### exemple
~~~js
const _0 = 'aaaaaaaaaaaaaa';
console.log(_0.randomCase());
// logs something like this: AaAaAaAAaAaAAa
~~~

## Code
~~~js
String.prototype.randomCase = function(){
	return this
		.split('')
		.map(c => Math.round(Math.random() * 2) == 2
			? c.toLowerCase()
			: c.toUpperCase()
	).join('')
};
~~~
