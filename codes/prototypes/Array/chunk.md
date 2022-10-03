##### usage
~~~ts
<Array>.chunk(limit: number): any[];
~~~
##### example 
~~~js
var myArray = [ 1, 2, 3, 4, 5, 6, 7, 8, 9 ];
console.log(myArray.chunk(3));
/* returns
 * [ [1, 2, 3], [4, 5, 6], [7, 8, 9] ];
 */
~~~

## Code
~~~js
Array.prototype.chunk = function (e) {
	for (var r = Math.ceil(this.length / e), t = [], o = 0; o < r; o++)
		t[o] = this.splice(0, e);
	return t;
};
~~~
