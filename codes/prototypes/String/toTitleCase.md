##### usage
~~~ts
String.toTitleCase(separator?: String);
~~~
##### example 
~~~js
const _0 = 'i like the strokes';
console.log(_0.toTitleCase());
// logs: I Like The Strokes
~~~

## Code
~~~js
String.prototype.toTitleCase = function(sep = ' '){
	return this
		.split(sep)
		.map(w => w.toLowerCase().replace(w[0].toLowerCase(), w[0].toUpperCase()))
		.join(sep)
};
~~~
