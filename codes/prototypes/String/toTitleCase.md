##### usage
~~~ts
String.toTitleCase(separator?: String): String;
~~~
##### example 
~~~js
const _0 = 'i like the strokes';
console.log(_0.toTitleCase());
// logs: I Like The Strokes
~~~

## Code
~~~js
String.prototype.toTitleCase = function () {
	return this.replace(/\w\S{1,}/gim, e => e[0]
		.toUpperCase() 
		.concat(e.slice(1))
	);
};
~~~
