##### usage
~~~ts
random(max: Number, min?: Number, decimals?: Boolean): Number;
~~~

##### example
~~~js
const _0 = random(30);
console.log(_0);
// some like 24
~~~

## Code
~~~js
function random (max, min = 0, decimals = false) {
	return decimals
		? Math.random() * (max - min) + min
		: Math.round(Math.random() * (max - min)) + min;
};
~~~
